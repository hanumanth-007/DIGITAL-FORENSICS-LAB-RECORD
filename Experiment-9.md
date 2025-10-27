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

---

### Step 2: Explore the Interface

- **Overview**: Summarized performance data.
- **CPU**: Process usage and threads.
- **Memory**: Physical memory allocation.
- **Disk**: File and I/O activity.
- **Network**: Communication endpoints and bandwidth usage.

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

---

### Step 5: Mitigate Threats

1. **End Task** – right-click → End Process.
2. **Disable Auto-start Entries** – via *System Configuration (msconfig)* or *Startup Apps.*
3. **Virus Scan** – with Windows Defender or trusted anti-malware.

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
