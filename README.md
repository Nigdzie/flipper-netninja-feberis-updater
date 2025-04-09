# Flipper NetNinja Feberis Firmware Update

## Project Description

This project provides a simple way to flash firmware onto ESP32-based NetNinja and Feberis boards using the **Flipper Zero**.

It is designed for makers, hackers, and developers who want to perform firmware updates without special tools or extra hardware – only using the Flipper Zero as a **USB-UART bridge** and the [ESP Web Flasher](https://esp.huhn.me).

Supported features:
- Flashing firmware to NetNinja / Feberis using Flipper Zero as a bridge
- Full update process via web browser (no drivers or command line required)
- Compatible with ESP32 Marauder firmware builds

---

## Example Firmware

In this example, we flash the **RogueMaster** build `RM0329-1941-0.420.0-d161b19` using the Flipper Zero and the ESP Web Flasher.

---

## Firmware Flashing Process

### ✅ Step-by-step guide

1. **Connect your NetNinja or Feberis board to the Flipper Zero** via GPIO/UART.
2. **Power on your Flipper Zero.**
3. **Enter DOWNLOAD mode** on the board:
    - Press and hold **left button**
    - While holding, press **right button once**
    - Release the **left button**
4. On the Flipper:
    - Navigate to **Apps**
  
      
    ![GPIO_Shoot](Gfx/GPIO1.jpg)
    - Navigate to **GPIO**
      
    ![GPIO_Shoot](Gfx/GPIO2.jpg)
    - Select **GPIO with I2C**
      
    ![GPIO_Shoot](Gfx/GPIO3.jpg)
    - Choose **USB-UART Bridge**
      
    ![GPIO_Shoot](Gfx/GPIO4.jpg)

6. **Connect the Flipper to your computer via USB.**

7. **Download the firmware** (example):  
   [ESP32_Marauder_FEBERIS_v1_4_1.bin](https://github.com/bpmcircuits/ESP32Marauder_FEBERIS/releases)  
   *(or any compatible .bin file)*

8. Open the browser and go to:  
   👉 [https://esp.huhn.me](https://esp.huhn.me)
    ![WEB_Shoot](Gfx/WEB1.jpg)

10. Click **Connect** and select your Flipper Zero – it should appear as a serial port (e.g. `FlipperZero (COMx)` or similar).
    ![WEB_Shoot](Gfx/WEB2.jpg)

12. In the interface, under the **0x10000** field, select the `ESP32_Marauder_FEBERIS_v1_4_1.bin` file.

    
    ![WEB_Shoot](Gfx/WEB3.jpg)
14. Click **Flash** to begin the update.

    ![WEB_Shoot](Gfx/WEB4.jpg)

---

### 🖼️ Web Interface Example

Below is an example of the web flasher setup screen:

![Web Flasher Screenshot](Gfx/WEB1.jpg)

---

## Technical Details

### NetNinja

- Communication: UART / USB-C  
- Firmware format: `.bin`  
- Power: 5V  
- [ESP32Marauder_NetNinja repo](https://github.com/bpmcircuits/ESP32Marauder_NetNinja)

### Feberis

- Communication: UART / USB-C    
- Firmware format: `.bin`
- Power: 3.3V / 5V  
- [ESP32Marauder_FEBERIS repo](https://github.com/bpmcircuits/ESP32Marauder_FEBERIS)

---

## License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## Authors

Created by [Your Name or Nickname] – contributions are welcome!
