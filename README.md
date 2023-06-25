# Airflow Docker FOSS4G 2023 Kosovo


## Prerequisites
- Docker installed
- Docker Compose installed
- Permissions to execute Docker

## Steps to install
- Clone the repository in the desired location
```bash 
git clone https://github.com/Kan-T-IT/FOSS4G-2023-Airflow.git
```
- cd to it
- (if in linux) add the user id for docker to create the files in the volumes folder with the correct permission
```bash 
echo -e "AIRFLOW_UID=$(id -u)" >> .env
```
- Build the initial db and setup processes
```bash 
docker compose up airflow-init
```
- Run the application
```bash 
docker compose up
```

## Additional configuration
This compose, by default, sets the passwords contained in the .env file. To change them, modify this file.
Also, it serves the webserver in localhost:80
it can be edited in the ports section of the webserver (line 120 of docker-compose.yaml)