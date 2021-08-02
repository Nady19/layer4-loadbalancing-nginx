# Layer-4 Load Balancer with Nginx

***Step by step compilation:***

    
    cd webapp
    

    docker build -t webapp .

We will run this image that we have built for 2 separate containers at 2 different ports


    docker run -p 8000:80 webapp
    

    docker run -p 7000:80 proxy
    
Open another tereminal and check

    sudo docker ps

Now just executing the second container:

    sudo docker exec -it ef684fa3cb5f sh

Changing 2nd Container index.html file from here:

     /usr/share/nginx/html/index.html
    
Reloading since we changed
 
    docker exec ef684fa3cb5f nginx -s reload
    
Checking in the browser

    localhost:8000


    localhost:7000
    
Another terminal:
    
**Go to proxy Directory**

    cd proxy
    
usual steps now:

    docker build -t nady/proxy .


    docker run -p 80:80 nady/proxy
    
Checking localhost

    localhost:80

