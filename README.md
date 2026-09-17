# AlertAway
### A lightweight edge-server home automation system designed to run on low-end Linux computers.

<p align="center">
  <img src="https://github.com/jdodgen/AlertAway/blob/main/aa_logo.jpg?raw=true" alt="AlertAway Logo" width="300" height="300">
</p>

**AlertAway** is best described as a *System of Systems*, gluing together existing open-source projects into a simplified interface. It functions as an edge-server designed to deploy efficiently on low-end Linux single-board computers (SBCs). 

Originally written in Perl, AlertAway is currently a work in progress as it undergoes a complete architectural redesign and conversion to **Python 3**.

* **Project Homepage:** [alertaway.com](http://alertaway.com)
* **Source Code:** [MQTT-home/linux/alertaway](https://github.com)

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

* [Eclipse Mosquitto](https://mosquitto.org) – MQTT Broker [1]
* [zigbee2mqtt](https://github.com) – ZigBee to MQTT bridge [1]
* [fauxmo](https://github.com) – Lightweight Amazon Alexa emulation [1]
* [DiyHue](https://diyhue.org) – Philips Hue ecosystem emulation [1]
* **Core Stack:** Python 3, SQLite 3, and structured SQL.

---

## 💻 Hardware Requirements

AlertAway is highly optimized to run on virtually any small single-board computer (SBC) capable of hosting Linux.

* **Network:** An RJ45/Ethernet port for a reliable, hardwired connection directly to your home router.
* **USB:** At least one available USB port to host a [compatible ZigBee adapter/dongle](https://zigbee2mqtt.io).

### Current Development Reference Stack [1]
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

This project is open-source software licensed under the terms of the **MIT License**. See the repository's [License: MIT](https://github.com/jdodgen/AlertAway/blob/main/LICENCE) file for full details.
