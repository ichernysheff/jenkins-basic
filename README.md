# Basic Jenkins in Docker

> [How to install WSL2](docs/wsl-installation.md)

> [How to install Docker](docs/docker-installation.md)

- Build Jenkins image

Plugins are installed at build time, the list of plugins to install is in the pluginst.txt file. 
Plugins can also be installed manually.

```
docker build -t jenkins-basic .
```

- Create volume

Volume saves jenkins state
```
docker volume create jenkins-basic
```

- Run Jenkins
```
docker run --name jenkins-basic --detach --rm --publish 8080:8080 --volume jenkins-basic:/home/jenkins/data/ jenkins-basic
```

Jenkins runned on _localhost:8080_

- Stop Jenkins
```
docker stop jenkins-basic
```
