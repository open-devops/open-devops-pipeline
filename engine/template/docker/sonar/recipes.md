# Run SonarQube with a PostgreSQL database

Use [docker-compose](https://github.com/docker/compose) to start the containers.

```bash
$ docker-compose up
```

Restart the containers (after plugin upgrade or install for example).

```bash
$ docker-compose restart sonarqube
```

Analyse a project:

```bash
mvn sonar:sonar \
  -Dsonar.host.url=http://ipaddress:9000 \
  -Dsonar.jdbc.url=jdbc:postgresql://ipaddress/sonar
```
