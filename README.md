# 🌟 ESP32 Single-LED Light Shift – Sequential GPIO Blinker

A simple and elegant LED project using an ESP32, where 5 LEDs light up **one at a time in a sequence**, creating a clean left-to-right (or directional) chase effect. Perfect for learning GPIO control and timing with `digitalWrite()`.

---

## 🔌 GPIO Pin Mapping

| LED Color | GPIO Pin | ESP32 Label | Resistor | Notes                       |
|-----------|----------|-------------|----------|-----------------------------|
| Red       | GPIO 2   | G2          | 220Ω     | Anode (+) to GPIO pin       |
| Yellow    | GPIO 4   | G4          | 220Ω     |                             |
| Green     | GPIO 5   | G5          | 220Ω     |                             |
| Blue      | GPIO 15  | G15         | 220Ω     |                             |
| White     | GPIO 18  | G18         | 220Ω     | Last in sequence            |

---

## 🛠️ Setup Instructions

1. Place 5 LEDs in a row on your breadboard.
2. Connect each **anode (+)** of the LED to its corresponding ESP32 GPIO pin via a **220Ω resistor**.
3. Connect all **cathodes (–)** to the **GND rail**.
4. Connect the GND rail to any **GND pin** on the ESP32.
5. Upload the `ESP32_LED_OneByOne_Sequence.ino` file using Arduino IDE or PlatformIO.
6. Watch the LEDs light up one by one in a loop!

---

## 🔁 Sequence Behavior

Each LED turns on for 400ms while all others remain off:

| Step | Active LED |
|------|------------|
| 1    | Red        |
| 2    | Yellow     |
| 3    | Green      |
| 4    | Blue       |
| 5    | White      |

Then the cycle repeats.

---

## 📃 License

MIT License — free for personal, educational, or commercial use.

---

## 💡 Tips

- Modify `delay(400)` to make the sequence faster or slower.
- Reverse the order for a right-to-left chase.
- Combine with other patterns (like all-on or fade-in) for more advanced effects.

