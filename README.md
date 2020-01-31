# Development Kafka Environment for Windows

Supports setup of a local single node kafka cluster with a simple Web UI using docker-compose.

## Prerequisites

You may need to create a free docker hub login if you do not already have one.

[Docker for Windows download](https://docs.docker.com/docker-for-windows/install/)

After downloading the windows exe and installation you will have docker installed on your workstation.
Requires Windows 10 Pro with Hypervisor Support.
Docker installation needs a reboot.

## Getting Started

Running ```docker-compose up``` in a powershell should get you started.

Now you can go to your browser and hit localhost:9000 which will open the kafdrop UI.
You can connect your local kafka client with localhost:9092 to the cluster.

If you are done shutdown the cluster with ```docker-compose down```.

In case docker complains with *up* that the container already exists run ```docker ps -a``` and ```docker rm [id]``` to remove the container kafka and zookeeper that might have been left over after an inproper shutdown.

In case you want to drop the data and run with a fresh setup run ```docker volume ls``` and delete the kafka-docker volumes.
