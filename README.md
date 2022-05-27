# Working with Microservices in Go (Golang)

Ref: https://www.udemy.com/course/working-with-microservices-in-go

## gRPC

```
$ protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative logs.proto
```

## Docker Swarm

```
$ docker swarm init
$ docker swarm ps
$ docker stack deploy -c swarm.yml myapp
$ docker service ls
$ docker service scale myapp_listener-service=3
$ docker service scale myapp_listener-service=2
$ docker service update --image paisit04/logger-service:1.0.1 myapp_logger-service
$ docker service scale myapp_broker-service=0
$ docker stack rm myapp
$ docker swarm leave --force
```
