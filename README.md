# Secure API

A containerized FastAPI application built using Docker.

## Features

- FastAPI REST API
- Dockerized application
- Health Check Endpoint

## Endpoints

GET /

GET /health

## Run

docker build -t secure-api .

docker run -p 8000:8000 secure-api