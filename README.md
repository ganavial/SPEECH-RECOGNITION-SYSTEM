# SPEECH-RECOGNITION-SYSTEM
"Company": CODTECH IT SOLUTION
"NAME": GANAVI AL
"INTERN ID" :CT04DG130
"DOMAIN": EMBEDDED SYSTEM
"DURATION": 4 WEEKS
"MENTO": NEELA SANTHOS

🗣️ Task-4: Speech Recognition System
Internship Program: CODTECH IT SOLUTIONS PVT. LTD
Internship Duration: June 5 – July 5, 2025
Platform: Arduino UNO + Tinkercad (Simulation)
Domain: Embedded Systems

📌 Objective:
The objective of this task is to design and simulate a Speech Recognition-Based Device Control System using Arduino. The system should respond to voice commands such as "turn on light" or "turn off fan" to control output devices like LEDs or relays. In this simulation, due to Tinkercad's limitations, actual speech input is replaced by Serial Monitor commands that mimic voice input.

🧠 Project Summary:
Speech recognition is a modern and intuitive way to control electronic systems. It allows users to operate devices hands-free, which is particularly beneficial in home automation, accessibility devices for disabled individuals, and smart environments. In embedded systems, speech recognition can be achieved using modules like the Elechouse Voice Recognition Module, Google Assistant via Bluetooth, or MIT App Inventor apps.

However, since Tinkercad does not support voice input or Bluetooth modules, we simulate speech commands using the Serial Monitor, where typing "on1" is equivalent to saying "turn on device 1", and so on. The Arduino reads these text inputs, interprets the commands, and performs the appropriate actions.

🧰 Components Used:
Arduino UNO

Breadboard

2 LEDs (representing appliances)

2 Resistors (220Ω)

Jumper Wires

Serial Monitor (used as simulated speech input)

🔌 Circuit Description:
Component	Arduino Pin	Purpose
LED1	Pin 7	Simulated appliance 1
LED2	Pin 8	Simulated appliance 2
Resistors	In series	Current limiting for LEDs
GND	Arduino GND	Common ground for LEDs

Each LED is connected to a digital pin and turns ON or OFF based on received commands, simulating the effect of a speech command.

💻 Arduino Code:
cpp
Copy
Edit
String command;

void setup() {
  Serial.begin(9600);
  pinMode(7, OUTPUT); // LED1
  pinMode(8, OUTPUT); // LED2
}

void loop() {
  if (Serial.available()) {
    command = Serial.readStringUntil('\n');

    if (command == "on1") {
      digitalWrite(7, HIGH);
    } else if (command == "off1") {
      digitalWrite(7, LOW);
    } else if (command == "on2") {
      digitalWrite(8, HIGH);
    } else if (command == "off2") {
      digitalWrite(8, LOW);
    }
  }
}
🧪 Simulation Steps in Tinkercad:
Open Tinkercad Circuits
Create a new circuit with Arduino UNO
Add 2 LEDs and 220Ω resistors
Connect LEDs to pins 7 and 8, GND through resistors
Paste the code above into the code editor
Start the simulation
Open Serial Monitor
Type commands such as:

on1 → LED1 ON

off1 → LED1 OFF

on2 → LED2 ON

off2 → LED2 OFF

These simulate spoken commands that would normally be recognized by a voice input module or app.

🎯 Learning Outcomes:
Understanding of command-based device control
Use of Serial communication as a simulated input interface
Logical programming using if-else conditions
Basic circuit building with LEDs and output control
Exposure to voice-to-action conversion logic

🌍 Real-World Applications:
In real life, speech recognition systems can:
Enable voice-controlled smart homes
Support assistive devices for the elderly or disabled
Integrate with Google Assistant or Alexa
Connect with smartphones via Bluetooth or Wi-Fi
With hardware modules or smartphone integration, this project can evolve into a fully functional IoT speech automation system.

🔮 Future Scope:
Use actual speech modules like Elechouse V3

Connect with Google Assistant via IFTTT and Bluetooth

Create a mobile app using MIT App Inventor for voice input

Expand system to support multiple appliances and natural language commands

📝 Conclusion:
The Speech Recognition System designed in this task successfully simulates the behavior of a voice-controlled embedded application. By substituting voice input with typed text commands, the project maintains its logical structure and serves as a solid foundation for real-world voice automation. This task builds strong fundamentals in serial communication, command parsing, and embedded decision-making—essential skills in modern IoT and automation systems.

OUTPUT
![Image](https://github.com/user-attachments/assets/e1eec093-18f2-4ffa-8af4-3bb45236646e)
