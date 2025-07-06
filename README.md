# 🛰️ Basic Network Scanner with MAC Address Lookup

A Python-based graphical network scanning tool that performs device reachability checks (via ping), resolves hostnames, and optionally performs MAC address lookups using the ARP table. Results are displayed in real-time and can be exported to a formatted Word report.

---

## 📌 Features

- 🔍 Scans multiple IP addresses in a given subnet
- 🌐 Optional hostname resolution
- 🧭 Optional MAC address lookup using ARP table
- 📊 Real-time progress bar and device status updates
- 📋 Auto-scroll log area with color-coded output (🟢 UP, 🔴 DOWN)
- 📁 Export scan results to a `.docx` Word file
- 🖱️ Modern GUI with checkboxes, combobox, and status labels

---

## 🧱 GUI Overview

### Screenshot

### Flowchart

graph TD
    A[Start Application] --> B[Enter Network Prefix]
    B --> C[Select Number of Devices to Scan]
    C --> D[Enable Options: Hostname / MAC Lookup]
    D --> E[Click Start Scan]
    E --> F{For each IP}
    F -->|Ping| G[Device UP/DOWN]
    G -->|If UP and MAC enabled| H[Parse MAC from ARP]
    H --> I[Display Result in GUI]
    G --> I
    I --> J{More IPs?}
    J -->|Yes| F
    J -->|No| K[Update Progress Bar & Status]
    K --> L[Export Results (Optional)]
    L --> M[Save Word Report]
    M --> N[End]


---

## 🚀 How to Run

### 🔧 Requirements

Install the dependencies:

```bash
pip install python-docx
```

### ▶️ Run the Application

```bash
python network_scanner_mac_gui.py
```

---

## 📄 Exported Report Example

The exported `.docx` file includes:

- Network prefix
- Number of devices scanned
- Timestamp
- Table with:
  - IP address
  - Hostname (if resolved)
  - Status (🟢 UP / 🔴 DOWN)
  - MAC address (if enabled)

---

## 📂 Project Structure

```
.
├── network_scanner_mac_gui.py     # Main GUI application
├── screenshots/
│   └── network_scanner_gui.png    # Example UI screenshot
├── README.md                      # This documentation
└── requirements.txt               # Dependencies
```

---

## 🧠 Tech Stack

- Python 3.x
- Tkinter (GUI)
- subprocess / socket / platform (system ops)
- `python-docx` (export to Word)

---

## 📌 Author

**Arijeet Dey**

Built for Kali Linux Edition with a Windows-compatible interface.

---

## 🛠️ Future Improvements

- CSV/PDF export support
- Port scanning functionality
- MAC vendor lookup from IEEE
- Logging to local file automatically
- Executable packaging for Windows (.exe)

---

## ✅ License

Open-source and free to use. Attribution appreciated.

