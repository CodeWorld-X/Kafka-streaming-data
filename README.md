# Kafka-streaming-data
Creating Streaming Data Pipelines using Kafka

# OVERVIEW
The project aims to reduce congestion on national highways by analyzing road traffic data from various toll plazas. When a vehicle passes through a toll plaza, vehicle data such as Vehicle_id, vehicle_type, toll_plaza_id, and timestamp will be sent to Kafka. The task is to create a data pipeline to collect real-time streaming data and load it into a database.

# OBJECTIVES
In this task you will create a streaming data pipe by performing these steps:
- Start a MySQL Database server.
- Create a table to hold the toll data.
- Install the Kafka python driver.
- Install the MySQL python driver.
- Start the Kafka server.
- Create file Producer "Toll Traffic Simulator"
- Create file Consumer "streaming_data_reader.py"
- Health check of the streaming data pipeline.

# PROCESS
### 1. Create a table to hold the toll data.
    create database tolldata;
![create database](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/66ad47d0-609c-48ec-b0c6-8086feeec516)
    use tolldata;
    create table livetolldata(timestamp datetime,vehicle_id int,vehicle_type char(15),toll_plaza_id smallint);
![create table](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/a474614a-d4fa-4dd1-a1c8-038e473ed01f)

### 2. Install the Kafka python driver and MySQL python driver.
    python3 -m pip install kafka-python
    python3 -m pip install mysql-connector-python==8.0.31
### 3. Start Zookeeper
    bin/zookeeper-server-start.sh config/zookeeper.properties
![Start Zookeeper](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/c523ffb3-9ece-4dd7-8c67-91bbbcf74157)

### 4. Start Kafka server
    bin/kafka-server-start.sh config/server.properties
![Start Kafka server](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/ed33e834-8d06-4066-a5eb-88f069bcded2)

### 5. Create a topic 
    bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic toll
![Create a topic ](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/83e49ef2-2244-4ed5-83a2-4b5670d670da)

### 6. Create file Producer "Toll Traffic Simulator"
![toll_traffic_generator](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/be2ab827-1aa5-42f2-bfda-7600b069cdf6)

### 7. Create file Comsumer "streaming_data_reader.py"
![streaming_data_reader](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/9e2efc08-ace9-43f9-92bf-8a3e83151103)

### 8. Run the Toll Traffic Simulator
![run toll trafic](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/90f5fda9-503e-4af4-9a4c-886a5f1b64a5)

### 9. Run streaming_data_reader.py
![run streaming data](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/4c4be518-ee89-4e38-845c-c46c15b8ae4c)

### 10. Health check of the streaming data pipeline.
![load data in db](https://github.com/CodeWorld-X/Kafka-streaming-data/assets/129016922/46256c60-8c33-4dcc-a8e2-fd0dfaa4faa5)






    
    
