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
If you run into an error starting elasticsearch saying somthing like
```
max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
```
you need to issue the command:
```
sudo sysctl -w vm.max_map_count=262144
```
to increase 

## Usefull commands
**Show all elasticsearch indices**<br>
`curl http://127.0.0.1:9200/_cat/indices?v` (from within the elastic-container)<br>
Should give you a quickstart-jdbc-test-index

**Show all in index**<br>
`curl http://127.0.0.1:9200/quickstart-jdbc-test/_search` (from within the elastic-container)

The vm_map_max_count setting could be set permanently in /etc/sysctl.conf:

`grep vm.max_map_count /etc/sysctl.conf`

vm.max_map_count=262144
