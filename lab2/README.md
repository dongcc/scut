# lab2: building your own text to speech container image

1. building the watson text to speech node into the node-red which requires the following packages,  write a Dockerfile to build a new image 'lab2', which will includes the those packages:
   - npm install axios
   - npm install node-red-node-watson
  
2. start lab2 container to make sure the text to speech nodes have been installed.

3. import the flow via loading the flows.json.

4. login into the ibmcloud.com(register an IBM id if does not have one), and create Text to Speech service from the catalog.

5. in the nodered, update the apikey from in the text to speech node of the flow that imported previously.

6. try out via the http://localhost:1880/talk

7. starting 2 container on different ports to sharing the same flow, investigate how to make the 2 or more containers to share the same flow.
