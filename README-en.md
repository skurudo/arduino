# Arduino/ESP Projects Collection

A collection of projects based on Arduino and ESP8266/ESP32 microcontrollers for automation and IoT solutions.

## 📁 Project Structure

### [ESP Relay Controller](./ESP%20Relay%20Controller/) - ESP-01 Relay Controller
**Relay control system with web interface, webhook API and Telegram Bot**

#### 🔧 Basic Version (v01)
- 🎛️ **Relay control** via GPIO0 (Pin 5)
- 🌐 **Web interface** with modern design
- 🔗 **Webhook API** for integration with external systems
- ⏱️ **Configurable pulse duration** (1-1000 ms)
- 📊 **Status monitoring** and operation statistics
- 📶 **WiFi connection** with automatic setup

#### 🤖 Extended Version (v02) with Telegram
- ✅ **All basic version features**
- 🤖 **Telegram Bot integration** for remote control
- 📱 **Telegram notifications** about all operations
- 🔐 **Secure SSL connection** for Telegram API

**Applications**: Automation, smart home, industrial control, equipment testing, mobile notifications.

[📖 Detailed Description](./ESP%20Relay%20Controller/README-en.md)

## 🚀 Quick Start

### Requirements
- Arduino IDE with ESP8266/ESP32 support
- ESP-01, ESP8266 or ESP32 microcontrollers
- Required libraries for each project

### Installation
1. Clone the repository
2. Open the desired project in Arduino IDE
3. Configure WiFi and GPIO parameters
4. Upload code to device

## 🔧 Technologies

- **Languages**: C++ (Arduino), HTML/CSS/JavaScript
- **Platforms**: ESP8266, ESP32, Arduino
- **Protocols**: WiFi, HTTP, WebSocket
- **Interfaces**: Web interface, REST API, Webhook

---

**Note**: All projects are tested and ready to use. However, testing in a safe environment before production deployment is necessary!
