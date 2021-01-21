# learn-kafka-streams
Learning Apache Kafka Streams 

# Download Apache kafka
https://downloads.apache.org/kafka/2.7.0/kafka_2.13-2.7.0.tgz

# Reference
https://www.javatpoint.com/installing-apache-kafka-on-macos

# Testing the downloaded copy
- To test, use '/bin/kafka-topics.sh'. If it gives the correct output means java is working.

# Starting kafka
- Apache Kafka needs zookeeper to be up 

## Starting Zookeper
- Create a data directory for zookeeper logs e.g. data/zookeeper
- edit the config/zookeeper.properties and update the datadir variable with this new path
- start the zookeeper with bin/zookeeper-server-start.sh config/zookeeper.properties that should also create a version-2 directory under kafka/zookeeper

- Once the zookeeper is started, its time to start kafka
- create a similar data directory for kafka logs e.g. data/kafka
- edit the config/server.properties and update the log.dirs variable with this new path
- start the kafka server with bin/kafka-server-start.sh config/server.properties

# Creating topics


# Producer and Consumer
### Producer 
`bin/kafka-console-producer.sh --broker-list localhost:9092 --topic first_topic`
### Consumer
`bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first_topic`
