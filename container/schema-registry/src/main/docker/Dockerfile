FROM rta/kafka-base

ENV COMPONENT=schema-registry

# Default listener
EXPOSE 8081

RUN yum -y install confluent-${COMPONENT} \
    && mkdir -p /etc/${COMPONENT}/secrets \
    && chmod -R ag+w /etc/${COMPONENT} /etc/${COMPONENT}/secrets

VOLUME ["/etc/${COMPONENT}/secrets"]

COPY include/etc/confluent/docker /etc/confluent/docker

CMD ["/etc/confluent/docker/run"]