WebRTC Showcase
==================

This is Play Framework application with Scala | Akka | WebSockets.
It connects users with Kurento Media Server to implement video chat functionality.

### Features
 
 - presenters may publish own web cam and microphone to large auditory (100 users)
 
 - low latency;
 
 - there could be severals rooms at the same time;
 
 - a quick jump into one of the multiple rooms;
 
 - easy to run locally or deploy to a server; 

 - simple chat and list of connected users.


### Setup
 
 - Oracle Java 8 must be installed
 
 - Install [Docker](https://www.docker.com/community-edition#/download) compose installed
 
 - Install [SBT](http://www.scala-sbt.org/release/docs/Setup.html) tool installed
 
 - Bind _local.trembit.com_ domain in _hosts_ file
 
 - Generate HTTPS certificates and put to nginx/certs `sudo certbot certonly --standalone -d local.trembit.com`
 
 - Generate `openssl dhparam -out nginx/certs/ssl-dhparams.pem 2048`
 
 - Run `sbt run`
 
 - Run `docker-compose up` (runs Kurento infrastructure) 
 
 - Open https://local.trembit.com page in 2 browsers and start broadcast in one of them

On remote server requires HTTPS to be used. It could be done with nginx proxy and HTTPS certificate generated with Let’s Encrypt.
https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion
