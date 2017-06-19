# Test-installation Kafka-Elasticsearch using fabric8
This is a prof of concept installation for a Kafka-Elasticsearch-stack using mysql as source

##Run
clone the repository
git clone http://github.com
##Usefull commands
**Show all indeces**<br>
curl http://127.0.0.1:9200/_cat/indices?v

**Show all in topic**<br>
curl http://127.0.0.1:9200/quickstart-jdbc-test/_search