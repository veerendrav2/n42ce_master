# About this Repo

This is the Git repo of the Docker [official image](https://docs.docker.com/docker-hub/official_repos/) for [n42ce_master](https://hub.docker.com/r/n42inc/n42ce_master/). See [the Docker Hub page](https://hub.docker.com/r/n42inc/n42ce_master/) for the full readme on how to use this Docker image and for information regarding contributing and issues.

Reside on swarm master , listen swarm events and send to redis.[n42ce_slave](https://hub.docker.com/r/n42inc/n42ce_slave/) reside on swarm slave node's and listen events from redis.


Docker deployment monitoring for applications, collects data to provide application topology discovery, multilayer diagnostic views and application sub components performance analytics

## Method 1:
wget -O n42inc_communityedition.sh https://raw.githubusercontent.com/N42Inc/docker-compose/master/n42inc_communityedition.sh && sudo bash n42inc_communityedition.sh <edge_servers>

Replace edge_servers with the userkey provided by N42.

Requirments:
      1.docker compose
      2.python
      
## Method 2

This image only contains swarm events listener.
## How to use this image
1.Drop a mail to <b>info@networks42.com</b> for the key

2.Launch docker image with provided key

### Without a Dockerfile
If you don't want to include a Dockerfile in your project, it is sufficient to do the following:
```
docker run --net=host   -e key=test_key -it --name=n42ce_master -d  n42inc/n42ce_master:latest
```
3.Ports open on firewall :
```
   redis: Port:6379  IP: 52.73.171.150   
```
4.Log into [http://54.67.112.100:8080/](http://54.67.112.100:8080/)  with provided crediantials.
