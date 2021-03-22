# Q5

Q5) Create a block diagram and explain how you will achieve monitoring the co2 level in a room using the circuitry of ur choice. Upon exceeding a certain threshold the solution should send a msg to the cloud. Here you can use http://www.hivemq.com/demos/websocket-client/ to publish the alarm data, the host is broker.mqttdashboard.com. You can assume that you are using
esp32/esp8266 as your base board. Share the code snippets for the same.
(https://user-images.githubusercontent.com/81143882/111952388-18afaf00-8b0b-11eb-8ef8-d7a951d8564d.png)








#include “wifi.h”
#include “ESPA syncWebServer.h” 
#include “DHTesp.h”
#include “SoftwareSerial.h”
#include “MHZ19”
#define RX_PIN33
#define TX_PIN32
Int dhtPin=4;
DHTesp dht;
MHZ19 myMHZ19;
SoftwareSerial mySerial(RX_PIN,TX_PIN);
AsyncWebServer Server(80);
Const char*ssid= “network name”;
Const char*Password=”Password”;
Serial.begin(115200);
Wifi.begin(ssid,password);
Server.on(“/C02”,HTTP.GET,[]);
(AsynWeb serverRequest*request));
