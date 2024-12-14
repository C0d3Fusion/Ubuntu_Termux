
# How to Install Ubuntu in Termux

This guide will help you set up Ubuntu on your Android device using Termux.

---

## Steps to Install Ubuntu in Termux

1. **Install Termux**  
   Download and install Termux from the [official GitHub page](https://github.com/termux/termux-app).  
   Open Termux and update it by running the following command:  
   ```bash
   pkg update && pkg upgrade
   ```

2. **Install Required Packages**  
   Install the necessary packages for Ubuntu installation:  
   ```bash
   pkg install proot-distro wget
   ```

3. **Install Ubuntu**  
   Use Proot-Distro to install Ubuntu:  
   ```bash
   proot-distro install ubuntu
   ```  
   Wait for the installation to complete. It will download and set up Ubuntu.

4. **Start Ubuntu**  
   Once the installation is finished, start Ubuntu by running:  
   ```bash
   proot-distro login ubuntu
   ```  
   You will now be inside the Ubuntu environment.

5. **Update Ubuntu**  
   Update the Ubuntu packages to the latest versions:  
   ```bash
   apt update && apt upgrade -y
   ```

6. **Install Additional Tools (Optional)**  
   Install commonly used tools and packages as needed:  
   - Install Python:  
     ```bash
     apt install python3 -y
     ```  
   - Install Git:  
     ```bash
     apt install git -y
     ```  
   - Install Vim:  
     ```bash
     apt install vim -y
     ```

7. **Exit Ubuntu**  
   To exit the Ubuntu environment and return to the Termux terminal, type:  
   ```bash
   exit
   ```

8. **Re-enter Ubuntu**  
   Whenever you want to access Ubuntu again, use this command:  
   ```bash
   proot-distro login ubuntu
   ```

9. **Uninstall Ubuntu**  
   If you need to remove Ubuntu, run:  
   ```bash
   proot-distro remove ubuntu
   ```

10. **Grant Storage Access (Optional)**  
    To allow Termux to access files outside its environment, run:  
    ```bash
    termux-setup-storage
    ```

---

## Additional Notes
- **No Root Required**: This method does not require a rooted device.  
- **Flexibility**: You can install other tools as needed using the `apt` package manager.  

Now you have successfully installed and configured Ubuntu on Termux. Enjoy exploring Linux on your Android device!
