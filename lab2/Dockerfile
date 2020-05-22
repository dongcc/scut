FROM nodered/node-red

# Copy package.json to the WORKDIR so npm builds all
# of your added modules for Node-RED
RUN npm install axios
RUN npm install node-red-node-watson

# Copy flow into the  image
#COPY flows.json /data/flows.json
