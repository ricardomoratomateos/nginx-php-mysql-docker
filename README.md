# How to execute it

```bash
$ docker-compose -up --build
$ docker-compose exec mysql sh /conf/mysql-setup.sh
```

And go to ` http://localhost:10000`

# Notes

* As the MySQL docker is the latest version (8.x), it can't connect by user and password, so the `mysql-setup.sh` change the way to do so to user and password again.

* If DBAL is the driver to connect to database, use a `.ini` file like this:
```ini
[database-config]
dbname = 'build'
user = 'root'
password = 'root'
host = 'mysql'
driver = 'pdo_mysql'
```

# TODO

* Not connect with root user.
* In PROD environment, remove the volumes of the docker.