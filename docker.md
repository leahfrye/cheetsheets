# Helpful Docker Commands

### Creating a database dump from a Docker container

`docker exec CONTAINER-NAME mysqldump -u root --password=PASSWORD DATABASE-NAME > backup.sql`

### Restoring a databse to a Docker container

`cat backup.sql | docker exec -i CONTAINER-NAME mysql -u root --password=PASSWORD DATABASE-NAME`
