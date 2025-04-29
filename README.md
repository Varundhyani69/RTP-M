# 🖥️ Process & System Monitor (Python)

A simple Python script that monitors **CPU** and **Memory** usage of specific desktop applications (like Chrome, VS Code, Postman, Premiere Pro, etc.) along with full system stats and running processes.

---

## 📌 Features

- ✅ Tracks usage of specific apps (`chrome.exe`, `code.exe`, `python.exe`, etc.)
- ✅ Aggregates CPU & Memory usage across multiple instances of the same app
- ✅ Shows full system stats:
  - Total RAM
  - Used RAM
  - Total CPU Usage
- ✅ Lists all active processes with individual usage
- ✅ Outputs everything in clean **JSON format**

---

## 🧠 Tech Stack

- [`psutil`](https://pypi.org/project/psutil/) – For system and process monitoring
- `json` – To serialize output
- `sys` – For flushing output
- `time` – For interval-based CPU calculations

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/process-monitor
cd process-monitor

2. Install required Python packages
pip install psutil

3. Run the monitor script
python monitor.py

This will print system stats and process data in JSON format.
{
  "apps": [
    {
      "name": "chrome.exe",
      "cpu": 3.24,
      "memory": 210.56,
      "instances": 4
    },
    {
      "name": "code.exe",
      "cpu": 1.55,
      "memory": 180.23,
      "instances": 1
    }
  ],
  "totalMemoryUsed": 390.79,
  "totalCpuUsed": 4.79,
  "allProcesses": [
    {
      "name": "chrome.exe",
      "pid": 1234,
      "cpu": 0.5,
      "memory": 52.1
    }
    // ... more processes
  ],
  "systemStats": {
    "totalCpuUsage": 27.4,
    "totalMemory": 15.92,
    "usedMemory": 9.45
  }
}
Edit the following list inside monitor.py to monitor different applications:
app_names = [
    "chrome.exe",
    "node.exe",
    "code.exe",
    "python.exe",
    "postman.exe",
    "slack.exe",
    "adobe premiere pro.exe",
    "afterfx.exe"
]

Clean Output
You can use this script's output in:

Node.js apps using child_process.spawn

Logging tools

Dashboards or APIs




