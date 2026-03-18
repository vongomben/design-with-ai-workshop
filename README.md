# design-with-ai-workshop
some side notes about a workshop I'm bringing around integrating sensecraft (as a startgin point, other tinyML tools on the long run) to Node-RED and Touch Designer

These are the side notes we are going to follow during the workshop.

In order to follow you have to have   
* a [Xiao ESP32S3 Sense](https://www.seeedstudio.com/XIAO-ESP32S3-Sense-p-5639.html) + USB cable
* an account on [Sensceraft AI](https://sensecraft.seeed.cc/ai/)
* [node-red installed on your PC](https://nodered.org/docs/getting-started/local)
* an MQTT broker locally installed, we are using [Aedes as a Node-RED node](https://flows.nodered.org/node/node-red-contrib-aedes)
* [OSC nodes installed in Node-RED](https://flows.nodered.org/node/node-red-contrib-osc)
* [Touch Designer](https://derivative.ca/) installed on your PC
* a local network, hence a Wifi router in my case

## Import Node-RED nodes

* Launch Node-RED 
* Install Aedes and OSC in your Node-RED 
* Import Design-with-AI-Flow-vers1.json in your Node-RED 
* Deploy 

![](https://github.com/vongomben/design-with-ai-workshop/blob/main/node-red.png?raw=true)

## Sensecraft

* create an Account 
* choose the classification model you want to deploy to the board (crosscheck if it's for your board) or create your model as I do in the video 
* configure MQTT with your IP address in your own network, and your SSID and Password and the IP of the broker.  
* copy the deviceId Sensecraft gave you tyo the Node-RED Flow, and edit the MQTT addresses with the correct one for you 
* deploy the model on the board 

You should be receiving things in Node-RED as you press "start" invoking data from the board. 

## TouchDesigner

* Import  osc-to-text.toe, you should see the command sent from Node-RED 

![](https://github.com/vongomben/design-with-ai-workshop/blob/main/touch-designer.png?raw=true)

Evviva!
