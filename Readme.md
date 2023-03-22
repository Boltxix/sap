## Installation

1. Install Docker by following the instructions in the [official documentation](https://docs.docker.com/get-docker/).
2. Clone the repository and navigate to the project directory.
3. Run the following command to create a Docker network:
	```sql
	docker network create my-network
	```
4. Run the following command to start a MySQL Docker container:
	```sql
	docker run -d --name db -e MYSQL_ROOT_PASSWORD=my-secret-password mysql:latest
	```
5. Run the following command to start a phpMyAdmin Docker container:
	```sql
	docker run -d --name phpmyadmin -p 8080:80 --network my-network phpmyadmin/phpmyadmin
	```
6.  Access phpMyAdmin by opening a web browser and navigating to `http://localhost:8080`. Log in using the MySQL root username and password.
