#include <Arduino.h>
#include <Wire.h>
#include <SoftwareSerial.h>

SoftwareSerial Bluetooth(10,11);
char Data;

void setup() {
  Bluetooth.begin(38400);
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(7, OUTPUT);
}

void loop() {
  if (Bluetooth.available()) {
    Data = Bluetooth.read();
    
    // LED 1
    if (Data == '5') digitalWrite(5, HIGH);
    if (Data == '1') digitalWrite(5, LOW);

    // LED 2
    if (Data == '6') digitalWrite(6, HIGH);
    if (Data == '2') digitalWrite(6, LOW);

    // LED 3
    if (Data == '7') digitalWrite(7, HIGH);
    if (Data == '3') digitalWrite(7, LOW);

    // ALL LEDs
    if (Data == '9') {
      digitalWrite(5, HIGH);
      digitalWrite(6, HIGH);
      digitalWrite(7, HIGH);
    }
    if (Data == '0') {
      digitalWrite(5, LOW);
      digitalWrite(6, LOW);
      digitalWrite(7, LOW);
    }
  }
}
