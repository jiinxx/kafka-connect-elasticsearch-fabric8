# Test-installation Kafka-Elasticsearch using fabric8
This is a prof of concept installation for a Kafka-Elasticsearch-stack using mysql as source

## Getting it up and running
Clone the repository:
```
git clone https://github.com/jiinxx/kafka-connect-elasticsearch-fabric8.git
```
Jump into container directory,`cd containers`, as thats where allt the interresting parts are<br>
Build the workspace using:
```
mvn docker:build
```
Run the build using:
```
mvn docker:start
```
and stop with:
```
mvn docker:stop
```

## Usefull commands
**Show all elasticsearch indeces**<br>
`curl http://127.0.0.1:9200/_cat/indices?v` (from within the elastic-container)

**Show all in topic**<br>
`curl http://127.0.0.1:9200/quickstart-jdbc-test/_search` (from within the elastic-container)