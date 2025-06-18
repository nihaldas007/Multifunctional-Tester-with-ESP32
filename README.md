

---

# 🔌 ESP32 Multi-Function Voltameter

A DIY digital multimeter made with an **ESP32** and a **0.91" OLED display**. This compact voltameter provides various electronic test features such as:
- 📐 **Voltage Measurement**
- 📏 **Resistance Calculation**
- 🔦 **Diode Test**
- 🔔 **Continuity Check**
- 📊 **Analog Input Monitor**
- ⚙️ **Servo Motor Tester**

Perfect for hobbyists, students, and makers who want a pocket-sized multipurpose test tool.

---

## 🧰 Features

| Feature            | Description |
|--------------------|-------------|
| 🔋 Voltage Meter    | Reads voltage from analog input pin. |
| 📏 Resistor Meter   | Estimates resistance based on voltage divider method. |
| 🔦 Diode Test       | Checks forward voltage drop of a diode. |
| 🔔 Continuity Test  | Detects low-resistance paths, with buzzer alert (optional). |
| 📈 Analog Reader    | Shows real-time ADC values. |
| ⚙️ Servo Tester      | Moves servo motor between 0°–180° to test rotation. |

---

## 🖥️ Display Interface (OLED 0.91")

The 0.91-inch OLED displays real-time data with mode switching (button-based or encoder-based).

### Example Screens:

| Mode | Display Example |
|------|-----------------|
| Voltage | `Voltage: 3.72V` |
| Resistor | `R: 1.02kΩ` |
| Diode | `VF: 0.62V` |
| Continuity | `Status: Connected ✅` |
| Analog | `ADC: 1023` |
| Servo | `Servo Angle: 90°` |

---

## 📷 Demo Images

Add the following to your GitHub repo:


📁 /images
┣━ voltage\_demo.jpg
┣━ resistor\_mode.jpg
┣━ diode\_test.jpg
┣━ continuity\_mode.jpg
┣━ analog\_test.jpg
┗━ servo\_test.jpg

````

Then embed them in the README:

```markdown
### 🔋 Voltage Measurement
![Voltage Demo](images/voltage_demo.jpg)

### 📏 Resistor Mode
![Resistor Mode](images/resistor_mode.jpg)

### 🔦 Diode Test
![Diode Test](images/diode_test.jpg)

### 🔔 Continuity Test
![Continuity Mode](images/continuity_mode.jpg)

### 📊 Analog Read
![Analog Test](images/analog_test.jpg)

### ⚙️ Servo Test
![Servo Test](images/servo_test.jpg)
````

---

## 🔧 Hardware Required

| Component                 | Description                |
| ------------------------- | -------------------------- |
| ESP32 Dev Board           | Main controller            |
| OLED 0.91" Display (I2C)  | For user interface         |
| 10k / 1k Resistors        | Voltage divider            |
| Buzzer (optional)         | For continuity alerts      |
| Servo Motor (SG90/MG90)   | For testing rotation       |
| Diode (for test mode)     | Any standard silicon diode |
| Jumper Wires & Breadboard | For prototyping            |

---

## 🔌 Pin Configuration (Example)

| Function     | ESP32 Pin |
| ------------ | --------- |
| OLED SDA     | GPIO 21   |
| OLED SCL     | GPIO 22   |
| Analog Input | GPIO 34   |
| Servo Signal | GPIO 13   |
| Mode Button  | GPIO 27   |
| Buzzer       | GPIO 26   |

*You can update pin numbers in the code according to your design.*

---

## 💾 Arduino Setup

1. Install **ESP32 board support** in Arduino IDE.
2. Install required libraries:

   * `Adafruit_SSD1306`
   * `Adafruit_GFX`
   * `Servo.h` (for servo control)
3. Upload the sketch from the `/code` folder.
4. Power via USB or Li-ion battery with 5V booster.

---

## 🧪 Modes & How to Use

* **Voltage Mode**: Connect input to ADC pin. Reads 0–25V using voltage divider.
* **Resistance Mode**: Connect unknown resistor between two known nodes.
* **Diode Test**: Connect diode, cathode to GND.
* **Continuity**: Connect wires; if low resistance, buzzer will beep.
* **Analog**: Shows raw ADC value from a connected analog signal.
* **Servo Test**: Connect servo signal wire and power. Watch it sweep.

---

## 📁 Folder Structure

```
ESP32-Voltameter/
 ┣━ /images           # Demo screenshots
 ┣━ /code             # Arduino source code
 ┗━ README.md         # This file
```

---

## 📜 License

This project is open-source under the **MIT License**. Feel free to use, modify, and share.

---

## 🙌 Acknowledgements

Special thanks to the Arduino & ESP32 community for example code and libraries!

---

## 📬 Contact

For suggestions, contributions, or issues, feel free to open a GitHub issue or message me directly.
