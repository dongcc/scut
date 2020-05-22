# lab3: build your container cluster

1. initalize the docker swarm
- docker swarm init

2. create a volume
- docker volume create --name lab3_data

3. check the volume that has been created
- docker volume ls

4. create the service which has 3 replicas
docker service create --replicas 3  --name lab3  -p 1880:1880 --mount type=volume,src=lab3_data,dst=/data lab2

5. check the service that has been created
- docker service ps

6. import the flows.json and deploy

7. delete and recreate the service:
- docker service rm lab3
- docker service create --replicas 3  --name lab3  -p 1880:1880 --mount type=volume,src=lab3_data,dst=/data lab2

8. try scaling the service to 5
- docker service scale lab3=5
- docker service ps
- docker ps