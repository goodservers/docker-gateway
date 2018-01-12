# Docker gateway
Simple gateway for any kind of Docker application. Automatic handles domains, letsencrypt certificates, nginx settings and containers health. No setup needed. Gateway consists of from 4 containers:
* [nginx reverse proxy](https://github.com/jwilder/nginx-proxy),
* [nginx settings generator](https://github.com/jwilder/docker-gen),
* [letsencrypt certificates handler](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion)
* [container health checker - zero downtime deployment](https://github.com/goodservers/docker-gateway).

## Setup on server
Init network `docker network create nginx-proxy`
Run gateway `docker-compose up`

## Pros & Cons
+ Supports docker compose (multiple services in deploy)
+ unlimited projects on own server
+ free unlimited web SSL certificates
+ zero downtime deployment
+ all stored in Docker containers => easy future Kubernetes or Cloud migration
+ simple migration
+ scaling of each instance
- needs a little bit more setup in project
