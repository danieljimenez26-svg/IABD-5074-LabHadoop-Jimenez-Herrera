# Laboratorio Apache Hadoop Multi-Nodo con Docker (HDFS y YARN)

* **Alumno:** Daniel Jiménez Herrera
* **Curso:** CE en Inteligencia Artificial y Big Data
* **Módulo:** Sistemas de Big Data (5074 / 5075)

## Arquitectura desplegada
Clúster distribuido de Apache Hadoop 3 levantado con Docker Compose sobre la red interna `hadoop-net`:
* **`namenode`**: Maestro HDFS (puerto web `9870`).
* **`datanode1`, `datanode2`, `datanode3`**: Trabajadores HDFS con bloques de `64 MiB` y factor de replicación `R=2`.
* **`resourcemanager`**: Maestro YARN (puerto web `8088`).
* **`nodemanager`**: Trabajador YARN para ejecución de contenedores MapReduce.

## Estructura del repositorio
* `docker/`: Archivos de infraestructura como código (`docker-compose.yml` y `config`).
* `evidencias/`: Capturas de pantalla de las comprobaciones en HDFS y YARN.
* `informe/`: Memoria técnica completa de la práctica en formato PDF.

## Comandos principales
```bash
cd docker
docker compose up -d
docker compose down -v




