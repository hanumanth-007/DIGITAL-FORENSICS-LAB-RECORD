# Windows Resource Monitor: Malicious Activity Detection Experiment

---

## 🎯 Aim

To monitor, analyze, and identify suspicious or malicious system behavior on a Windows environment using **Windows Resource Monitor**.

---

## 🧰 Tools & Requirements

| Tool / Resource            | Purpose                                                |
|----------------------------|--------------------------------------------------------|
| **Windows Resource Monitor** | Track resource usage and process behavior              |
| **Windows OS**             | Platform; available in Windows 7 and later             |
| **Administrator Privileges** | Required for system resource visibility                |
| **Internet Connection**    | Research unknown/suspicious processes                  |

---

## ⚙️ Procedure

### Step 1: Launch the Tool

1. Open **Task Manager** (`Ctrl + Shift + Esc`).
2. Go to **Performance** tab.
3. Click **Open Resource Monitor**.
4. Or, run `resmon.exe` from the Run dialog (`Win + R`).



<img width="1223" height="753" alt="506177099-578a5fee-a6d7-4ca3-bf51-757d7f86d1b3" src="https://github.com/user-attachments/assets/fe64863a-cc4a-4de6-946a-99e696951d47" />


---

### Step 2: Explore the Interface

- **Overview**: Summarized performance data.
- **CPU**: Process usage and threads.
- **Memory**: Physical memory allocation.
- **Disk**: File and I/O activity.
- **Network**: Communication endpoints and bandwidth usage.



<img width="1271" height="770" alt="506178434-de02cbd3-e460-4a03-a20c-291bc4a38e4d" src="https://github.com/user-attachments/assets/8ae685a3-01d6-4a7e-a6e3-f49d1160e325" />



---

### Step 3: Identify Suspicious Activity

1. **Unusual CPU usage** – processes using high CPU consistently.
2. **Memory leaks** – processes continuously eating up memory.
3. **Disk usage spikes** – unknown processes with heavy read/write activity.
4. **Network anomalies** – persistent outbound connections from unfamiliar processes.
5. **File location check** – right-click a process → *Open File Location* to verify directory (e.g., `C:\Windows\System32`).

---

### Step 4: Cross-Verify Process Reputation

- Search unknown process names online.
- Use [VirusTotal](https://www.virustotal.com/) or [Hybrid Analysis](https://www.hybrid-analysis.com/).



<img width="1191" height="762" alt="506178705-923e8d6f-8982-477d-8767-2593b91e79e5" src="https://github.com/user-attachments/assets/06ad6de7-7c20-4ac5-88bc-57d156d3a900" />



---

### Step 5: Mitigate Threats

1. **End Task** – right-click → End Process.
2. **Disable Auto-start Entries** – via *System Configuration (msconfig)* or *Startup Apps.*
3. **Virus Scan** – with Windows Defender or trusted anti-malware.



<img width="1246" height="732" alt="506179348-509129b0-a70d-4f35-98e9-8ddc9e978db9" src="https://github.com/user-attachments/assets/c77c7d87-3683-4952-af5e-4a46c482204b" />



---

## 🔍 Observations

| Process Name        | Suspicious Behavior        | Action Taken          |
|---------------------|---------------------------|----------------------|
| tempwatcher.exe     | High disk writes, unknown | Terminated           |
| svchost.exe         | Stable, verified safe     | Monitored            |
| browserassist.exe   | Persistent outbound traffic | Scanned & Quarantined |

---

## 📈 Result

Windows Resource Monitor efficiently detected unusual activities, guiding identification and mitigation of potentially harmful processes.

---

## 📚 Conclusion

Windows Resource Monitor is a reliable native tool for diagnosing system anomalies. Coupled with process verification and antivirus actions, it strengthens system defense and integrity.

---
