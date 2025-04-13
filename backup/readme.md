# RaspberryPi_ComputerModule3B_Backup  
- Works on Linux (Ubuntu) or a virtual machine  

## Install the Rpiboot Driver  
1. First, install `git`:  
```sh
sudo apt install git
```  

2. Clone the specified GitHub repository and switch to the `usbboot` directory:  
```sh
git clone --depth=1 https://github.com/raspberrypi/usbboot
cd usbboot
```  

3. Install `libusb-1.0-0-dev`:  
```sh
sudo apt install libusb-1.0-0-dev
```  

4. Use `make` to build and install the `usbboot` tool:  
```sh
make
```  

5. Run the `usbboot` tool and wait for the Raspberry Pi to connect:  
```sh
sudo ./rpiboot
```  
> Now connect the Raspberry Pi to your PC or laptop. On Linux, you might be prompted to approve the device or grant permission. Once approved, the terminal will start processing automatically.

6. Use `lsblk` to check the connected Raspberry Pi device. You can identify it by its storage size (e.g., `/dev/sdX`):  
```sh
lsblk
```  

## Start Backing Up the System  
1. Open a terminal in the directory where you want to save the `.img` file, then run the `dd` command:  
```sh
sudo dd of=raspberry.img if=/dev/sdX bs=1M
```  
**Note on `dd`:**  
- Used for backing up or restoring entire disks.  
- Can be used to copy raw device files like the MBR (Master Boot Record).  
- Supports data format conversion (e.g., ASCII to EBCDIC, case conversion).  
- Can create fixed-size files.  
- `if=` specifies the input file/device.  
- `of=` specifies the output file.  
⚠️ **Be very careful when using `dd` with root privileges! A wrong command can corrupt your system and data.**

## Compress the Img File  
1. Download the PiShrink script from GitHub:  
```sh
wget https://raw.githubusercontent.com/Drewsif/PiShrink/master/pishrink.sh
```  

2. Set execute permission for the script:  
```sh
chmod +x pishrink.sh
```  

3. Move `pishrink.sh` to `/usr/local/bin`:  
```sh
sudo mv pishrink.sh /usr/local/bin
```  

4. Move your `.img` file to `/usr/local/bin` and run the compression:  
```sh
sudo pishrink.sh "your img"
```  
