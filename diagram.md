```mermaid

graph
    User[USER - Physical hub] -->|Uses| Hub
    UserRemote[USER - Remote / Web-interface] -->|Uses| Hub

    subgraph Hub [Smart Hub]
        Sensors[SENSORS: Temp, Humidity, PIR]
        Interface[INTERFACE: Joystick / display + Web-interface]
        Comminucation[COMMINUCATION: WiFi, MQTT/HTTP]
    end

   subgraph Backend [Backend / cloud]
        Temp[API]
        Hum[Store data]
        PIR[Log]
    end

    Hub --> |Send data| Backend
    Backend --> Remote_app
    Backend --> admin

   subgraph Remote_app [Web interface]
    end

   subgraph admin [Support / Admin]
    end