# 🔘 Arduino Button LED

## 📌 Project Idea
A simple project to control an LED using a push button.

- When the button is pressed → LED turns ON  
- When the button is released → LED turns OFF  

---

## ⚙️ Components
- Arduino Uno  
- LED  
- 220Ω Resistor  
- Push Button  
- Breadboard  
- Jumper Wires  

---

## 🔌 Circuit Connection
- LED:
  - Pin 13 → LED → Resistor → GND  

- Button:
  - One side → Pin 2  
  - Other side → GND  

---

## 💻 Code
```cpp
void setup() {
  Serial.begin(9600);

  pinMode(2, INPUT_PULLUP); // Button input
  pinMode(13, OUTPUT);      // LED output
}

void loop() {
  int sensorVal = digitalRead(2);

  if (sensorVal == HIGH) {
    digitalWrite(13, LOW);  // LED OFF
  } else {
    digitalWrite(13, HIGH); // LED ON
  }
}
