# Hemma Hubb

## Project Overview
Developing a smart home hub IoT system that monitors and controls security and safety sensors, together with indoor/outdoor climate monitoring. The system should be accessible both locally via a physical touch-display and remotely via a mobile app/web app.

**Included:**
**Sensors:** temperature, humidity, PIR motion detector, sound level sensor, particulate matter sensor
User interface: 1x3.2” TFT Touch Display
Backend/cloud system for data storage, API, and administration
Network configuration and security
Mobile app for remote monitoring and control

**Excluded** (for safety and privacy reasons):
- **No** integration with external apps or services like Google
- **No** microphone (no voice recording or voice recognition)
- **No** camera (no video monitoring)
- **No** third party data sharing


## Hardware Architecture

### Hardware Components
- Display: [3.2" Touch Display](https://www.amazon.se/dp/B07PKB691V/ref=sspa_dk_detail_1?pd_rd_i=B07PKB691V&pd_rd_w=TwqEg&content-id=amzn1.sym.952b25a7-f1aa-48f8-81f4-555c2c111a1c&pf_rd_p=952b25a7-f1aa-48f8-81f4-555c2c111a1c&pf_rd_r=3GGTRKJ2E0563R0MY15A&pd_rd_wg=iuttN&pd_rd_r=899f87bb-970c-43ec-af7e-41a963e74899&aref=jCyRA0eT9a&sp_csd=d2lkZ2V0TmFtZT1zcF9kZXRhaWw&th=1)


### Code
**lots and lots and lots of code**


- RFID Sensor: [Alternativ 1](https://amzn.eu/d/filleh1) [Alternativ 2](https://www.electrokit.com/rfid-modul-13.56mhz-med-2-taggar-rc522)

- **ESP32 - Microcontroller** (gateway)
- **Raspberry Pi Zero 2W** (node 1) 
- **Arduino Uno R4** (node 2)


**Components:**
- ILI9341 1x3.2” TFT Touch Display
- Temperature and humidity sensor DHT11
- Temperature sensor DS18B20
- PIR Motion Sensor 
- Buzzer (passive)
- Lights
- Reed Switch (door / window)
- Gas sensor MQ2
- Temp sensor NTC
- Rain Water sensor



### Software Components
- Embedded UI: LVGL
- Web UI: Figma
- Enviroment: platform.IO

### Network Configuration
- WiFi connection using MQTT and HTTP
- Security: WPA2/WP3 for WiFi
 

*Mermaid test:*
```mermaid

flowchart LR
  A[Start] --> B{Decision}
  B -->|Yes| C[Continue]
  B -->|No| D[Stop]
