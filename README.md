# kafka-commands
- ## Run Zookeeper Service  (keep window open)

.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

- ## Run Kafka Service (keep window open)

.\bin\windows\kafka-server-start.bat .\config\server.properties

- ## Execute One-Time Commands - create, list, delete topics 

.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic kafka-notes
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list

- ## Run Kafka Producer (will provide a > prompt for writing messages)

.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic kafka-notes

- ## Run Kafka Consumer (to show messages from the beginning)

.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic kafka-notes --from-beginning
