# lab3: build your container cluster

- initalize the docker swarm
docker swarm init

- create a volume
docker volume create --name lab3_data

- check the volume that has been created
docker volume ls

- create the service which has 3 replicas
docker service create --replicas 3  --name lab3  -p 1880:1880 --mount type=volume,src=lab3_data,dst=/data lab2

- check the service that has been created
docker service ps

- import the flows.json and deploy

- delete and -recreate the service:
docker service rm lab3
docker service create --replicas 3  --name lab3  -p 1880:1880 --mount type=volume,src=lab3_data,dst=/data lab2

- try scaling the service to 5
docker service scale lab3=5
docker service ps
docker ps