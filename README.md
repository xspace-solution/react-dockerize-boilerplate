# Dockerized React Application

## Docker Configuration with npx serve
### Build the Docker image for the current folder 
### and tag it with `dockerized-react`
docker build . -t dockerized-react

### Check the image was created
docker images | grep dockerized-react

### Run the image in detached mode 
### and map port 3000 inside the container with 3000 on current host
docker run -p 3000:3000 -d dockerized-react

## Docker Configuration with nginx
### See all running containers
docker ps

### Stop the previous container
### Copy "Name" or "Container ID" of your container
### and pass it into docker stop
docker stop <container name|id>

docker build . -t dockerized-react
### Notice we're now mapping port 80 inside the container 
### to port 3000 on the host machine!
docker run -p 3000:80 -d dockerized-react
