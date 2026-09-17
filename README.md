# AlertAway   
A lightweight ho# 🔔 AlertAway
### A lightweight edge-server home automation system designed to run on low-end Linux computers.

[License: MIT](./LICENSE)

**AlertAway** is best described as a *System of Systems*, gluing together existing open-source projects into a simplified interface. It functions as an edge-server designed to deploy on low-end Linux single-board computers (SBCs). 

Originally written in Perl, AlertAway is currently a work in progress as it undergoes a complete architectural redesign and conversion to **Python 3**.

* **Project Homepage:** [alertaway.com](http://alertaway.com)
* **Source Code:** [MQTT-home/linux/alertaway](https://github.com/jdodgen/MQTT-home/tree/main/linux/alertaway)

---

## 🛠️ Core Services

AlertAway handles the heavy lifting of gathering distributed devices into a singular, clean environment:

* **Unified Device Management:** Collects IP and ZigBee devices into a single interface.
* **Lightweight HTTP Servers:** Built-in web endpoints to maintain and map Fauxmo, Philips Hue, and ZigBee devices.
* **Device Discovery & Mapping:** Allows automatic and manual entry of custom IP devices.
* **Rich Notifications:** Maps MQTT messages to outgoing emails, with support for attaching optional IP camera JPEG captures.
* **Cross-Device Triggers:** Coordinates device-to-device automation (e.g., a sensor trigger causing an action on a separate target device).
* **Broker Flexibility:** Works seamlessly with both local and cloud-hosted MQTT Brokers.
* **Zero-Config Deployment:** Explicitly designed to require **NO user configuration** once a compiled SD card image is built.

---

## 🔌 Supported Protocols & Devices

* **MQTT** – An efficient, lightweight messaging protocol optimized for IoT devices.
* **ZigBee HA** – Home Automation mesh networks.
* **IP / WiFi** – Standard local network home automation equipment.
* **WeMo Emulation** – Built-in legacy support.
* **Philips Hue Emulation** – Integrated lighting control *(TBD)*.

---

## 🤝 Open Source Ecosystem

AlertAway stands on the shoulders of these excellent open-source projects:

* [Eclipse Mosquitto](https://mosquitto.org/) – MQTT Broker
* [zigbee2mqtt](https://github.com/Koenkk/zigbee2mqtt) – ZigBee to MQTT bridge
* [fauxmo](https://github.com/n8henrie/fauxmo) – Lightweight Amazon Alexa emulation
* [DiyHue](https://diyhue.org/) – Philips Hue ecosystem emulation
* **Core Stack:** Python 3, SQLite 3, and structured SQL.

---

## 💻 Hardware Requirements

AlertAway is highly optimized to run on virtually any small single-board computer (SBC) capable of hosting Linux.

* **Network:** An RJ45/Ethernet port for a reliable, hardwired connection directly to your home router.
* **USB:** At least one available USB port to host a [compatible ZigBee adapter/dongle](https://www.zigbee2mqtt.io/guide/adapters/).

### Current Development Reference Stack
* **OS:** Raspbian Linux
* **SBC:** AML-S905X-CC (Le Potato) — *chosen for its excellent availability over the Raspberry Pi 3*
* **Hardware Bridge:** SONOFF Zigbee 3.0 USB Dongle Plus — *highly reliable and budget-friendly*

---

## 🕰️ Project History

The project was originally started in **2011** and written entirely in **Perl**. The inspiration came after a friend suffered severe property damage from an undetected water leak while they were away from home. 

In its earliest iterations, the system relied heavily on Digi XBee radios. Over time, the architecture shifted toward standardized ZigBee HA hardware, and the legacy XBee radios have since been completely phased out.

---

## 📄 License & Copyright

Copyright (c) 2011-2026 jdodgen.

This project is open-source software licensed under the terms of the **MIT License**. See the repository's `LICENSE` file for full details.
me automation system designed to run on low end Linux Computers
It it built on MQTT. It is composed of timers" like for a security light, triggers: where one device causes action on another device, emailer: where events cause emails with jpgs, and voice commands through smart speakers)
It is Edge server system desighed to run on low end Linux SBCs
It is best described as a System of Systems, gluing together other open source projects 
Code lives here: [MQTT-home/linux/alertaway](https://github.com/jdodgen/MQTT-home/tree/main/linux/alertaway)
It is currently a work in progress during converson from a older system.
It has a domain alertaway.com that displays this content.

### Features:
- MQTT - A IBM designed messaging system for devices
- WeMo emulation- legacy
- Phillips Hue emulation (TBD)
- ZigBee HA Home Automation Devices
- IP/WiFi home automation devices
    
### It uses these and other open source projects:
- [fauxmo](https://github.com/n8henrie/fauxmo)
- [zigbee2mqtt](https://github.com/Koenkk/zigbee2mqtt)
- [DiyHue](https://diyhue.org/)
- [Eclipse Mosquitto](https://mosquitto.org/)
- And of course lots of tools like python3, sqlite3

### AlertAway provides the following services: 
- Collecting IP and ZigBee devices into a simplified interface
- Lightweight HTTP servers for:
  - maintain/map fauxmo/Hue  devices
  - Uses zigbee2mqtt to maintain zigbee devices
  - Allow automatic and manual entry of custom IP devices
  - Map MQTT messages to emails with optional IP camera pictures
  - Trigger devices from other devices
- Uses a local or cloud MQTT Brokers
- Written in Python3 with some SQL<br>
- Designed to require NO user configuration after a SD image is built. 

## Hardware requirements 
Simple SBC pretty much anything that can run Linux.      
Must have both a RJ45 to connect to the home router,    
Also a USB port for the zigbee2mqtt compatable [zigbee dongle](https://www.zigbee2mqtt.io/guide/adapters/)

## Current development system:
- Raspbian linux<br>
- AML-S905X-CC (Le Potato) SBC (because RPI 3's were unavailble)
- SONOFF Zigbee 3.0 USB Dongle (compatable and cheap)


It is best described as a System of Systems, gluing together other open source projects.    
Code lives here: [github](https://github.com/jdodgen/MQTT-home/tree/main/linux/alertaway)   
### Features:
- MQTT - A IBM designed messaging system for devices
- WeMo emulation- legacy
- Phillips Hue emulation
- ZigBee HA Home Automation Devices
- IP/WiFi MQTT home automation devices
    
### It uses these and other open source projects:
- [fauxmo](https://github.com/n8henrie/fauxmo)
- [mqtt](https://github.com/eclipse/mosquitto)
- [zigbee2mqtt](https://github.com/Koenkk/zigbee2mqtt)
- [DiyHue](https://diyhue.org/)
- And of course lots of tools like python3, sqlite3

### AlertAway provides the following services: 
- Collecting IP and ZigBee devices into a simplified interface
- Lightweight HTTP servers for:
  - maintain/map fauxmo/Hue  devices
  - Uses zigbee2mqtt to maintain zigbee devices
  - Allow automatic and manual entry of custom IP devices
  - Map MQTT messages to emails with optional IP camera pictures
  - Trigger devices from other devices
- Uses a local or cloud MQTT Brokers
- Written in Python3 with some SQL<br>
- Designed to require NO user configuration after a SD image is built. 

## Hardware requirements 
small SBC, pretty much anything that can run Linux.    
A RJ45/Ethernet port to connect to the home router,        
Also a USB port for the zigbee2mqtt compatable [zigbee dongle](https://www.zigbee2mqtt.io/guide/adapters/)

## Current development system:
- Raspbian linux<br>
- AML-S905X-CC (Le Potato) SBC (because RPI 3's were unavailble)
- SONOFF Zigbee 3.0 USB Dongle (compatable and cheap)

### History:
<pre>
The Project was started in 2011. Originaly written in Perl. 
I started it after a friend had some damage from a water leak when they were away.
At first it used Digi XBee's and later some ZigBee HA devices.
XBee's are all gone now.  
</pre>
