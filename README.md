# Демо для курса по Docker

Сборка сервиса
```
docker build -t test -f apps/api/Dockerfile .
```# docker-demo


docker service create --name registry --publish 5000:5000 --constraint node.labels.registry==true --mount type=bind,source=/home/vagrant/registry,destination=/var/lib/registry -e REGISTRY_HTTP_ADDR=0.0.0.0:5000 registry:latest