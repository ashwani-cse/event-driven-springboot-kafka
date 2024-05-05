# event-driven-springboot-kafka
This repository contains a demonstration of building microservices with Spring Boot for producing and consuming messages using Apache Kafka, showcasing an event-driven architecture.

## Features

- **Event-Driven Architecture:** Illustrates how to implement event-driven communication patterns using Kafka and Spring Boot, enabling loose coupling and scalability.
- **Producer Microservice:** A Spring Boot application responsible for generating events and publishing them to Kafka topics.
- **Consumer Microservice:** Another Spring Boot application that subscribes to Kafka topics, processes incoming events, and triggers appropriate actions.
- **Real-Time Data Processing:** Demonstrates how Kafka facilitates real-time data processing and analytics by streaming events between microservices.
- **Scalable and Resilient:** Shows how Kafka's distributed nature ensures scalability and fault tolerance in handling large volumes of data and processing events.

## Kafka Setup on Local

To run the Kafka producer and consumer locally, you need to have Apache Kafka installed. You can follow the steps below to set up Kafka on your local machine:

1. **Download Apache Kafka:**
   Download Apache Kafka from the [official website](https://kafka.apache.org/downloads).

2. **Extract the Archive:**
   Extract the downloaded Kafka archive to a directory of your choice.

3. **Start Zookeeper:**
   Navigate to the Kafka directory and start Zookeeper using the following command:

   bin/zookeeper-server-start.sh config/zookeeper.properties

5. **Start Kafka Broker:**
Open a new terminal window, navigate to the Kafka directory, and start the Kafka broker using the following command:
bin/kafka-server-start.sh config/server.properties

6. **Create Kafka Topics:**
You can create Kafka topics either manually or by running the application. If you want to create topics manually, you can use the following commands:

bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3 --topic topic-with-partitions-3
bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3 --topic message-payload-topic


## Clone Repository

To clone this repository, use the following steps:

1. **Clone the Repository:**
git clone <repository_url>


2. **Navigate to Project Directory:**
cd kafka-producer-consumer

## Run Spring Boot Application To run the Spring Boot application, follow these steps: 1. **Build the Project:**
mvn clean install


2. **Run the Application:**
mvn spring-boot:run


Once the application is running, you can produce messages through the Kafka topics using specified endpoint.
curl --location 'http://localhost:8081/publish' \
--header 'Content-Type: application/json' \
--data '{
    "message": "#test message3 partion -> 0"
}'







