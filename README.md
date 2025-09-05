# Meouth_Display  

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

## Images 

<img width="934" height="458" alt="Screenshot from 2025-09-04 10-51-11" src="https://github.com/user-attachments/assets/6e78ad2e-aa5f-498a-a266-02564eb537b9" />

<img width="1920" height="1080" alt="Screenshot from 2025-09-04 12-28-22" src="https://github.com/user-attachments/assets/c31b01fb-e424-47e7-a4ba-a780cd50f649" />

<img width="1920" height="1080" alt="Screenshot from 2025-09-04 12-29-07" src="https://github.com/user-attachments/assets/2647cae9-ab1b-44bb-9bbc-3cbb62ad3afd" />

<img width="1920" height="1080" alt="Screenshot from 2025-09-04 12-42-15" src="https://github.com/user-attachments/assets/617945bf-d291-4132-830d-dbc3be3cc653" />

<img width="1920" height="1080" alt="Screenshot from 2025-09-04 12-42-28" src="https://github.com/user-attachments/assets/bc080120-3b1a-4509-965e-da5e11e39fb2" />
<img width="742" height="634" alt="Screenshot from 2025-09-04 10-52-03" src="https://github.com/user-attachments/assets/c60cccf2-c7af-40dc-b9fe-439d4aac0d9f" />

<img width="806" height="657" alt="Screenshot from 2025-09-04 10-54-39" src="https://github.com/user-attachments/assets/3f0c7f29-b90b-4d38-912c-195d9d593a08" />

<img width="889" height="734" alt="Screenshot from 2025-09-04 10-54-50" src="https://github.com/user-attachments/assets/4fa1b555-9b31-456c-961b-bd571af451a6" />

<img width="919" height="942" alt="Screenshot from 2025-09-04 10-55-08" src="https://github.com/user-attachments/assets/21eec221-ed9b-4cd1-b93d-b9e8f08bea08" />

<img width="745" height="850" alt="Screenshot from 2025-09-04 10-51-38" src="https://github.com/user-attachments/assets/fb1eaa44-eb1b-46af-bc9f-798ab3d2fa82" />

## 🛠️ Hardware I used  
- [Seeed Studio XIAO RP2040](https://wiki.seeedstudio.com/XIAO-RP2040/)- By HQ

- [4.2″ Black & White e-Paper Display (SSD1683)](https://robu.in/product/4-2-inch-high-refresh-rate-black-and-white-e-paper-display/) - $28.38
  
- A simple USB-C cable for XIAO - I managed it from a corner of my house . ~$2

- PCB - JLCPCB - $34 

```
Total - ~$68
```

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



