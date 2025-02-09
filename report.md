# Project Report: PawFeeder - Smart Telegram-Controlled Pet Feeder

## 📌 Introduction
The **PawFeeder** is an innovative IoT-based pet feeding system that allows users to control their pet’s feeding through Telegram commands. This project leverages an ESP8266 microcontroller, a servo motor, and an OLED display to automate pet feeding with predefined food quantities.

## 🎯 Objectives
- Develop an automated pet feeding system.
- Enable remote food dispensing via a Telegram bot.
- Provide real-time feedback using an OLED display.
- Ensure accurate food measurement through servo motor control.

## 🛠️ System Components
- **ESP8266/NodeMCU**: Manages WiFi connectivity and Telegram bot integration.
- **Servo Motor**: Controls the dispensing mechanism.
- **Adafruit SSD1306 OLED Display**: Provides visual feedback.
- **CTBot Library**: Enables Telegram communication.
- **Power Supply (5V)**: Powers the entire system.

## ⚙️ Working Mechanism
1. The user sends a command (`100g` or `200g`) to the Telegram bot.
2. The ESP8266 receives and processes the command.
3. The servo motor rotates accordingly to dispense the requested amount of food.
4. The OLED display shows a confirmation message.
5. The servo motor resets to its initial position after dispensing.

## 📑 Implementation Steps
1. **Set Up the Telegram Bot**: Create a bot using BotFather and obtain the bot token.
2. **Configure the ESP8266**: Upload the Arduino code with WiFi credentials and bot token.
3. **Connect Components**: Properly wire the ESP8266, servo motor, and OLED display.
4. **Deploy the System**: Power up the system and test Telegram commands.

## 🚀 Features
- **Remote feeding control via Telegram**.
- **Predefined food portions (100g, 200g)**.
- **OLED display for real-time feedback**.
- **WiFi-enabled operation**.
- **Automated servo reset after dispensing**.

## 📊 Future Enhancements
- Implement **scheduled feeding**.
- Add a **weight sensor** for precise dispensing.
- Develop a **mobile app** for a better user experience.
- Enable **voice commands** using AI integration.

## 📌 Conclusion
The **PawFeeder** simplifies pet feeding by integrating IoT technology with a user-friendly Telegram interface. This system enhances pet care by ensuring timely and accurate feeding while providing remote control convenience.

---
**Developed with ❤️ by Rishik kumar**

