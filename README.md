# Kafka Docker Compose Setup

Este repositorio proporciona una configuración de Docker Compose para ejecutar un clúster de Kafka localmente. Sigue los siguientes pasos para lanzar y probar Kafka utilizando Docker Compose.

## Paso 1: Clonar el Repositorio

Clona este repositorio en tu máquina local utilizando el siguiente comando:

```bash
git clone 
```
## Paso 2: Ejecutar Docker Compose
```bash
docker-compose -f kafka-docker.yml up -d
```
## Paso 3: Acceder al contenedor de Kafka
```bash
docker exec -it kafka-broker-1 bash
```
## Paso 4: Crear un tópico
```bash
kafka-topics --create --topic mi_topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
```

## Paso 5: Listar los tópicos
```bash
kafka-topics --list --bootstrap-server localhost:9092
```

## Paso 6: Crear un productor
```bash
kafka-console-producer --topic mi_topic --bootstrap-server localhost:9092
```

## Paso 7: Crear un consumidor
```bash
kafka-console-consumer --topic mi_topic --bootstrap-server localhost:9092
```

<p align="center">
  <img src="https://banner2.cleanpng.com/20180821/zwc/kisspng-node-js-javascript-express-js-portable-network-gra-mixin-software-5b7c72478c6ba0.9607634315348823755752.jpg" alt="Logo de Node.js" width="200" />
  <img src="https://e7.pngegg.com/pngimages/630/547/png-clipart-kafka-vertical-logo-tech-companies-thumbnail.png" alt="Logo de Kafka" width="200" />
</p>
