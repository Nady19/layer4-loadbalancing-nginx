# writing docker compose file:

First declare the version

`version: '3'`

then 

`services:`

then name of the service,under the services bracket

`cont1`

then we put the build command under the cont1 bracket

`build`

then indicating from where it will build the dockerfile,it will be under the cont1 bracket

`context: ./cont1`

you can also decalre ports for the dockerfile but it will be under the services bracket

`ports:`
`     -"8080:80"`

Now in the terminal

`sudo docker-compose build`

`sudo docker-compose up`

Thus the two containers are connected via a bridge now and docker-compose is working as the l2 device.

we can `sudo docker network ls` and find this new network that we have created.

Now we can check this layer 2 network device  by 

`layer4_load_balancer_with_nginx_default`

