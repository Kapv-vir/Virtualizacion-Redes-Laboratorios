## Descripción

En esta práctica se realizó el proceso de publicación y versionado de una imagen personalizada utilizando Docker Hub.

Se creó el versionado semántico de la imagen mediante etiquetas, se publicó en un repositorio remoto y posteriormente 
se recuperó desde Docker Hub para verificar su funcionamiento.

## Objetivo

Aprender a publicar imágenes Docker en Docker Hub, aplicar versionado mediante etiquetas y recuperar imágenes desde un repositorio remoto.

## Herramientas utilizadas

- Docker
- Docker Hub
- Ubuntu
- VirtualBox
- GitHub

- ## Comandos utilizados

docker login -u kapv

docker tag mi-web-personalizada:latest kapv/bci-web:1.0.0

docker tag mi-web-personalizada:latest kapv/bci-web:stable

docker push kapv/bci-web:1.0.0

docker push kapv/bci-web:stable

docker rm -f $(docker ps -aq)

docker rmi -f $(docker images -q)

docker run -d -p 8080:80 kapv/bci-web:stable

docker ps

docker history kapv/bci-web:stable

## Evidencias

### Historial de construcción de la imagen
<img width="1438" height="832" alt="GITHUB" src="https://github.com/user-attachments/assets/3f1ff18b-53f7-4f5e-b90e-9c9d40f0d84f" />

## Video de la práctica
https://www.youtube.com/watch?v=FDxQ1-up7s0&authuser=1

## Repositorio Docker Hub

https://hub.docker.com/r/kapv/bci-web

## Conclusiones

Durante esta práctica se aprendió a utilizar Docker Hub como repositorio remoto para almacenar imágenes Docker.

También se aplicó el uso de etiquetas para implementar versionado semántico y se comprobó la recuperación automática 
de imágenes desde la nube mediante Docker.

Este proceso facilita la distribución, administración y reutilización de imágenes en distintos entornos de trabajo.
