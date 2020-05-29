# Docker-elk-using-docker
ELK on docker 

Pre-requisite installations : 

 1. Docker 
 2. Java 

Steps to setup ELK stack using docker containers

1. Clone the git repository :
```bash
git clone https://github.com/deviantony/docker-elk.git
```

2. To run the stack, get inside the directory and run docker-compose
```bash
cd /docker-elk
docker-compose up -d
```

3.  Verify the installation.
```bash
sudo docker ps
```   

4. Access Kibana by entering: `http://localhost:5601` in your browser.
  
5. Post data to elasticsearch using Postman or curl 
```bash
curl -XPUT \
-u elastic:changeme http://localhost:9200/movies/_doc/1 \
-d '{"director": "Burton, Tim", \
  "genre": ["Comedy","Sci- Fi"], "year": 1996, \
  "actor": ["Jack Nicholson","Pierce Brosnan","Sarah Jessica Parker"],\
  "title": "Mars Attacks!"}'\
-H 'Content-Type: application/json'
```
  
