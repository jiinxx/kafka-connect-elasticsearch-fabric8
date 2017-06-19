# Test-installation Kafka-Elasticsearch using fabric8
This is a prof of concept installation for a Kafka-Elasticsearch-stack using mysql as source

## Getting it up and running
Clone the repository:
```
git clone https://github.com/jiinxx/kafka-connect-elasticsearch-fabric8.git
```
Jump into project folder and build the workspace using:
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
**Show all elasticsearch indices**<br>
`curl http://127.0.0.1:9200/_cat/indices?v` (from within the elastic-container)<br>
Should give you a quickstart-jdbc-test-index

**Show all in index**<br>
`curl http://127.0.0.1:9200/quickstart-jdbc-test/_search` (from within the elastic-container)