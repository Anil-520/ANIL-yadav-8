# ANIL-yadav-8
Identify and Remove Suspicious Browser Extesion 

       Antivirus Installation & System Scan

Intern: Your Name  
Batch: Elevate Lab Internship  

## 📖 Description
This task was about installing antivirus software, scanning the system for threats, and documenting the results. It helps in protecting the computer from malware, viruses, and security risks.

## 📂 Files in this Repo
- `Task6_Antivirus_Report.md` → Detailed explanation of the task  
- `scan_script.py` → Example Python script for file scanning (optional learning)  

## ✅ Outcome
- Antivirus installed successfully  
- Full system scan completed  
- Threats removed/quarantined (if any)

     Antivirus Installation & System Scan

## 🛠 Objective
To install antivirus software, perform a full system scan, and ensure the computer is free from threats.

## 🔎 Steps
1. Downloaded and installed **[Antivirus Name: Windows Defender / Avast / Quick Heal]**.  
2. Updated antivirus definitions.  
3. Performed a **Quick Scan** first.  
4. Performed a **Full Scan** of the system.  
5. Checked the report for detected threats.  
6. Removed/quarantined malicious files if found.  

## 📸 Screenshots
- Before scan screenshot (Dashboard)  
- After scan screenshot (Results)  

## ❓ Interview Q&A
**Q1:** Why is antivirus important?  
**A1:** To detect and remove malware that can steal data or harm the system.  

**Q2:** What’s the difference between quick scan and full scan?  
**A2:** Quick scan checks common infection areas, full scan checks the entire system.  

**Q3:** Can antivirus detect all threats?  
**A3:** No, but it reduces risks significantly.  

**Q4:** What is real-time protection?  
**A4:** Continuous monitoring that blocks malware as soon as it appears.  

## ✅ Outcome
System scan completed successfully, no major threats found. Gained practical knowledge of antivirus usage and system protection.


import os

Define suspicious file extensions (for demo)
suspicious_ext = [".exe", ".bat", ".vbs", ".scr"]

def scan_directory(path):
    print(f"Scanning directory: {path}\n")
    for root, dirs, files in os.walk(path):
        for file in files:
            if file.lower().endswith(tuple(suspicious_ext)):
                print(f"[!] Suspicious file found: {os.path.join(root, file)}")
    print("\n✅ Scan complete!")

# Example: scan current folder
scan_directory(".")

