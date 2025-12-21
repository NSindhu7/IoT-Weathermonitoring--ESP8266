# IoT Weather Monitoring System using ESP8266

## 📌 Project Overview
This project is an IoT-based Weather Monitoring System developed using **NodeMCU (ESP8266)** and the **Blynk IoT platform**.  
It monitors real-time environmental parameters and displays them remotely on a mobile dashboard.

---

## 🔧 Hardware Components
- NodeMCU ESP8266
- DHT11 Temperature & Humidity Sensor
- BMP085 Pressure Sensor
- Rain Sensor
- LDR (Light Dependent Resistor)
- Servo Motor
- 2 LEDs (Temperature & Pressure indication)
- Breadboard & Jumper Wires

---

## ⚙️ Software & Tools
- Arduino IDE
- Blynk IoT App
- ESP8266 Board Package
- GitHub

---

## 📚 Required Libraries (Arduino IDE)

Install the following libraries from **Arduino IDE → Library Manager**:

1. **Blynk** (by Volodymyr Shymanskyy)
2. **Adafruit BMP085 Unified**
3. **Adafruit Unified Sensor**
4. **DHT sensor library**
5. **ESP8266WiFi** *(comes with ESP8266 package)*
6. **Servo** *(built-in)*

> Make sure all libraries are successfully installed before uploading the code.

---

## 🔌 ESP8266 Board Setup
1. Open **Arduino IDE**
2. Go to **File → Preferences**
3. Add this URL in *Additional Board Manager URLs*:
https://arduino.esp8266.com/stable/package_esp8266com_index.json
4. Go to **Tools → Board → Boards Manager**
5. Install **esp8266 by ESP8266 Community**
6. Select:
- Board: **NodeMCU 1.0 (ESP-12E Module)**
- Upload Speed: **115200**

---

## 📱 Blynk IoT Setup (Important)

### Step 1: Create Template
- Platform: **Blynk IoT**
- Hardware: **ESP8266**
- Connection Type: **WiFi**

### Step 2: Note Credentials
Copy and paste these into your code:
```cpp
#define BLYNK_TEMPLATE_ID "TMPLxxxx"
#define BLYNK_TEMPLATE_NAME "smart weather forecast"
#define BLYNK_AUTH_TOKEN "Your_Auth_Token"

### **Step 3: Create Datastreams**
Add these Virtual Pin Datastreams in the Blynk template:

Datastream	Virtual Pin
Temperature	V0
Humidity	V1
Pressure	V2
Rain Sensor	V3
LDR Status	V4

### **Step 4: Mobile Dashboard**

1. Open **Blynk Mobile App**
2. Add widgets (Gauge / Value Display)
3. Assign widgets to:
   - **V0** → Temperature (°C)
   - **V1** → Humidity (%)
   - **V2** → Pressure (hPa)
   - **V3** → Rain Value
   - **V4** → LDR Status (0/1)

---

## ▶️ Running the Project

1. Open `weather.ino`
2. Update **WiFi credentials** and **Blynk credentials**
3. Upload the code to **NodeMCU ESP8266**
4. Select the correct **COM Port**
5. Open **Serial Monitor** (115200 baud)
6. View live sensor data on the **Blynk App**

---

## 🌦️ Project Features

- Real-time temperature and humidity monitoring  
- Atmospheric pressure monitoring  
- Rain detection with servo motor control  
- Day/Night detection using LDR  
- LED alerts for threshold conditions  
- Remote monitoring using **Blynk IoT**

---

## 🔌 Circuit Diagram

The circuit diagram is available in the `images/` folder.

---

## 👤 Author

**Naseeb Sindhu**  
B.Tech – Electronics & Communication Engineering
