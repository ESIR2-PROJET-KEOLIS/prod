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
2. Build the frontend image with the good environnement variable setup.
> The environnement variables are processed at build time, so you need to rebuild the image to change them. By default, the frontend is connected to the backend in localhost. It means if you want to host the app. You must configure "URLBACK" and "URLWS" by "http://<host-ip>:3500" and "ws://<host-ip>:4000"
> 
> A possible way to do that is to edit the GitHub action workflow to build the frontend image with the good environnement variables. See the make envfile step in the workflow : "docker-img-publish.yml"
2. In docker compose, replace frontend image by your custom image.
3. Run `docker-compose up` to start the application
4. Open host machine's port 80 to the internet
5. Connect to the application on `http://<host-ip>/`