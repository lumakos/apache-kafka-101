# apache-kafka-101

This guide provides instructions for installing and running Apache Kafka on a Linux system.

### Installation

1.  **Download Kafka:**
    ```sh
    wget [https://downloads.apache.org/kafka/3.8.0/kafka_2.13-3.8.0.tgz](https://downloads.apache.org/kafka/3.8.0/kafka_2.13-3.8.0.tgz)
    ```
2.  **Extract the archive:**
    ```sh
    tar -xzf kafka_2.13-3.8.0.tgz
    ```
3.  **Move Kafka to the `/opt` directory:**
    ```sh
    sudo mv kafka_2.13-3.8.0 /opt/kafka
    ```
4.  **Set the PATH:**
    Open your `~/.bashrc` file.
    ```sh
    nano ~/.bashrc
    ```
5.  Add the following line to the end of the file to include Kafka's `bin` directory in your system's PATH.
    ```sh
    export PATH="/opt/kafka/bin:$PATH"
    ```
6.  **Apply the changes:**
    ```sh
    source ~/.bashrc
    ```

---

### Start Zookeeper and Kafka

Apache Kafka requires Zookeeper to run. You will need to open two separate terminal windows for this process.

* **Terminal 1 (Start Zookeeper):**
    ```sh
    zookeeper-server-start.sh /opt/kafka/config/zookeeper.properties
    ```
* **Terminal 2 (Start Kafka):**
    ```sh
    kafka-server-start.sh /opt/kafka/config/server.properties
    ```

---

### Status Checks

You can verify that Zookeeper and Kafka are running by using the following commands:

* **Zookeeper Status:**
    ```sh
    ps aux | grep zookeeper
    ```
* **Kafka Status:**
    ```sh
    ps aux | grep kafka
    ```