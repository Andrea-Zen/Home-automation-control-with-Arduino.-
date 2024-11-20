Features
Temperature and Humidity Monitoring: Uses a DHT22 sensor to measure and display values.
Air Quality Detection: Monitors air quality using an MQ-135 gas sensor and sends email alerts if levels exceed a threshold.
Light Level Monitoring: Uses an LDR to measure ambient light.
Burglar Alarm: Detects motion using a PIR sensor and sends an email alert when triggered.
Relay Control: Two relays can be turned on/off manually or scheduled for specific times.
Event Log: Maintains a log of activities and events.
Web Interface: Provides a real-time dashboard for sensor readings, relay control, and logs.
Components Required
Arduino Uno or compatible board
ESP8266 Wi-Fi Module
DHT22 Sensor (for temperature and humidity)
MQ-135 Gas Sensor
PIR Motion Sensor
LDR (Light Dependent Resistor)
2 Relay Modules
RTC Module (Real-Time Clock)
Resistors, jumper wires, breadboard
How It Works
Wi-Fi Connection: Connects to a Wi-Fi network and hosts a web server to provide a control interface.
Sensor Data: Collects data from sensors (temperature, humidity, air quality, light, and motion).
Relay Control: Allows manual and scheduled control of relays for devices like lights or fans.
Email Notifications: Sends email alerts for air quality and motion detection events.
Historical Data: Stores the last 10 readings of temperature, humidity, and air quality for display on a web interface.
Event Logging: Logs up to 100 events, such as relay activations or motion detections.
Setting Up the Code
Libraries to Install:

DHT.h (for temperature and humidity)
MQ135.h (for gas sensor)
RTClib.h (for RTC module)
ESP8266WiFi.h (for Wi-Fi connectivity)
SMTPClient.h (for email notifications)
ArduinoJson.h (for JSON parsing)
Wi-Fi Configuration:
Replace the placeholders YOUR_SSID and YOUR_PASSWORD in the code with your Wi-Fi credentials.

Email Setup:
Replace emailRecipient and emailPassword with your email address and password for sending alerts.

Hardware Connections:

Connect the sensors and relays to the specified pins in the code.
Ensure proper power supply for the ESP8266 module.
Web Interface
Access the web interface by entering the ESP8266’s IP address in a browser.
Features:
View real-time sensor readings (temperature, humidity, air quality, and light levels).
Control relays (turn on/off or schedule).
View historical graphs for temperature and air quality.
View and clear the event log.
Email Alerts
Air Quality: If the air quality exceeds the threshold (300 PPM), an email alert is sent.
Motion Detection: If the PIR sensor detects motion, an email alert is sent immediately.
Future Improvements
Add a smartphone app for remote control.
Expand relay control to more devices.
Integrate voice commands using a virtual assistant (e.g., Alexa, Google Assistant).
