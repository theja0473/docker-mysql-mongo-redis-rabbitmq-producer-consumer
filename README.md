# Docker-mysql-mongo-redis-rabbitmq-producer-consumer
# RabbitMQ messaging system producer/consumer example

* Demonstrates example RabbitMQ simple producer/consumer running in Docker container

* Run MySQL, MongoDB, and Redis in docker

* The project can used in development environment
  hello hi
* **Do not use in production environment**

## Prerequisites

* [docker](https://docs.docker.com/install/)
* [docker-compose](https://docs.docker.com/compose/install/)
* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git/)
* [docker & docker-compose instll](https://support.netfoundry.io/hc/en-us/articles/360057865692-Installing-Docker-and-docker-compose-for-Ubuntu-20-04)

## Installing

git clone the project

```shell
git clone https://github.com/theja0473/docker-mysql-mongo-redis-rabbitmq-producer-consumer.git
```
Set the environment variable RABBIT_HOST_IP. This should be the host IP you get using e.g. ifconfig.

    $ export RABBIT_HOST_IP=<your host IP - not localhost or 127.0.0.1>  

## Running

```shell
cd docker-mysql-mongo-redis-rabbitmq-producer-consumer
docker-compose up -d

# show docker-compose log
docker-compose logs -f
```

## Databases username and password

| database | username | password |
| :------: | :------: | :------: |
|  mysql   |   root   |   root   |
|  mongo   |    /     |    /     |
|  redis   |    /     |    /     |


If your environment variable is set incorrectly, you'll get something like

    $ pika.exceptions.AMQPConnectionError: Connection to 127.0.0.1:5672 failed: [Errno 111] Connection refused
    

## Start the management interface to see the message traffic
    
    http://${RABBIT_HOST_IP}:15672 or if running locally http://127.0.0.1:15672/

    Note: The default administrator username and password are guest and guest. 
