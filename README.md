# SwiftLing App - Kafka Docker Compose Setup

## Overview

This repository provides a `docker-compose.yml` file to set up Kafka for asynchronous communication between microservices within the SwiftLing application.

## Prerequisites

Ensure the following dependencies are installed on your system:

- **Docker** (latest version recommended)
- **Docker Compose** (If using standalone Docker installations)

## Running Kafka

1. Clone the repository:

   ```sh
   git clone https://github.com/CundullahT/swiftling-kafka-docker-compose.git
   cd swiftling-kafka-docker-compose
   ```

2. Start the container:

   ```sh
   docker-compose up
   ```

3. Wait until you see the below INFO log message:
   ```
   Kafka Server started (kafka.server.KafkaRaftServer)
   ```
   
   Access Kafka in your browser:
   ```
   http://localhost:9092
   ```

## Stopping and Removing Container

To stop and remove the running container, execute:

```sh
docker-compose down
```

## Additional Information

- Ensure that each microservice is configured to use the correct **Realm Name** and **Client ID**.
- Each microservice that integrates with Kafka should set the `spring.kafka.bootstrap-servers` config in its configuration file (application.yml or application.properties).

## License

This project is licensed under [MIT License](LICENSE).
