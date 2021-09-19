# microservices

# Repository structure
[Dockerfile] - description of the image
[mongod.conf] - config prepared in advance for mongodb
[db_config] - contains variable with link to mongodb
[start.sh] - script for application execution

# Image build
docker build -t app:latest .

#Check the result
docker images -a

#Run a container
docker run --name app -d -p 127.0.0.1:9292:9292 app:latest

#Push our image to DockerHub
docker tag app:latest <your_dockerhub_account>/app:latest
docker push <your_dockerhub_account>/app:latest

