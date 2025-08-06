# IoT Node-RED MQTT

The project focuses on generating, publishing, receiving, processing, and logging MQTT messages, as well as visualizing temperature data and integrating with ThingSpeak.

---

## Project Overview
The flow simulates IoT data generation and processing using a local Mosquitto MQTT broker.  
It includes:
- Periodic message generation with random IDs and timestamps
- Publishing messages to an MQTT topic
- Subscribing to messages and processing based on specific conditions
- CSV logging of generated IDs, published temperature data, and ACK messages
- Filtering and validating payloads
- Temperature data plotting in Node-RED Dashboard
---

## ⚙️ Features
1. ID Generator – Generates random IDs and timestamps every 5 seconds.
2. CSV Logging – Saves ID logs (`id_log.csv`), filtered temperature data (`filtered_publish.csv`), and ACK logs (`ack_log.csv`).
3. Topic Subscription & Processing – Extracts N from ID (`N = ID % 7711`) and retrieves related CSV row.
4. Publish Message Builder – Builds MQTT messages based on CSV row data.
5. Temperature Plotting – Filters only Fahrenheit temperature messages and plots average values.

---

## Requirements
- [Node-RED](https://nodered.org/)
- [Mosquitto MQTT Broker](https://mosquitto.org/)
- ThingSpeak account (for data visualization)
- Node-RED Dashboard nodes
