# sample-NGINX-load-balancer
A sample load balancer for scaling your service

Dockerfile:
creates new image out of default NGINX image; overwrites default configuration settings with those specified in the .conf file

NGINX config:
sets up container to serve as load balancer; will load balance between the specified servers for all http traffic hitting this container. Specify a balancing algorithm before listing out your servers (see https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/#method for more info on different algorithms).


# docker commands
docker build -t jbframe/[iamge nname] .
docker push jbframe/[iamge name]
docker run --name [container name] -p 80:80 -d jbframe/[iamge name]
