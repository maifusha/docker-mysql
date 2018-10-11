> Docker image for MySQL

#### Badages
```
[![build status](https://git.yoursite.com/docker/mysql/badges/master/build.svg)](https://git.yoursite.com/docker/mysql/commits/master)
```

#### Quick Start
```bash
docker run -d --name=mysql_instance -e MYSQL_ROOT_PASSWORD=your_root_password -p 3306:3306 -v ./mysql_data:/var/lib/mysql --restart=always git.yoursite.com:5005/docker/mysql:latest
```

#### Account Config
```bash
# foouser => foo_password
docker exec -it mysql_instance bash

mysql -uroot -p

GRANT ALL ON *.* TO foouser@%         IDENTIFIED BY 'foo_password';
GRANT ALL ON *.* TO foouser@localhost IDENTIFIED BY 'foo_password';
```

#### Usefull ENV (Reference: `hub.docker.com/_/mysql/`)
* `MYSQL_ROOT_PASSWORD`：specify the root password
* `MYSQL_DATABASE`：specify the database which will auto created on container start
* `MYSQL_USER`：specify the user which will auto created on container start
* `MYSQL_PASSWORD`：specify the password of the auto created user
