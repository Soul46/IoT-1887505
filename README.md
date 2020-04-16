### IoT-1887505

Andrea Gaetano Ferrara mat.1887505

Repository work and structure
```
├── Device1.js                      #1st device in node.js for the first assignment
│   
├── Device2.js                      #2nd device in node.js for the first assignment
│   
│── ferrara_1887505                 #folder for the web page
│   │
│   ├── web1.html
│   ├── README.md
│   └── web
│       |
|       ├── css.css
|       └── foto.jpg
│
│   
├── Gateway                         #Gateway configuration and execution file for the second assignment
│   │   
│   ├── MQTT-SNGateway
|   └── gateway.conf
│      
├── MOSQUITTO_Bridge                #Configuration file for the mosquitto bridge of the 2nd assignment
│       |
|       └── mosquitto_bridge.conf
|
└── Devices                         #Folder containing Riot OS devices for assignment 2 and 3
│       |
|       ├── LoRaWAN_Nodes           #Folder containing devices for the 3rd assignment that generate random values, LoRaWAN
|       |      ├── Device1
|       |      |    ├── Makefile
|       |      |    ├── Makefile.tests_common
|       |      |    ├── README.md
|       |      |    └── main.c
|       |      └── Device2
|       |           ├── Makefile
|       |           ├── Makefile.tests_common
|       |           ├── README.md
|       |           └── main.c
|       ├── LoRaWAN_Sensors         #Folder containing devices for the 3rd assignment that access real values, LoRaWAN
|       |      ├── Device1
|       |      |    ├── Makefile
|       |      |    ├── Makefile.tests_common
|       |      |    ├── README.md
|       |      |    └── main.c
|       |      └── Device2
|       |           ├── Makefile
|       |           ├── Makefile.tests_common
|       |           ├── README.md
|       |           └── main.c
|       ├── RIOT_OS_Client_1        #Folder containing device 1 for the 2nd assignment that generate random values, MQTT-SN
|       |    ├── Makefile
|       |    ├── README.md
|       |    └── main.c
|       ├── RIOT_OS_Client_2        #Folder containing device 2 for the 2rd assignment that generate random values, MQTT-SN
|       |    ├── Makefile
|       |    ├── README.md
|       |    └── main.c
|       |
|       └── RIOT_OS_REAL_BOARD      #Folder containing devices for the 2rd assignment that access real values, MQTT-SN
|            ├── Makefile
|            ├── README.md
|            └── main.c

```

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

[Youtube video link](https://www.youtube.com/watch?v=CBi96h9ubBE)

[LinkedIn article](https://www.linkedin.com/pulse/emulate-virtual-environmental-sensors-riot-os-publish-ferrara/?published=t)

## Third assignment

In the third assignment we were asked to create new devices with Riot OS that will be flashed in the **LoRaWAN kit** boards in IoT-Lab.
We created two different devices that create random values for temperature, humidity, wind direction, wind intensity and rain height and two other devices that will access the board's hts221 sensor to get the temperature and humidity of the real hardware.
Both devices will then send via semtech_loramac_send the obtained values to the respective devices created in **TheThingsNetwork**, after that, through integration in Thingsboard, we will be able to create devices in our cloud broker so that we can get the values to show them in our web-dashboard.

##### Links

[Youtube video link](https://www.youtube.com/watch?v=4waQTOxwi6g&feature=youtu.be)

[LinkedIn article](https://www.linkedin.com/pulse/creating-sensor-network-using-virutal-real-devices-via-ferrara/?published=t&trackingId=CZ3nHzb0QoMQ4wDm898lVQ%3D%3D)

## Acknowledgments

This reposiotry is part of several assignments from the IoT course held at Sapienza University of during the academic year 2019-2020.

### End
