### IoT-1887505

##### The project

This repository contains all the files and links needed for the creation of a Cloud-based IoT system that collects information from a set of virtual environmental sensors using the MQTT protocol. As a first part there are some clients written in node.js code that create random values to send to them to the **Thingsboard** cloud broker so we can show them in a web dashboard. Subsequently we will use the RIOT OS to create the clients in a MQTT-SN system, and since they cannot communicate to the cloud broker directly we need the PAHO transparent gateway.

## First assignment

##### Overview

The first assignments consist in creating the two devices Device1 and Device2 with node.js that create new values and send them to the Thingsboard broker.
First we need to create two devices in Thingsboard and get the access token that will be passed to the script. After the connection we specify a topic and the telemetry can start.
Then we need to create a web site that shows in table the data retrieved from the Thingsboard database so we can a have a clearer view on the values received.

##### Links

Below there are the links that bring you to the tutorial of the whole process as well as a short video of the implementation and the technology used.

[Youtube video link](https://www.youtube.com/watch?v=LOiYgVSLlrE&feature=youtu.be)

[LinkedIn article](https://www.linkedin.com/pulse/cloud-based-iot-system-collects-information-from-set-virtual-ferrara/?published=t)

## Second assignment

##### Overview

The second assignment consists of the continue of the first one, in fact instead of having the clients in node.js we will create them with the **RIOT** Operative System. They will communicate via MQTT-SN protocol through a transparent gateway in **PAHO** to the **MOSQUITTO** broker, so that we can finally store them in thingsboard.
So in order for every thing to work we will need to install all of these necessary programs. More details in the tutorial.
Then we will use the **IoT-Lab** testbed to test our main **RIOT OS** file on a real board stored in the IoT-lab in France. Doing this we can access real temperature values through the sensors of our chosen hardware, so that we can send them to our cloud broker and access them in the web dashboard.
Finally we will make some changes to the HTML file of the first assignment.

##### Links

Below there are the links that bring you to the tutorial of the whole process as well as a short video of the implementation and the technology used.

[Youtube video link]

[LinkedIn article]

### End
