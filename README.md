# test

-> Difference between an image and a container. An image is the binaries and libraries and source code that all make up your application. 
The container is a running instance of that image.

-> When you actually start a container, you're really in the background connecting to a particular Docker network. 
By default "bridge" network.

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
docker container run  -ti  --name proxy nginx bash (interactive - running a new container)
docker container exec  -ti   <<CONATINER_NAME>> bash (interactive - already running container)

docker network ls  (show networks)
docker network inspect <<network_name>> (inspect a network)
docker network create <<network_name>> (Create a network)
docker network connect (attach a newtork to container)
docker network disconnect (detach from contaienr)
docker container run --publish 80:80 --detach --name ggarg_container_name --network <<network_name>> nginx (run the image in the detched mode)


docker run -p 8080:8080 -p 50000:50000 jenkins
docker container run --publish 80:8080 --name ggarg_jenkins jenkins --detach

