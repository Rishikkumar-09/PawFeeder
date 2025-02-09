#include "CTBot.h"
#include <Servo.h>
#include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>

#define SCREEN_WIDTH 128
#define SCREEN_HEIGHT 64
#define OLED_RESET -1
Adafruit_SSD1306 display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, OLED_RESET);

int SERVO_PIN = D4; // Pin connected to the servo
CTBot myBot;
TBMessage msg;
String ssid  = "WIFI Username"; // Enter WiFi Username
String pass  = "Wifi Password"; // Enter WiFi Password
String token = "Token"; // Enter Your Telegram Bot Token

Servo dispenserServo;

void setup() {
  Serial.begin(115200);
  pinMode(SERVO_PIN, OUTPUT);
  dispenserServo.attach(SERVO_PIN);
  dispenserServo.write(0); // Initial position

  if (!display.begin(SSD1306_SWITCHCAPVCC, 0x3C)) {
    Serial.println("SSD1306 allocation failed");
    for (;;);
  }
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(WHITE);
  display.setCursor(0, 0);
  display.println("Starting TelegramBot...");
  display.display();

  Serial.println("Starting TelegramBot...");
  myBot.wifiConnect(ssid, pass);
  myBot.setTelegramToken(token);
  
  if (myBot.testConnection()) {
    Serial.println("\ntestConnection OK");
  } else {
    Serial.println("\ntestConnection NOK");
  }
}

void rotateServo(int times, String message) {
  for (int i = 0; i < times; i++) {
    dispenserServo.write(90); // Rotate to dispense
    delay(1000); // Hold for 1 second
    dispenserServo.write(0);  // Return to initial position
    delay(1000); // Wait before next rotation
  }
  display.clearDisplay();
  display.setCursor(0, 0);
  display.println(message);
  display.display();
}

void loop() {
  if (myBot.getNewMessage(msg)) {
    if (msg.text.equalsIgnoreCase("100g")) {    
      rotateServo(1, "Dispensed 100g");
      Serial.println("Dispensed 100g");
    }
    if (msg.text.equalsIgnoreCase("200g")) {    
      rotateServo(2, "Dispensed 200g");
      Serial.println("Dispensed 200g");
    }
  }
  delay(10);
}
