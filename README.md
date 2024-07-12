<h1>Weather Monitoring and Reporting System</h1>
<br>
<br>

<h3> Overview </h3>
This repository contains the code and documentation for a comprehensive Weather Monitoring and Reporting System. The system uses a NodeMCU (ESP8266) to collect environmental data from various sensors, stores the data on Anedya IoT Cloud, and visualizes it in real-time using a Streamlit dashboard.

<b> Features </b>
<b>Real-time Monitoring:</b> Measures temperature, humidity, UV index, atmospheric pressure, and soil moisture levels. <br>
<b>Cloud Storage:</b> Stores data on Anedya IoT Cloud for remote access and long-term storage. <br>
<b>Interactive Dashboard:</b> Visualizes data using a Streamlit-based web application. <br>
<b>Local Display:</b> Displays real-time sensor data on a 0.96-inch OLED display. <br>
<br>
<br>
<br>
<b>Components </b> <br>
NodeMCU (ESP8266) <br>
DHT22 Sensor (Temperature and Humidity) <br>
GUVA-S12SD UV Sensor <br>
BMP180 Sensor (Pressure) <br>
Soil Moisture Sensor <br>
CD4051 IC Multiplexer <br>
0.96-inch OLED Display 
<br>
<br>

<b> Setup Instructions </b>
<br>
Hardware Connections <br>
DHT22 Sensor: <br>

VCC to +5V <br>
GND to GND <br>
Data to GPIO D5 <br>
<br>
GUVA-S12SD UV Sensor:<br>

VCC to +5V  <br>
GND to GND <br>
Signal to CD4051 multiplexer input <br> 

BMP180 Sensor: <br>
VCC to +5V  <br>
GND to GND <br>
SDA to GPIO D2 <br>
SCL to GPIO D1 <br>
<br>
Soil Moisture Sensor: <br>
VCC to +5V  <br>
GND to GND <br>
Signal to CD4051 multiplexer input <br>
<br>
CD4051 IC Multiplexer: <br>
Connect signal inputs from analog sensors <br>
Control pins to GPIO pins on NodeMCU <br>
Output to A0 (analog input pin) on NodeMCU <br>
<br>
0.96-inch OLED Display: <br>
VCC to +5V  <br>
GND to GND <br>
SDA to GPIO D2 <br>
SCL to GPIO D1 <br>
<br>
<br>


<b> Install Required Libraries </b> <br>

DHT.h <br>
Adafruit_Sensor.h <br>
Adafruit_BMP085.h <br>
ESP8266WiFi.h <br>
ESP8266HTTPClient.h <br>
Adafruit_GFX.h <br>
Adafruit_SSD1306.h <br>


<br>
<br>
<b> Upload Code to NodeMCU </b> <br>

<p>Open the weather_monitoring.ino file in the Arduino IDE. Configure your WiFi credentials and Anedya IoT Cloud API endpoint in the code. Then upload the code to your NodeMCU. this file is avalable in Firmware folder.</p> <br>
<br>
 
<b> Set Up Anedya IoT Cloud </b> <br>
Create an account on Anedya IoT Cloud.<br>
Set up a new project and configure the endpoints for data reception.<br>

<br>
<b>Install Streamlit and Run Dashboard </b> <br>
<p>
 Ensure you have Python and pip installed. Then install Streamlit and run the dashboard.
</p> <br>

pip install streamlit <br>

streamlit run dashboard.py <br> 

The dashboard.py script should be located in the root directory of the cloned repository. <br>

<br>
<br>

<b>Contributing </b> <br>

Contributions are welcome! Please fork the repository and submit a pull request.
 

