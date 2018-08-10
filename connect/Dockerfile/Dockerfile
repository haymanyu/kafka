# Base image:
# https://github.com/confluentinc/cp-docker-images/blob/master/debian/kafka-connect-base/Dockerfile

# Using conflunet-connect in distributed mode.
# Informations about configuration, offset, statu will stored in topics.
# If there are more than one team using the kafka-cluster, ACL should be enabled.



# Builds a docker image for Kafka JDBC Connect
# Volumes in base image:
# driver jars: /etc/kafka-connect/jars
# keyfile: /etc/kafka-connect/secrets
# Default kafka-connect rest.port = 8083


# plugins:
# Debezium CDC postgres-0.8.1

FROM confluentinc/cp-kafka-connect:4.1.1
MAINTAINER 	HaymanYu<hayman.yu@letote.cn>
COPY lib/* /etc/kafka-connect/jars/
