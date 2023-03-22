## Instructions

To run this code, follow these steps:

1. Creaete a Docker netowork using the following command:

docker network create my-network

2. Run the MySQL Docker image with the name "db" and root password of "my-secret-password" using the following command:

docker run -d --name db --network my-network -e MYSQL_ROOT_PASSWORD=my-secret-password mysql:latest

3. Run the phpMyAdmin Docker image on the network previously created, mapping a port of your choice (e.g. 8080) to port 80 of the container using the following command:

docker run -d --name phpmyadmin --network my-network -p 8080:80 phpmyadmin/phpmyadmin

Note: Replace "8080" with the port of your choice.