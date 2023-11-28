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