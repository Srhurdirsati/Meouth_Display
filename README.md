# 🖥️ E-Paper Desk Display with Seeed XIAO RP2040  

Hey BOSS , Look what I've made , another cool project

This is a **cool little desk gadget** I built using a **Seeed XIAO RP2040** and a **4.2″ e-Paper display**.  
It shows the **time, date, temperature, and weather conditions** in real time – all information tken from my PC and sent to the e-Paper via USB.  

Think of it as a **minimalist smart desk clock*(  that never distracts, looks awesome, and keeps your workspace futuristic.  

---

## ✨ What it does  
-  Always shows the **current time**  
-  Displays the **date**  
-  Fetches **temperature** from your city  
-  Shows **weather conditions** (Clear, Clouds, Rain, etc.)  
-  Uses a **low-power e-Paper screen** that keeps the image even when idle  
-  Powered & updated via a **single USB-C cable**  

---

## 🛠️ Hardware I used  
- [Seeed Studio XIAO RP2040](https://wiki.seeedstudio.com/XIAO-RP2040/)

- [4.2″ Black & White e-Paper Display (SSD1683)](https://robu.in/product/4-2-inch-high-refresh-rate-black-and-white-e-paper-display/)
  
- A simple USB-C cable for XIAO

---

## 📐 Wiring (XIAO RP2040 ↔ e-Paper)  

| e-Paper Pin | XIAO RP2040 Pin | Function        |
|-------------|----------------|----------------|
| **BUSY**    | D4             | Busy signal    |
| **RST**     | D5             | Reset          |
| **DC**      | D6             | Data/Command   |
| **CS**      | D7             | Chip Select    |
| **CLK (SCK)** | D8           | SPI Clock      |
| **DIN (MOSI)** | D10         | SPI Data       |
| **VCC**     | 3.3V           | Power          |
| **GND**     | GND            | Ground         |

---

## ⚙️ Software Setup  

### 1️⃣ Arduino Side (XIAO RP2040)  
- Install [Arduino IDE](https://www.arduino.cc/en/software)  
- Add the **RP2040 board package**  
- Install libraries:  
  - `GxEPD2` (by Jean-Marc Zingg)  
  - `Adafruit GFX`  
- Flash the sketch: [`xiao_epaper.ino`](./xiao_epaper.ino)  

### 2️⃣ PC Side (Python Script)  
- Install Python 3  
- Install dependencies:  
  ``` pip install pyserial requests ```

And then run it 
```python send_weather.py``` aftre saving it by the name ```send_weather.py```



