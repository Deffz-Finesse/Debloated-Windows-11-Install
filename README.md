
# **Debloated Windows 11 Installation** 🚀

This project contains an unattended Windows 11 installation configuration that bypasses hardware checks, removes unnecessary bloatware, disables certain Windows services, and applies custom configurations for an optimized, streamlined experience.

The unattended installation automates the process of setting up Windows with minimal user intervention, while simultaneously removing a variety of built-in apps, optimizing system settings, and improving overall performance. Below is a detailed explanation of everything that the configuration does to the system.

---

## **Features Overview** 🛠️

1. **Bypass Hardware Checks** ⚠️
   - **TPM, Secure Boot, and RAM Checks:** Automatically bypasses TPM, Secure Boot, and minimum RAM checks, allowing installation on devices that don't meet the strict hardware requirements of Windows 11.
  
2. **Disable Windows Defender** 🛡️
   - **Runs a VBScript (`disable-defender.vbs`)** during installation that disables Windows Defender services such as:
     - `WinDefend` (Windows Defender Antivirus)
     - `WdBoot`, `WdFilter`, `WdNisDrv`, and `WdNisSvc` (related to Defender's boot and filter services).

3. **Remove Built-in Windows Apps (Debloat)** 🗑️
   - **Removes several pre-installed Windows applications** that are commonly considered bloatware. These include:
     - **Apps Removed (via `remove-packages.ps1`):**
       - 3D Viewer, Bing Search, Calculator, Camera, Clipchamp, Alarms, Feedback Hub, Microsoft Family, Get Help, Notepad, Paint, Sticky Notes, Skype, Xbox, Your Phone, Zune Music, and others.
     - **Capabilities Removed (via `remove-caps.ps1`):**
       - Internet Explorer, Math Recognizer, WordPad, Notepad, PowerShell ISE, Windows Media Player, Snipping Tool, and Quick Assist.
     - **Features Removed (via `remove-features.ps1`):**
       - Remote Desktop Connection, Microsoft Recall, and Snipping Tool.

4. **Custom User Accounts** 👤
   - **Automatically creates local user accounts**:
     - `Admin` with administrative privileges.
     - `REPLACE-ME` as a standard user.
   - Passwords for these accounts are specified during setup (replace `REPLACE-ME` placeholders with actual passwords).
   - **REPLACE-ME** placeholders in the unattended XML:
     - For Admin and Standard User: Username and password.
     - Computer name.

5. **Auto Logon** 🔑
   - **Automatically logs in the `Admin` account** upon first boot to streamline setup.

6. **First Logon Commands (Custom System Configurations)** 🖥️
   Several customizations are applied automatically at the first logon to optimize performance and behavior:
   
   - **Disable Search Indexing:**
     - Disables search indexing for all drives except `C:\Users` to improve performance.
   - **Disable Prefetcher:**
     - Disables the prefetcher to optimize memory usage.
   - **Disable Unused Services:**
     - Disables services like:
       - `XboxGipSvc`, `XboxNetApiSvc` (related to Xbox features)
       - `Fax`, and `Print Spooler`
   - **Apply High-Performance Power Plan:**
     - Applies the "Ultimate Performance" power plan for optimal system performance.
   - **Install AMD Drivers (if applicable):**
     - Installs drivers from the `C:\Drivers\AMD` directory if present.

7. **Windows Customizations** 🎨
   The following customizations are applied to the Windows UI and system behavior:
   
   - **Move Taskbar to the Left:**
     - Moves the taskbar alignment to the left, similar to the classic Windows layout.
   - **Enable Classic Right-Click Context Menu:**
     - Restores the classic context menu behavior in Windows 11.
   - **Show Hidden Files and File Extensions:**
     - Configures File Explorer to display hidden files and file extensions.
   - **Disable "News and Interests" Widget:**
     - Removes the "News and Interests" feature from the taskbar.

8. **Windows Update Customizations** 🌀
   - **Disable Automatic Restarts for Logged-On Users:** Prevents Windows from automatically restarting while users are logged on after updates.
   - **Disables Unnecessary Features in Windows Update (e.g., DevHome Updates)**

9. **Disable Windows Copilot and Other Features** 🤖
   - **Removes Windows Copilot and related services:**
     - Disables Windows Copilot by removing associated registry entries and services.

10. **Virtual Machine Tools Installation** 🖥️💻
    - **Detects and installs guest additions** for VirtualBox and VMware:
      - **VirtualBox Guest Additions:**
        - Installs Guest Additions automatically if detected.
      - **VMware Tools:**
        - Installs VMware Tools automatically if detected.

11. **Registry Tweaks and Additional Optimizations** 🛠️
    - **Enable Long File Paths:** 
      - Enables support for file paths longer than the default 260 characters.
    - **Disable UAC (User Account Control)**

---

### **Important Notes:**

- **REPLACE-ME placeholders:** Ensure you update the XML with the appropriate usernames, passwords, and computer names in the following sections:
  - **User Accounts:** Replace the username and password (Admin and standard user).
  - **Computer Name:** Replace the `REPLACE-ME` with your desired computer name.
---

## **How to Use** 🔧

1. **Download the repository**: 
   ```bash
   git clone https://github.com/Deffz-Finesse/Debloated-Windows-11-Install.git
   ```

2. **Modify the unattended.xml file:**
   - Open `unattend.xml` and replace the `REPLACE-ME` placeholders with the actual user information and computer name.

3. **Create a Bootable USB Drive**:
   - Use a tool like [Rufus](https://rufus.ie/) to create a bootable USB drive and Copy the autounattend.xml file to the root folder of the USB drive that contains the Windows Setup files and connect it to the computer

4. **Install Windows**: 
   - Boot from the USB and the installation will proceed automatically with the provided configurations.

Enjoy your streamlined, debloated Windows 11 installation! 🎉
