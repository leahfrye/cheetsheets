# Helpful Docker Commands

### Creating a database dump from a Docker container

`docker exec CONTAINER-NAME mysqldump -u root --password=PASSWORD DATABASE-NAME > backup.sql`

### Restoring a databse to a Docker container

`cat backup.sql | docker exec -i CONTAINER-NAME mysql -u root --password=PASSWORD DATABASE-NAME`

### Access a docker container's files
`docker exec -it CONTAINER_ID bash`

### Run docker-compose, but using a specific docker-compose file
`docker-compose -f DOCKER_COMPOSE_FILE_NAME up`
Can also be build, run, down, etc.
