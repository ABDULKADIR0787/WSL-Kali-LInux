# WSL-Kali-LInux

To install Kali Linux and set up Remote Desktop Protocol (RDP) on Windows 11, follow these step-by-step instructions:

### Step 1: Enable Windows Subsystem for Linux (WSL)
1. **Open PowerShell as Administrator:** Press `Windows Key + X` and select "Windows PowerShell (Admin)."
2. **Enable WSL:** Run the following command:
   ```sh
   wsl --install
   ```
3. **Restart Your Computer:** Restart your computer to apply the changes.

### Step 2: Install Kali Linux from Microsoft Store
1. **Open Microsoft Store:** Click on the Microsoft Store icon on your taskbar or search for it in the Start menu.
2. **Search for Kali Linux:** Type "Kali Linux" in the search bar and select the Kali Linux app from the search results.
3. **Install Kali Linux:** Click the "Install" button to download and install the Kali Linux app.

### Step 3: Launch Kali Linux
1. **Open Kali Linux:** Once installed, click the "Launch" button in the Microsoft Store or find Kali Linux in your Start menu and open it.
2. **Set Up Kali Linux:** Follow the on-screen instructions to complete the initial setup, including creating a username and password.

### Step 4: Install XRDP on Kali Linux
1. **Open Kali Linux Terminal:** Once Kali Linux is running, open the terminal.
2. **Update Package List:** Run the following command:
   ```sh
   sudo apt update
   ```
3. **Install XRDP:** Run the following command to install XRDP:
   ```sh
   sudo apt install xrdp
   ```
4. **Enable XRDP Service:** Run the following command to enable XRDP on startup:
   ```sh
   sudo systemctl enable xrdp
   ```
5. **Start XRDP Service:** Run the following command to start the XRDP service:
   ```sh
   sudo systemctl start xrdp
   ```
6. **Check XRDP Service Status:** Run the following command to check the status of the XRDP service:
   ```sh
   sudo systemctl status xrdp
   ```
7. **Find Your IP Address:** Run the following command to find your IP address:
   ```sh
   ip a
   ```
8. **Connect from Windows 11:**
   - Open the Remote Desktop Connection app on Windows 11 (`mstsc`).
   - Enter the IP address of your Kali Linux machine and click "Connect."
   - Enter your Kali Linux username and password to access the remote desktop.

### Step 5: Optional Configuration
1. **Adjust XRDP Settings:** If needed, you can adjust the XRDP settings in the configuration file `/etc/xrdp/xrdp.ini` to customize your remote desktop experience.

That's it! You should now be able to access your Kali Linux desktop from your Windows 11 machine using RDP. If you encounter any issues, feel free to ask for further assistance!
