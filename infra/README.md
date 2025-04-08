# EduVial – Infraestructura del Backend 🚦

Este proyecto define la infraestructura de la API de EduVial utilizando Docker. El backend está desarrollado con Node.js y Express, y se conecta a una base de datos PostgreSQL, todo orquestado con Docker Compose.

## Estructura del Proyecto

Primer-Sprint-Scrum-infraestructura/
 ├── backend/ 
 │ ├── index.js 
 │ ├── package.json 
 │ ├── Dockerfile 
 │ └── docker-compose.yml
 └── mock-app/

## Requisitos

- Tener [Docker](https://www.docker.com/) instalado.
- Tener [Docker Compose](https://docs.docker.com/compose/) instalado.
- Tener Git instalado para clonar el repositorio (opcional).
- Tener Node.js instalado (versión 14 o superior).

### Construir la imagen del backend
Desde la carpeta `backend`:
    ```bash
docker build -t eduvial-backend .

## Ejecutar el contenedor manualmente (sin PostgreSQL)
    docker run -p 3000:3000 eduvial-backend

## Orquestar backend y base de datos con Docker Compose
Desde la carpeta backend, ejecuta:
    docker-compose up

Esto levantará:
    El backend en Express (puerto 3000)
    Una base de datos PostgreSQL (puerto 5432)

## Detener y eliminar los contenedores
docker-compose down

## Limpiar volúmenes persistentes (útil si reinicias la base de datos)
docker-compose down -v

## Verificar que funciona
Abre tu navegador y entra a:
    http://localhost:3000/

