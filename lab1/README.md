# Lab1: running your first docker container
1. run a container on port 1880:
- docker run -it -p 1880:1880 --name 1stnodered nodered/node-red

2. import and deploy the flow: lab1.json

3. try out via: http://localhost:1880/talk

4. issue command to check container status via docker ps in a sparate window

5. try the docker start/stop/logs/inspect/rm/rmi commands

6. run another cantainer on port 1881:
- docker run -it -p 1881:1880 --name 2ndnodered nodered/node-red
- check is the flow has been deployed still being there? why? how to archieve that? 