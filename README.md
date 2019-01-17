# docker-jenkins
[Jenkins](https://jenkins.io/) sobre [Docker](https://www.docker.com/). Se incluye la instalación de Maven y de plugins.

Para construir la imagen, ejecutar el siguiente comando:
```
$ docker-compose build
```

Para arrancar Jenkins, ejecutar el siguiente comando:
```
$ docker-compose up -d
```

Acceder a Jenkins con un navegador a http://localhost:8080

Para obtener la contraseña del usuario `admin` de Jenkins, ejecutar el siguiente comando:
```
$ docker exec -it dockerjenkins_master_1 cat /var/jenkins_home/secrets/initialAdminPassword
```

Para bajar la imagen desde docker hub
```
$ docker pull jcvaldes/jenkins-maven
```
Para crear el docker
```
$ docker run --name dockerjenkins_master_1 -p 8080:8080 -p 50000:50000 -v /var/jenkins_home jcvaldes/jenkins-maven
```
---

Tags: devops, docker, jenkins, maven