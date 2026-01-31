# -Windows-Registry-Forensics-Analysis
This project focuses on analyzing Windows Registry artifacts to identify user activity, system information, External Devices/USB device forensics and forensic evidence using Registry Explorer. The aim is to understand how registry keys help in digital investigations.
## 📌 Project Overview
This project focuses on **Windows Registry Forensics**, which is a critical part of
Digital Forensics and Incident Response (DFIR).  
The Windows Registry stores configuration data, user activity, system information,
and software details. By analyzing registry hives, investigators can reconstruct
user actions and system behavior.

This project demonstrates **hands-on registry analysis** using forensic tools
and explains important registry keys used in investigations.

---

## 🎯 Objectives of the Project
- Understand the structure of the Windows Registry
- Learn the purpose of major registry hives
- Identify forensic artifacts from registry keys
- Analyze user activity, system configuration, and startup programs
- Build strong fundamentals for SOC and Digital Forensics roles

---

## 🧠 What is Windows Registry? (Detailed Explanation)

The **Windows Registry** is a **hierarchical database** used by the Windows operating
system to store low-level settings for:

- Operating system
- Hardware devices
- Installed software
- User profiles
- System services
- Startup programs

Windows continuously reads and writes data to the registry while the system is running.

👉 In simple words:  
**Registry = Brain of Windows OS**

---

## 🗂️ Windows Registry Structure

The registry is organized into **Keys**, **Subkeys**, and **Values**:

- **Key** → Like a folder  
- **Subkey** → Folder inside a folder  
- **Value** → Actual data (name, type, data)

Example:
HKLM\Software\Microsoft\Windows NT\CurrentVersion


---

## 🧩 Major Registry Hives (Very Important)

### 1️⃣ HKEY_LOCAL_MACHINE (HKLM)
- Stores system-wide configuration
- Applies to all users
- Common forensic artifacts:
  - OS version
  - Installed software
  - System services
  - Startup programs

📍 Physical hive file:
C:\Windows\System32\Config\SOFTWARE
C:\Windows\System32\Config\SYSTEM


---

### 2️⃣ HKEY_CURRENT_USER (HKCU)
- Stores settings for the currently logged-in user
- User activity and preferences
- Extremely useful in investigations

📍 Physical hive file:
NTUSER.DAT


---

### 3️⃣ HKEY_USERS (HKU)
- Contains registry data for all user profiles
- Each user has a unique SID

---

### 4️⃣ HKEY_CLASSES_ROOT (HKCR)
- File associations
- Helps identify how files are opened

---

## 🧪 Important Registry Keys for Forensics

### 🔹 OS Information
![UserAssist Evidence](OS-Versiion.png)

HKLM\Software\Microsoft\Windows NT\CurrentVersion

Used to find:
- Windows version
- Build number
- Install date
- Registered owner

---

### 🔹 Startup Programs (Persistence)
HKCU\Software\Microsoft\Windows\CurrentVersion\Run
HKLM\Software\Microsoft\Windows\CurrentVersion\Run

Used to detect:
- Malware persistence
- Suspicious startup entries

---

### 🔹 Installed Software
HKLM\Software\Microsoft\Windows\CurrentVersion\Uninstall

Used to find:
- Installed applications
- Installation dates
- Software publisher

---

### 🔹 User Activity (Recent Files)
HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs

Used to track:
- Recently opened files
- User interaction timeline

---

### 🔹 USB Device History
HKLM\SYSTEM\CurrentControlSet\Enum\USBSTOR

Used to identify:
- USB devices connected
- Device serial numbers
- First and last connection time

---

## 🛠️ Tools Used
- Registry Explorer
- FTK Imager
- Autopsy
- Windows OS
- GitHub

---

## 🔍 Project Workflow
1. Collected registry hive files (SAM, SYSTEM, SOFTWARE, NTUSER.DAT)
2. Loaded hives into Registry Explorer
3. Navigated key forensic registry paths
4. Extracted user and system artifacts
5. Documented findings with explanations
6. Created this GitHub project for learning and demonstration

---

## 📊 Key Findings
- Identified OS version and installation details
- Extracted user activity artifacts
- Detected startup and persistence entries
- Analyzed installed software evidence
- Understood registry-based investigation techniques

---

## 📚 Learning Outcome
- Strong understanding of Windows Registry structure
- Practical experience with registry forensic analysis
- Improved DFIR and SOC investigation skills
- Better understanding of how malware uses registry keys
- Confidence in explaining registry artifacts in interviews

---

## 👤 Author
**Ananya Arya**  
Cyber Security | SOC & Digital Forensics Enthusiast  
Windows Forensics | OSINT | Incident Response
