# Kafka in Docker Quick Setup
A quick setup for running Kafka in Docker involves pulling the Kafka image from Docker Hub and running a Kafka container. Here’s a brief description:

1. **Pull the Kafka Image**:  
   Run `docker pull apache/kafka:3.8.0` to fetch the Kafka image version 3.8.0 from Docker Hub.

```sh
docker pull apache/kafka:3.8.0
```

2. **Run a Kafka Container**:  
   Use the command `docker run --name my-kafka -p 9092:9092 apache/kafka:3.8.0` to start a Kafka container named "my-kafka" in detached mode.

```sh
docker run --name my-kafka -p 9092:9092 apache/kafka:3.8.0
```

3. **Create a Topic in Kafka**:  
    Use local kafka client for connecting to kafka server `bin/kafka-topics.sh --create --topic quickstart-topic --bootstrap-server localhost:9092`, To download the Kafka client 3.8.0 click the [Link](https://dlcdn.apache.org/kafka/3.8.0/kafka_2.13-3.8.0.tgz) then extract and start using the client.

```sh
bin/kafka-topics.sh --create --topic quickstart-topic --bootstrap-server localhost:9092
```

4. **To know more about the topic**:
    Use the below command to know more about the topic `bin/kafka-topics.sh --describe --topic quickstart-topic --bootstrap-server localhost:9092`
```sh
bin/kafka-topics.sh --describe --topic quickstart-topic --bootstrap-server localhost:9092
```