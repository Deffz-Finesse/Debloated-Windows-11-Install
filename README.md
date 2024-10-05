
# Windows Unattended Installation Script 🚀

This project provides an unattended installation configuration for Windows. It includes scripts that automate setup, bypass hardware checks, remove unwanted bloatware, and configure the system according to your needs.

## Key Features

- **🚫 Bypass Hardware Checks**: Automatically bypass TPM, Secure Boot, and RAM checks during installation, allowing installation on older or unsupported systems.
  
- **🛡️ Disable Windows Defender**: Runs a custom script that disables Windows Defender, freeing up system resources and improving performance for certain tasks.

- **🧹 Remove Bloatware**: Automatically uninstalls a variety of pre-installed Microsoft apps and services that are often considered bloatware.

- **👥 Custom User Accounts**: Automatically creates local user accounts with specified administrative and standard privileges.

- **🛠️ Custom First Logon Commands**: Runs scripts during the first logon to further configure the system, such as disabling unnecessary services, managing search indexing, and configuring power settings.

## Bloatware Removed 🧽

The following applications and capabilities are automatically removed during installation:

- Microsoft.Microsoft3DViewer
- Microsoft.BingSearch
- Microsoft.WindowsCalculator
- Microsoft.WindowsCamera
- Clipchamp.Clipchamp
- Microsoft.WindowsAlarms
- Microsoft.Windows.DevHome
- MicrosoftCorporationII.MicrosoftFamily
- Microsoft.WindowsFeedbackHub
- Microsoft.GetHelp
- Microsoft.Getstarted
- Microsoft.WindowsMaps
- Microsoft.MixedReality.Portal
- Microsoft.BingNews
- Microsoft.WindowsNotepad
- Microsoft.Office.OneNote
- Microsoft.OutlookForWindows
- Microsoft.MSPaint
- Microsoft.People
- Microsoft.PowerAutomateDesktop
- MicrosoftCorporationII.QuickAssist
- Microsoft.SkypeApp
- Microsoft.ScreenSketch
- Microsoft.MicrosoftSolitaireCollection
- Microsoft.MicrosoftStickyNotes
- MicrosoftTeams
- MSTeams
- Microsoft.Todos
- Microsoft.WindowsSoundRecorder
- Microsoft.BingWeather
- Microsoft.Xbox.TCUI
- Microsoft.XboxApp
- Microsoft.XboxGameOverlay
- Microsoft.XboxGamingOverlay
- Microsoft.XboxIdentityProvider
- Microsoft.XboxSpeechToTextOverlay
- Microsoft.GamingApp
- Microsoft.YourPhone
- Microsoft.ZuneMusic
- Microsoft.ZuneVideo

## Capabilities Removed 🗑️

- Browser.InternetExplorer
- MathRecognizer
- Microsoft.Windows.MSPaint
- Microsoft.Windows.Notepad
- Microsoft.Windows.PowerShell.ISE
- App.Support.QuickAssist
- Microsoft.Windows.SnippingTool
- Media.WindowsMediaPlayer
- Microsoft.Windows.WordPad

## System Configuration ⚙️

- **AutoLogon Configuration**: Automatically logs in the specified user during the first logon.
- **Power Configuration**: Sets the system power plan to **Ultimate Performance** mode.
- **Service Configuration**: Disables unwanted services like Xbox-related services, Fax, Print Spooler, and more to improve overall system performance.

## How to Use 🔧

1. Clone the repository:
   ```bash
   git clone https://github.com/Deffz-Finesse/Debloated-Windows-11-Install.git
   ```

2. Modify the following sensitive information in the `unattend.xml` file:
   - **Password**: Replace the passwords on lines 541, 549, and 560 with your own passwords.
   - **Username**: Update the username on line 546.
   - **Computer Name**: Update the computer name on line 522.

3. After modifying the file, use this configuration in your Windows setup for a customized installation experience.

## License 📄

This project is open-source and licensed under the MIT License. Feel free to modify and share!

---

Created with ❤️ by Deffz-Finesse.
