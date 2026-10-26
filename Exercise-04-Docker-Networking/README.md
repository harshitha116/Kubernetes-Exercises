
# Exercise 4: Docker Networking

## Objective
Understand Docker bridge networking and communication between containers.

## Files
- app.py
- requirements.txt
- Dockerfile

## Commands Used
```powershell
docker build --no-cache -t flask-api .\Exercise-04-Docker-Networking
docker network create --driver bridge my-bridge-net
docker run -d --name mysql --network my-bridge-net -e MYSQL_ROOT_PASSWORD=LabPass123! mysql:latest
docker run -d --name redis --network my-bridge-net redis:latest
docker run -d --name flask --network my-bridge-net -p 5001:5001 flask-api
docker ps
```

## Result
The Flask REST API was successfully accessed at /about.
MySQL, Redis, and Flask were configured on a shared Docker bridge network.
