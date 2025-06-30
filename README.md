# Controlled LED System with Arduino and Buttons

This Arduino project demonstrates how to control **three individual LEDs** using **three push buttons**. It’s a beginner-friendly project to learn how input (buttons) can be used to control output (LEDs) through digital pins.

Overview:

- Each of the 3 push buttons is connected to the Arduino.
- Each button controls **one LED**.
- When a button is pressed, the corresponding LED lights up.
- When the button is released, the LED turns off.

This is a practical example of digital input/output control using Arduino.

Components:

- Arduino UNO
- Breadboard
- 3 Push Buttons
- 3 LEDs (Red)
- 3 Resistors for LEDs (220Ω–330Ω recommended)
- 3 Resistors for buttons (10kΩ pull-down)
- Jumper wires


```Code:
//Buttons
const int buttonPin1 = 2;  
const int buttonPin2 = 3;
const int buttonPin3 = 4; 

//LEDs
const int ledPin1 = 5;
const int ledPin2 = 6;
const int ledPin3 = 7;

void setup() {
  pinMode(buttonPin1, INPUT);
  pinMode(buttonPin2, INPUT);
  pinMode(buttonPin3, INPUT);

  pinMode(ledPin1, OUTPUT);
  pinMode(ledPin2, OUTPUT);
  pinMode(ledPin3, OUTPUT);
}

void loop() {
  digitalWrite(ledPin1, digitalRead(buttonPin1));
  digitalWrite(ledPin2, digitalRead(buttonPin2));
  digitalWrite(ledPin3, digitalRead(buttonPin3));
}
