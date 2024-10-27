# Ubuntu_Installation_Guide
This guide offers a step-by-step process for installing Ubuntu. It covers downloading the ISO, creating a bootable USB, adjusting BIOS/UEFI settings, and finalizing the installation. Ideal for beginners and advanced users alike, it ensures a smooth setup of Ubuntu on your computer.


# **Ubuntu Installation Guide**

## **1. Requirements**
Before starting the Ubuntu installation, make sure you have the following:
- **An empty USB stick** (minimum 8 GB recommended)
- **Ubuntu ISO file** (downloadable from the official website)
- **A tool to create a bootable USB** (e.g., **Rufus** or **Balena Etcher**)

## **2. Download the Ubuntu ISO File**
1. Visit the official Ubuntu website: [Download Ubuntu](https://ubuntu.com/download).
2. Choose the version of Ubuntu you want (Recommended: **Ubuntu 22.04 LTS**).
3. Download the ISO file to your computer.

## **3. Create a Bootable USB**
### **For Windows Users:**
1. Download and run **Rufus**: [Download Rufus](https://rufus.ie/).
2. In the **Device** section, select your USB stick.
3. In the **Boot selection** section, choose the downloaded Ubuntu ISO file.
4. Click the **Start** button and wait for the bootable USB creation process to finish.

### **For Linux Users:**
1. Open the terminal and use the following commands to write the ISO file to the USB:
   
   ```bash
   sudo dd if=/path/to/ubuntu.iso of=/dev/sdX bs=4M
   sync
   ```

   **Note:** Replace `sdX` with your USB device identifier (e.g., `/dev/sdb`).

## **4. Configure BIOS/UEFI Settings**
1. Restart your computer and enter BIOS/UEFI (Usually by pressing **Del**, **F2**, **F10**, or **Esc** during boot).
2. In the **Boot Order** section, move your USB stick to the top.
3. Save the changes and exit.

## **5. Start the Ubuntu Installation**
1. When your computer restarts, it should boot from the USB stick.
2. Choose **"Install Ubuntu"** from the options ("Try Ubuntu" or "Install Ubuntu").
3. Follow the installation wizard:
   - Choose your **language**.
   - Select the **keyboard layout**.
   - Decide whether to install **updates and third-party software**.

## **6. Disk Partitioning**
1. In the **Installation Type** section, choose how you want to install Ubuntu:
   - **Erase disk and install Ubuntu**: Installs a clean version of Ubuntu by wiping the entire disk.
   - **Something else**: Allows you to customize partition settings.
2. Choose the desired option and proceed.

## **7. Create a User Account**
1. Set a username, computer name, and password.
2. The password should be secure and memorable.

## **8. Complete the Installation**
1. After configuring all the settings, click the "Install Now" button.
2. Once the installation is complete, restart the computer and remove the USB stick.
3. Your Ubuntu is now ready!

## **9. Final Settings and Updates**
1. When the system starts, run the **Update Manager** and install updates:
   
   ```bash
   sudo apt update
   sudo apt upgrade
   ```

2. Install any necessary drivers and additional software.
