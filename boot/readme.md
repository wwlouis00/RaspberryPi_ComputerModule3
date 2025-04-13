# RaspberryPi_ComputerModule3_Boot  
## Flashing Method  

### 🧰 Required Components  
1. Compute Module PoE board  
2. Raspberry Pi Compute Module 3+ (CM3)  
3. MicroUSB power cable (5V 3A) suitable for Raspberry Pi 3 B / B+  
4. MicroUSB data cable  
5. HDMI cable  
6. Monitor with HDMI port  

---

### 🔧 Assembling CM3 and Carrier Board  
1. Insert the CM3 diagonally into the Compute Module PoE board  
2. Plug the Raspberry Pi power cable into the **POWER** port  
3. Connect the MicroUSB cable to the **SLAVE** port on the board and to your computer or laptop  
4. After all connections are made, press the power button on the power cable — the LED next to **POWER** should light up  

---

### 💾 Download balenaEtcher  
- Go to the official website and download the balenaEtcher installer:  
👉 [Click here](https://www.balena.io/etcher/)

---

### ⚙️ Install Rpiboot Driver (Windows)  
1. Open the default installation path:  
   `C:\Program Files (x86)\Raspberry Pi`  
2. Right-click and **Run rpiboot as Administrator**  
3. Wait for the terminal to start running  
4. At this point, plug in the **SLAVE** port of the board — it should detect the device  

---

### 🔥 Flash the `.img` using balenaEtcher  
1. Launch **balenaEtcher**  
2. Click **Flash from file** and select your `.img` file  
3. Click **Select target** and choose the Compute Module  
4. Press **Flash** to begin the flashing process  
5. Wait for it to complete  

---

### 🖥️ Booting Up the CM3  
1. Disconnect the Raspberry Pi power cable  
2. Unplug the MicroUSB data cable  
3. Connect an HDMI cable from the Compute Module to a monitor, or use a ribbon cable to connect to a small touchscreen  
4. Press the power button to boot the Raspberry Pi  
5. Confirm that the screen displays the boot process  
6. Once functionality is verified, power off the board and carefully remove the CM3 module  

---
