# sample-NGINX-load-balancer
A sample load balancer for scaling your service

Dockerfile:
creates new image out of default NGINX image; overwrites default configuration settings

NGINX config:
sets up container to serve as load balancer; will load balance between the specified servers for all http traffic hitting this container. Specify a balancing algorithm before listing out your servers (see https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/#method for more info on different algorithms).

