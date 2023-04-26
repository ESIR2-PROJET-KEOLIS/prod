# Docker Compose Production

This is a production ready docker-compose setup for the application.


Every time the main branch of a module is updated, the docker image is rebuilt and pushed to the docker hub.

## How to use

1. Clone the repository
2. Run `docker-compose up` to start the application
3. Connect to the application on `http://localhost/`

## How to host

On the host machine :

1. Clone the repository
2. Run `docker-compose up` to start the application
3. Open host machine's port 80 to the internet
4. Connect to the application on `http://<host-ip>/`