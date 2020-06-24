# Elasticsearch, Logstash, Filebeat, Kibana in dockers

## Setup

### 1 Initial configuration
In the file .env you can configure ELK_VERSION you needed and initial ELK_PASSWORD for username elastic.
Example:
```
ELK_VERSION=7.8.0
ELK_PASSWORD=changeme
```
### 2 Download
```
git clone https://github.com/aleksandryz/elkdockers.git
cd elkdockers
```
### 3 Create certificates (Runs only once)
```
docker-compose -f create-certs.yml run --rm create_certs
```
### 4 Run dockers
```
docker-compose up -d
```
### 5 Open https://DOCKER_HOST_IP:5601/
