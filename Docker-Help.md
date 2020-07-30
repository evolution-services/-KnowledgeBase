## Setup RabbitMQ Docker
docker run -d — hostname rabbitmq — name rabbitmq -p 8080:15672 -p 5672:5672 -p 25676:25676 rabbitmq:3-management


## Setup ElasticSearch Docker
docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -e "transport.host=127.0.0.1" -e ELASTIC_PASSWORD="my@password" --name elastic docker.elastic.co/elasticsearch/elasticsearch:7.5.2

## Setup Kibana Docker
docker run --link elastic:elastic-url -e "ELASTICSEARCH_URL=http://elastic-url:9200" -e ELASTICSEARCH_PASSWORD="my@password" -p 5601:5601 --name kibana docker.elastic.co/kibana/kibana:6.8.11 

## Setup Kibana Dashboard
docker run --net="host" docker.elastic.co/beats/metricbeat:7.8.1 setup -e \ -E output.logstash.enabled=false \ -E output.elasticsearch.hosts=['localhost:9200'] \ -E output.elasticsearch.username=metricbeat_internal \ -E output.elasticsearch.password="my@password" \ -E setup.kibana.host=localhost:5601

## Delete every Docker containers
#### Must be run first because images are attached to containers

docker rm -f $(docker ps -a -q)

## Delete every Docker image

docker rmi -f $(docker images -q)
