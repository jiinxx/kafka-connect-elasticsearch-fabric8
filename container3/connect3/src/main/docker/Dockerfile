FROM confluentinc/cp-kafka-connect:latest
EXPOSE 8083

ENV CONNECT_BOOTSTRAP_SERVERS='broker:9092'
ENV CONNECT_REST_ADVERTISED_HOST_NAME=connect
ENV CONNECT_REST_PORT=8083
ENV CONNECT_GROUP_ID=compose-connect-group
ENV CONNECT_CONFIG_STORAGE_TOPIC=docker-connect-configs
ENV CONNECT_OFFSET_STORAGE_TOPIC=docker-connect-offsets
ENV CONNECT_STATUS_STORAGE_TOPIC=docker-connect-status
ENV CONNECT_KEY_CONVERTER=io.confluent.connect.avro.AvroConverter
ENV CONNECT_KEY_CONVERTER_SCHEMA_REGISTRY_URL='http://schema-registry:8081'
ENV CONNECT_VALUE_CONVERTER=io.confluent.connect.avro.AvroConverter
ENV CONNECT_VALUE_CONVERTER_SCHEMA_REGISTRY_URL='http://schema-registry_1:8081'
ENV CONNECT_INTERNAL_KEY_CONVERTER=org.apache.kafka.connect.json.JsonConverter
ENV CONNECT_INTERNAL_VALUE_CONVERTER=org.apache.kafka.connect.json.JsonConverter
ENV CONNECT_ZOOKEEPER_CONNECT="zookeeper:2181"


VOLUME ./file:/tmp/quickstart
VOLUME ./jars:/etc/kafka-connect/jars