# Event-Driven Spring Boot with Kafka

This repository contains a demonstration of building microservices with Spring Boot for producing and consuming messages using Apache Kafka, showcasing an event-driven architecture.

## Features

- **Event-Driven Architecture:** Illustrates how to implement event-driven communication patterns using Kafka and Spring Boot, enabling loose coupling and scalability.
- **Producer Microservice:** A Spring Boot application responsible for generating events and publishing them to Kafka topics.
- **Consumer Microservice:** Another Spring Boot application that subscribes to Kafka topics, processes incoming events, and triggers appropriate actions.
- **Real-Time Data Processing:** Demonstrates how Kafka facilitates real-time data processing and analytics by streaming events between microservices.
- **Scalable and Resilient:** Shows how Kafka's distributed nature ensures scalability and fault tolerance in handling large volumes of data and processing events.

## Kafka Setup on Local

To run the Kafka producer and consumer locally, you need to have Apache Kafka installed. Follow the steps below to set up Kafka on your local machine:

1. **Download Apache Kafka:**
   Download Apache Kafka from the [official website](https://kafka.apache.org/downloads).

2. **Extract the Archive:**
   Extract the downloaded Kafka archive to a directory of your choice.

3. **Start Zookeeper:**
   Open a new terminal, navigate to the Kafka directory and start Zookeeper using the following command:
   ```bash
   bin/zookeeper-server-start.sh config/zookeeper.properties
   ```

4. **Start Kafka Broker:**
   Open a new terminal window, navigate to the Kafka directory, and start the Kafka broker using the following command:
   ```bash
   bin/kafka-server-start.sh config/server.properties
   ```

5. **Create Kafka Topics:**
You can create Kafka topics either manually or by running the application. If you want to create topics manually, you can use the following commands:
   ```bash
   bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic message-payload-topic --partitions 3 --replication-factor 1
   ```

## Repositories Setup

1. **Clone the both Repositories:**
- Producer Repository: [kafka-producer-service](https://github.com/ashwani-cse/kafka-producer-service)
- Consumer Repository: [kafka-consumer-service](https://github.com/ashwani-cse/kafka-consumer-service.git)

2. **Navigate to Each Project Directories:**
   ```bash
   cd repository-name
   ```

## Run Spring Boot Application 
### To run the Spring Boot application, follow these steps: 
1. **Build the Project:**
   ```bash
   mvn clean install
   ```

3. **Run the Application:**
   ```bash
   mvn spring-boot:run
   ```

Once the application is running, you can produce messages through the Kafka topics using a specified endpoint.
   ```bash
   curl --location 'http://localhost:8081/publish' \
   --header 'Content-Type: application/json' \
   --data '{
       "message": "#test message3 partion -> 0"
   }'
   ```

## Stay Connected

Connect with us on social media and stay updated with the latest news and developments:

- [LinkedIn](https://www.linkedin.com/in/ashwanicse/)
- [Leetcode](https://leetcode.com/ashwani__kumar/)
- [Topmate](https://topmate.io/ashwanikumar)

## Subscribe to our Newsletter
Stay ahead of the curve by subscribing to our LinkedIn newsletter:
- [Subscribe Now](https://www.linkedin.com/newsletters/7084124970443767808/)





