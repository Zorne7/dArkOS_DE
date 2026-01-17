# 🌙 dArkOS_DE

> Elegant and efficient tools to install and enable a Desktop Environment on dArkOS

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![dArkOS](https://img.shields.io/badge/compatible%20with-dArkOS-darkblue.svg)](https://github.com/christianhaitian/dArkOS)

## 📋 Overview

**dArkOS_DE** provides a suite of automated scripts to easily install and configure a Desktop Environment (DE) on [dArkOS](https://github.com/christianhaitian/dArkOS), a modern and lightweight Linux distribution.

Perfect if you want an intuitive GUI while maintaining the lightweight nature of dArkOS!

## ✨ Features

- 🚀 **Automated Installation** - Completely automated scripts
- ⚡ **Lightweight & Fast** - Optimized for performance
- 🎯 **Easy to Use** - Just run the commands
- 🛡️ **Safe & Tested** - Compatible with official dArkOS

## 🖥️ Supported Desktop Environments

- **XFCE4** - Lightweight, responsive and customizable ✅

*Support for other DEs coming soon...*

## 📁 Included Files

| File | Description |
|------|-------------|
| `DE_install.sh` | Desktop Environment installation script |
| `DE_start.sh` | Script to start the DE |
| `README.md` | This file |

## 💡 Requirements

- dArkOS (or a compatible distribution)
- Administrator/sudo permissions
- Internet connection for package downloads
- An SD card or storage device
- SSH and SFTP access capabilities

---

## 🚀 Installation Guide

Follow these steps to install and run the Desktop Environment on dArkOS:

### Step 1: Install dArkOS on SD Card

1. Download the latest dArkOS image from the [official repository](https://github.com/christianhaitian/dArkOS)
2. Flash the image to an SD card using tools like:
   - **Balena Etcher** (recommended)
   - **Rufus**
   - **dd** command on Linux/Mac
3. Safely eject the SD card

### Step 2: Boot dArkOS

1. Insert the SD card into your device
2. Power on the device and wait for dArkOS to boot
3. You should see the dArkOS boot screen

### Step 3: Configure Network Connection

1. Access the dArkOS settings menu
2. Navigate to **Network/WiFi** settings
3. Select your WiFi network
4. Enter your WiFi password
5. Wait for the connection to establish

### Step 4: Enable Remote Services

1. Go to **Settings**
2. Enable **SSH** - for remote command execution
3. Enable **SFTP** - for file transfer
4. Note down your device's IP address (shown in Network settings)

### Step 5: Transfer Installation Scripts

On your computer, use SFTP to upload the scripts:

```bash
# Connect to your device via SFTP
sftp root@<device-ip>

# Upload the scripts
put DE_install.sh
put DE_start.sh

# Exit SFTP
bye
```

Replace `<device-ip>` with your device's actual IP address.

### Step 6: Run Installation via SSH

Connect to your device via SSH and execute the installation script:

```bash
# SSH into your device
ssh root@<device-ip>

# Run the installation script
bash DE_install.sh

# Wait for installation to complete (this may take several minutes)
```

### Step 7: Start the Desktop Environment

After installation completes, start the DE:

```bash
bash DE_start.sh
```

The Desktop Environment should now be running on your device!

---

## 🎮 Quick Command Reference

```bash
# Install the DE
bash DE_install.sh

# Start the DE
bash DE_start.sh
```

---

## ⚠️ Known Issues

The following issues are currently known and may affect your experience:

### 🎮 Controller Cannot Be Used as Mouse
- **Description:** Game controllers and joysticks cannot be used to control the mouse cursor
- **Workaround:** Use a USB mouse or keyboard for navigation
- **Status:** Under investigation

### ⌨️ Virtual Keyboard Not Functioning
- **Description:** The on-screen virtual keyboard does not appear or respond to input
- **Workaround:** Use a physical keyboard for text input
- **Status:** Under investigation

---

## 🔗 Useful Links

- [dArkOS Official Repository](https://github.com/christianhaitian/dArkOS) - Official dArkOS project
- [XFCE Desktop Environment](https://www.xfce.org/) - Official XFCE website

---

## 📝 License

This project is distributed under the MIT License.

---

**Built to simplify the dArkOS experience** 🎉