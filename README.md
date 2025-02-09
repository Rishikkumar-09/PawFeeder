
# 🐾 PawFeeder: Smart Telegram-Controlled Pet Feeder  

## 📌 Project Overview  
The **Smart Pet Feeder** is an IoT-based automated pet feeding system that allows users to dispense food for their pet using a Telegram bot. The system integrates a servo motor for dispensing food in predefined amounts (100g and 200g) and an Adafruit OLED display to show the feeding status.  

## 🔥 Features  
✔️ Control feeding via Telegram commands.  
✔️ Dispense **100g** or **200g** of food based on user input.  
✔️ Servo motor mechanism for controlled food dispensing.  
✔️ WiFi connectivity for remote operation.  
✔️ OLED display to show feeding status.  
✔️ Real-time feedback on food dispensing.  

## 🛠️ Components Used  
1️⃣ **ESP8266/NodeMCU** - For WiFi and Telegram bot integration.  
2️⃣ **Servo Motor** - Controls food dispensing mechanism.  
3️⃣ **Adafruit SSD1306 OLED Display** - Displays feeding confirmation.  
4️⃣ **CTBot Library** - Enables Telegram bot communication.  
5️⃣ **Arduino IDE** - Programming environment.  
6️⃣ **5V Power Supply** - Powers the ESP8266 and servo motor.  
7️⃣ **Food Storage & Dispensing Mechanism** - Holds and releases food as needed.  

## 🚀 Setup Instructions  
### 📥 1. Install Required Libraries  
- `CTBot.h`  
- `Servo.h`  
- `Wire.h`  
- `Adafruit_GFX.h`  
- `Adafruit_SSD1306.h`  

### 🔧 2. Update WiFi Credentials  
Modify the `ssid` and `pass` variables with your **WiFi details** in the code.  

### 🤖 3. Set Up Telegram Bot  
- Create a bot using **BotFather** on Telegram.  
- Copy the bot **token** and update it in the `token` variable in the code.  

### ⬆️ 4. Upload the Code  
Use **Arduino IDE** to upload the modified code to the ESP8266/NodeMCU.  

### ⚡ 5. Connect Components  
Ensure the **servo motor** and **OLED display** are correctly wired to the ESP8266.  

### 🔌 6. Power Up the System  
Once powered, the system connects to **WiFi** and is ready for **Telegram commands**.  

## 🎮 Usage  
💬 **Send** `100g` to the Telegram bot → Feeds **100g** of food.  
💬 **Send** `200g` to the Telegram bot → Feeds **200g** of food.  
🖥️ **OLED Screen** → Confirms the action.  
⚙️ **Servo Motor** → Rotates accordingly and returns to its initial position.  

## 🔮 Future Enhancements  
📅 **Scheduled Feeding** - Add a real-time clock for automated feeding.  
⚖️ **Precision Feeding** - Integrate a weight sensor for accurate food dispensing.  
📱 **Mobile App** - Develop an intuitive app for better user interaction.  
🤖 **AI-Based Food Detection** - Prevent overfeeding with smart monitoring.  
🐕 **Multi-Pet Modes** - Customize feeding portions for different pets.  
🗣️ **Voice Commands** - Enable Alexa/Google Assistant integration.  

## 🔌 Wiring Diagram  

| 🔩 Component | 🔗 ESP8266 Pin |  
|-------------|--------------|  
| 🌀 Servo Motor Signal | **D4** |  
| 📟 OLED SDA | **D2** |  
| 📟 OLED SCL | **D1** |  
| ⚡ Power (5V) | **Vin** |  
| 🛑 Ground | **GND** |  

---

## 🛡️ Security Best Practices  
🔒 **Never hardcode WiFi credentials** in the code. Use environment variables.  
🤖 **Secure the Telegram Bot Token** using a `.env` file.  
🚀 **Use a strong password** for your WiFi to prevent unauthorized access.  

## 🛠️ Troubleshooting Guide  
❌ **WiFi not connecting?** Double-check credentials and router settings.  
❌ **Servo motor not rotating?** Ensure correct wiring and sufficient power supply.  
❌ **Telegram bot not responding?** Verify the bot token and check if the ESP8266 is online.  
---

## ⭐ Show Your Support  
If you find this project useful, consider giving it a **⭐ on GitHub!**  

---

**Developed with ❤️ by Rishik kumar**  
