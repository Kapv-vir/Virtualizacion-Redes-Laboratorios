# Persistencia de Datos con Docker y MariaDB

## Descripción

En esta práctica se demostró el funcionamiento de contenedores efímeros y persistentes utilizando Docker y MariaDB.

Primero se creó un contenedor sin volumen para comprobar que los datos se pierden al eliminar el contenedor. Posteriormente, se utilizó un volumen Docker para mantener la persistencia de la información incluso después de recrear el contenedor.

---

# Objetivo

Comprender el uso de volúmenes en Docker y su importancia para mantener la persistencia de datos en aplicaciones como bases de datos.

---

# Comandos utilizados

## Crear contenedor sin volumen
docker run -d --name db-efimera -e MYSQL_ROOT_PASSWORD=123 mariadb

## Acceder a MariaDB
docker exec -it db-efimera mariadb -u root -p

## Crear volumen Docker
docker volume create mi-data-db

## Crear contenedor con volumen
docker run -d --name db-persistente -v mi-data-db:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123 mariadb

## Verificar volumen
docker volume inspect mi-data-db

---

# Video de evidencia:
https://www.youtube.com/watch?v=1QE-y3tlP9w&authuser=1

---

<img width="1431" height="849" alt="EVIDENCIA DE DOCKER" src="https://github.com/user-attachments/assets/f1f12f42-0d2b-4cf9-8ca5-e700f6a78974" />

