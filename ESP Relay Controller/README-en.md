# ESP Relay Controller

A relay control system based on ESP-01 (ESP8266) microcontroller with web interface and webhook API for remote control.

## 📁 Project Versions

### 🔧 [rele-activator-v01-final](./rele-activator-v01-final) - Basic Version
**Relay control system with web interface and webhook API**

- 🎛️ **Relay control** via GPIO0 (Pin 5)
- 🌐 **Web interface** with modern design
- 🔗 **Webhook API** for integration with external systems
- ⏱️ **Configurable pulse duration** (1-1000 ms)
- 📊 **Status monitoring** and operation statistics
- 📶 **WiFi connection** with automatic setup

### 🤖 [rele-activator-v02-with-tg](./rele-activator-v02-with-tg) - Extended Version with Telegram
**All basic version features + Telegram Bot integration**

- ✅ **All basic version features**
- 🤖 **Telegram Bot integration** for remote control
- 📱 **Telegram notifications** about all operations
- ⚙️ **Web interface for configuring** Telegram bot
- 🔐 **Secure SSL connection** for Telegram API
- 📋 **Setup instructions** in web interface

## 🚀 Key Features

- **Relay control** via GPIO0 (Pin 5)
- **Web interface** with modern design
- **Webhook API** for integration with external systems
- **Configurable pulse duration** (1-1000 ms)
- **Status monitoring** and operation statistics
- **WiFi connection** with automatic setup
- **Telegram Bot** for mobile control (v02)

## 🔧 Technical Specifications

- **Microcontroller**: ESP-01 (ESP8266)
- **Relay GPIO**: GPIO0 (Pin 5)
- **Default**: 5 ms pulse
- **Web server**: port 80
- **Connection**: WiFi
- **Telegram**: SSL connection (v02)

## 📡 API Endpoints

### Main Routes

- **`/`** - Main control page
- **`/relay`** - Relay activation (5 ms default)
- **`/enable`** - Webhook for quick activation (5 ms)
- **`/activate?ms=X`** - Webhook with custom time (1-1000 ms)
- **`/status`** - JSON system status
- **`/telegram`** - Telegram bot configuration (v02 only)

### Usage Examples

```bash
# Quick activation (5 ms)
curl http://[IP]/enable

# Activation with custom time (10 ms)
curl "http://[IP]/activate?ms=10"

# Get status
curl http://[IP]/status
```

## 🤖 Telegram Bot (v02)

### Setup
1. Create a bot via [@BotFather](https://t.me/BotFather) in Telegram
2. Get the bot token
3. Find out your Chat ID
4. Configure via web interface `/telegram`

### Features
- **Notifications** about all relay operations
- **System status** on request
- **Secure connection** via SSL
- **Easy configuration** via web interface

## ⚙️ Configuration

1. **WiFi connection**: change `ssid` and `password` in code
2. **Relay GPIO**: GPIO0 (Pin 5) is used by default
3. **Pulse duration**: configure `defaultPulseDurationMs`
4. **Telegram Bot** (v02): configure `telegramBotToken` and `telegramChatID`

## 🔌 Connection Diagram

```
ESP-01 GPIO0 (Pin 5) → Relay → Load
```

## 📊 Features

- **Automatic WiFi reconnection**
- **Overload protection** (maximum 1000 ms)
- **Operation statistics** (activation count, last activation time)
- **System information** (memory, uptime, GPIO state)
- **Responsive web interface** for mobile devices
- **Telegram integration** for mobile control (v02)

## 📈 Monitoring

The system provides:
- Relay activation count
- Time since last activation
- WiFi connection status
- Signal strength (RSSI)
- Free memory
- System uptime
- Telegram bot status (v02)

## 🔒 Security

⚠️ **Warning**: Current version has no authentication. Recommended to use only in secure networks or add authorization for production.

## 📚 Requirements

### Basic Version (v01)
- Arduino IDE with ESP8266 support
- Libraries: ESP8266WiFi, ESP8266WebServer
- ESP-01 module
- Relay module
- 3.3V power supply

### Extended Version (v02)
- All basic version requirements
- Libraries: UniversalTelegramBot, ArduinoJson
- SSL certificates for Telegram API

## 🎯 Applications

- **Process automation**
- **Smart home** and IoT solutions
- **Industrial control**
- **Equipment testing**
- **Monitoring and notifications** (v02)

## 📄 License

Project is distributed under the license specified in the root README.md

