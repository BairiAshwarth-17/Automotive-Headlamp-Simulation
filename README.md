# Automotive-Headlamp-Simulation
This project simulates an automotive feature where: •⁠  ⁠Ambient Light Sensor detects light level (lux) •⁠  ⁠BCM ECU decides whether to turn Headlamp ON/OFF •⁠  ⁠Actuator (Relay) executes the command.


# 🚗 Headlamp Auto ON System Simulation

This project simulates a simple automotive feature using *CAN messages*.

## 📌 Feature:
•⁠  ⁠*Sensor (Ambient Light Sensor)* → Detects light level (lux).
•⁠  ⁠*BCM ECU* → Decides whether to turn the headlamp ON or OFF.
•⁠  ⁠*Actuator (Relay)* → Switches the headlamp.

## 🔧 How It Works
1.⁠ ⁠Sensor sends ⁠ Ambient Light Value ⁠ on CAN (ID = 0x101).
2.⁠ ⁠BCM ECU reads the value:
   - If lux < 300 → Headlamp ON
   - Else → Headlamp OFF
3.⁠ ⁠BCM sends ⁠ Headlamp Status ⁠ (ID = 0x201).
4.⁠ ⁠Actuator executes the command.
