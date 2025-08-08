# apache-kafka-101

Install ApacheKafka in Linux

1. wget https://downloads.apache.org/kafka/3.8.0/kafka_2.13-3.8.0.tgz
2. tar -xzf kafka_2.13-3.8.0.tgz
3. sudo mv kafka_2.13-3.8.0 /opt/kafka
4. nano ~/.bashrc
5. Add the PATH "export PATH="/opt/kafka/bin:$PATH"
6. source ~/.bashrc


## Start Zookeeper and Kafka
terminal 1 
zookeeper-server-start.sh /opt/kafka/config/zookeeper.properties

terminal 2 
kafka-server-start.sh /opt/kafka/config/server.properties

### Zookeeper Status
ps aux | grep zookeeper

### Kafka Status
ps aux | grep kafka