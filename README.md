# streaming-apps-of-today
This repository contains streaming application development using :

1) Kafka
2) Spark Streaming

# Kafka setup commands with docker

1) Install Docker Toolbox and open docker quickstart terminal and run commands from step-2 to 15
2) docker-machine create --driver virtualbox default
3) docker-machine start
4) docker-machine env
5) docker search kafka
6) docker pull spotify/kafka
7) docker run -p 2181:2181 -p 9092:9092 --env ADVERTISED_HOST=192.168.99.100 --env ADVERTISED_PORT=9092 --name kafka -d spotify/kafka
8) docker exec -it kafka bash
9) /opt/kafka*/bin/kafka-topics.sh --zookeeper localhost:2181 --create --topic sourcetopic --partitions 1 --replication-factor 1
10) /opt/kafka*/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic sourcetopic
11) /opt/kafka*/bin/kafka-console-consumer.sh --zookeeper localhost:2181 --topic targettopic --from-beginning
12) /opt/kafka*/bin/kafka-topics.sh --zookeeper localhost:2181 --list
13) docker rm -f kafka
14) docker ps
15) docker-machine stop
