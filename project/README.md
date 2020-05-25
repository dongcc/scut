Team Project: Building a chat robot for COVID19 status(an AI Assistant for COVID19)
- Application:
  - Front end, you can:
    - create a front chat ui, which will show the chatting history and a message box
    - you can use whatever language to create your UI or you can leverage the node-red dashboard(https://flows.nodered.org/node/node-red-dashboard)
  - Back end can do the following:
    - receive the text message from the UI
    - analyze the sentence to extract the intent(e.g. asking COVID19 or something else) and entity(e.g. location) and query the COVID19 service to generate a reply message
    - convert the reply message to the speech and play in within the front end UI
  - About the conversion handling:
    - use the Watson Assistant service(https://cloud.ibm.com/catalog/services/watson-assistant) to build a dialog flow, which can understand what the user asking
    - Watson Assistant tutorial: https://cloud.ibm.com/docs/assistant?topic=assistant-getting-started#getting-started-tutorial
  - About the COVID19 service:
    - https://flows.nodered.org/node/node-red-contrib-twc-covid19-tracker

Build container image for the front end and back end application.

Deploy the application into a k8s cluster(minikube or minishift or a real k8s cluster) or a Docker Swarm cluster.
- all the services need to have 2 + replicas

A reference:
https://developer.ibm.com/components/node-red/tutorials/create-a-voice-enabled-covid-19-chatbot-using-node-red/