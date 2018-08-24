# test

Difference between an image and a container. An image is the binaries and libraries and source code that all make up your application. 
The container is a running instance of that image.


===================== Docker Commands =================
docker version 
docker info
docker pull httpd

docker container run --publish 80:80 --name ggarg_container_name nginx 
docker container run --publish 80:80 --detach --name ggarg_container_name nginx (run the image in the detched mode)
docker container ls (list all the containers)
docker container stop <<CONTAINTER_ID>> (to stop a container)
docker container ls -a (displaying stopped containers)
docker container rm id_1 id_2 (removing stopped IDs)
docker run --name ggargmysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql
docker container logs <<container_name/container_id>>


