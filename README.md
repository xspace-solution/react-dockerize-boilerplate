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