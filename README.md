# Display Time Using RTC (Real Time Clock)

This project is an Arduino program that displays the current time (hours, minutes, seconds, and date) using an RTC (Real Time Clock) module.

## 📌 Description

The program reads the current time from an RTC module and displays it on the Serial Monitor (or LCD if used). The RTC keeps accurate time even when the Arduino is powered off because it uses a backup battery.

## 🛠️ Hardware Requirements

* Arduino board (Uno / Nano / Mega)
* RTC Module (DS1307 or DS3231)
* Jumper wires
* (Optional) 16x2 LCD with I2C module
* CR2032 battery (for RTC backup power)

## 📚 Required Library

Make sure you install the following library via Arduino IDE:

* `RTClib` by Adafruit

### How to Install the Library

1. Open Arduino IDE
2. Click **Sketch → Include Library → Manage Libraries**
3. Search for **RTClib**
4. Click **Install**

## 🔌 Wiring Example (DS3231 with Arduino Uno)

| RTC Pin | Arduino Uno |
| ------- | ----------- |
| VCC     | 5V          |
| GND     | GND         |
| SDA     | A4          |
| SCL     | A5          |

> For Arduino Mega: SDA = 20, SCL = 21

## ▶️ How to Use

1. Connect the RTC module to the Arduino board.
2. Upload `menampilkan_jam_rtc.ino` to your Arduino.
3. Open **Serial Monitor**.
4. Set the baud rate according to the sketch (usually 9600).
5. The current date and time will be displayed in real-time.

## ⏰ Setting the Initial Time

If the displayed time is incorrect, uncomment the following line in the code (if available):

```cpp
rtc.adjust(DateTime(F(__DATE__), F(__TIME__)));
```

Upload the sketch once to set the RTC time based on your computer’s current time.
After that, comment the line again and re-upload to prevent the time from resetting every time the board restarts.

## 📷 Example Serial Monitor Output

```
Date : 27/02/2026
Time : 14:35:10
```

## 🚀 Features

* Displays hours, minutes, and seconds
* Displays date, month, and year
* Real-time clock updates
* Keeps time even when power is disconnected (with RTC battery)

## 📄 License

This project is open-source and free to use for educational and development purposes.

---
