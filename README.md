<h1>Weather Monitoring and Reporting System</h1>
<br>
<br>

<h3> Overview </h3>
This repository contains the code and documentation for a comprehensive Weather Monitoring and Reporting System. The system uses a NodeMCU (ESP8266) to collect environmental data from various sensors, stores the data on Anedya IoT Cloud, and visualizes it in real-time using a Streamlit dashboard.

<b> Features </b>
<b>Real-time Monitoring:</b> Measures temperature, humidity, UV index, atmospheric pressure, and soil moisture levels.
<b>Cloud Storage:</b> Stores data on Anedya IoT Cloud for remote access and long-term storage.
<b>Interactive Dashboard:</b> Visualizes data using a Streamlit-based web application.
<b>Local Display:</b> Displays real-time sensor data on a 0.96-inch OLED display.
<br>
<br>
<br>
<b>Components </b>
NodeMCU (ESP8266)
DHT22 Sensor (Temperature and Humidity)
GUVA-S12SD UV Sensor
BMP180 Sensor (Pressure)
Soil Moisture Sensor
CD4051 IC Multiplexer
0.96-inch OLED Display
<br>
<br>

<b> Setup Instructions </b>
<br>
Hardware Connections
DHT22 Sensor:

VCC to 3.3V
GND to GND
Data to GPIO D5
<br>
GUVA-S12SD UV Sensor:

VCC to 3.3V
GND to GND
Signal to CD4051 multiplexer input <br>

BMP180 Sensor:
VCC to 3.3V
GND to GND
SDA to GPIO D2
SCL to GPIO D1
<br>
Soil Moisture Sensor:
VCC to 3.3V
GND to GND
Signal to CD4051 multiplexer input
<br>
CD4051 IC Multiplexer:
Connect signal inputs from analog sensors
Control pins to GPIO pins on NodeMCU
Output to A0 (analog input pin) on NodeMCU
<br>
0.96-inch OLED Display:
VCC to 3.3V
GND to GND
SDA to GPIO D2
SCL to GPIO D1
<br>
<br>


<b> Install Required Libraries </b>

DHT.h
Adafruit_Sensor.h
Adafruit_BMP085.h
ESP8266WiFi.h
ESP8266HTTPClient.h
Adafruit_GFX.h
Adafruit_SSD1306.h


<br>
<br>
<b> Upload Code to NodeMCU </b>

<p>Open the weather_monitoring.ino file in the Arduino IDE. Configure your WiFi credentials and Anedya IoT Cloud API endpoint in the code. Then upload the code to your NodeMCU. this file is avalable in Firmware folder.</p>
<br>

<b> Set Up Anedya IoT Cloud </b>
Create an account on Anedya IoT Cloud.<br>
Set up a new project and configure the endpoints for data reception.<br>

<br>
<b>Install Streamlit and Run Dashboard </b>
<p>
 Ensure you have Python and pip installed. Then install Streamlit and run the dashboard.
</p>

pip install streamlit <br>

streamlit run dashboard.py <br> 

The dashboard.py script should be located in the root directory of the cloned repository.

<br>
<br>

<b>Contributing </b> <br>

Contributions are welcome! Please fork the repository and submit a pull request.
 

