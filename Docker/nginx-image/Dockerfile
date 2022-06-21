FROM nginx
COPY index.html /usr/share/nginx/html

# docker build -t stacksimplify/mynginx_image1:v1 .
# docker run --name mynginx1 -p 80:80 -d stacksimplify/mynginx_image1:v1

# =>
# docker build -t hambali999/mynginx_image1:v1 .

# Replace your docker hub account Id
# docker build -t <your-docker-hub-id>/mynginx_image1:v1 .
# docker run --name mynginx1 -p 80:80 -d <your-docker-hub-id>/mynginx_image1:v1

# =>
# docker run --name mynginx1 -p 80:80 -d hambali999/mynginx_image1:v1


# =>
# remove the dockers processes status
# docker ps -a
# docker rm $(docker ps -a -q)

# Step-4: Tag & push the Docker image to docker hub
# docker images
# docker tag hambali999/mynginx_image1:v1 hambali999/mynginx_image1:v1
# docker push hambali999/mynginx_image1:v1
