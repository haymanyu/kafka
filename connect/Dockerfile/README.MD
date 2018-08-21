


- Build Image

 ```
docker build -t kafka-connect-jdbc:4.1.1 .
 ```

- Run Container

 ```
docker run -d \
  --name=kafka-connect \
  -p 28082:28082 \
  -e CONNECT_BOOTSTRAP_SERVERS=<kafka-server1>:<port>,<kafka-server2>:<port>,<kafka-server3>:<port> \
  -e CONNECT_REST_PORT=28082 \
  -e CONNECT_GROUP_ID="<group-id>" \
  -e CONNECT_CONFIG_STORAGE_TOPIC=<group_conf> \
  -e CONNECT_OFFSET_STORAGE_TOPIC=<group_offset> \
  -e CONNECT_STATUS_STORAGE_TOPIC=<group_status> \
  -e CONNECT_KEY_CONVERTER="org.apache.kafka.connect.json.JsonConverter" \
  -e CONNECT_VALUE_CONVERTER="org.apache.kafka.connect.json.JsonConverter" \
  -e CONNECT_INTERNAL_KEY_CONVERTER="org.apache.kafka.connect.json.JsonConverter" \
  -e CONNECT_INTERNAL_VALUE_CONVERTER="org.apache.kafka.connect.json.JsonConverter" \
  -e CONNECT_REST_ADVERTISED_HOST_NAME="0.0.0.0" \
  -e CONNECT_LOG4J_LOGGERS=org.reflections=ERROR \
  -e CONNECT_PLUGIN_PATH=/usr/share/java \
kafka-connect-jdbc:4.1.1
 ```