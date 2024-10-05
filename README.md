
# 🚀 Windows Unattended Setup Configuration

This project contains an unattended XML file for automating Windows installations. The file has been optimized to include customization of settings, bypassing certain system checks, removing bloatware, and setting up default user accounts.

## ✨ Features

- **Bypass Hardware Checks:** Automatically bypass TPM, Secure Boot, and RAM checks during installation.
- **Disable Windows Defender:** Runs a custom script to disable Windows Defender during installation.
- **Remove Bloatware:** Removes several built-in apps like Xbox, Skype, and others via PowerShell scripts.
- **Custom User Accounts:** Automatically creates specified local user accounts with administrative and standard privileges.
- **Custom First Logon Commands:** Runs scripts for additional configurations like disabling services, managing search indexing, and setting the power plan.

## 📝 How to Use

### 1. **Clone the Repository**
```bash
git clone <repository_url>
```

### 2. **Customize the Unattend File**

The `unattend.xml` file is pre-configured for automation, but certain sensitive details like usernames, passwords, and computer names need to be customized for your environment.

#### 🚨 Important: Change These Values Before Use!

1. **Computer Name** (Line 522)
   - Replace:
     ```xml
     <ComputerName>REPLACE_ME</ComputerName>
     ```

2. **Admin User Password** (Lines 541 and 560)
   - Replace:
     ```xml
     <Value>REPLACE_ME</Value>
     ```

3. **Standard User Account Name & Password** (Lines 546 and 549)
   - Replace:
     ```xml
     <Name>REPLACE_ME</Name>
     <Value>REPLACE_ME</Value>
     ```

### 3. **Run the Setup**

Once the unattend file is updated with your custom values, you can proceed with the Windows installation. The unattended setup will automatically configure the system as per the instructions in the file.

Enjoy your streamlined Windows installation! 😎
