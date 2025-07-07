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


![Screenshot 2025-07-06 231618](https://github.com/user-attachments/assets/35679dab-da81-4f54-8020-b36482d657aa)
![Screenshot 2025-07-06 231539](https://github.com/user-attachments/assets/6a6fc7e1-2f0c-409e-af5b-5dd3da0973bf)

IP  NETWORK

![Screenshot 2025-07-06 231407](https://github.com/user-attachments/assets/cd560680-3f50-41bf-8254-ac89441d628e)
![Screenshot 2025-07-06 231423](https://github.com/user-attachments/assets/9c3f44a8-9ce2-433a-a9cc-aa1ff338a4eb)

![Screenshot 2025-07-06 231342](https://github.com/user-attachments/assets/b1e3c56b-86f8-4c85-8089-09121e46b7b1)

![Screenshot 2025-07-06 231739](https://github.com/user-attachments/assets/60f67317-00d0-42b1-b1fc-7f2decec9d0e)

### Flowchart

```mermaid
flowchart TD;
    A[Start Application] --> B[Enter Network Prefix];
    B --> C[Select Number of Devices to Scan];
    C --> D[Enable Options - Hostname / MAC Lookup];
    D --> E[Click Start Scan];
    E --> F{For each IP};
    F -->|Ping| G[Device UP/DOWN];
    G -->|If UP and MAC enabled| H[Parse MAC from ARP];
    H --> I[Display Result in GUI];
    G --> I;
    I --> J{More IPs?};
    J -->|Yes| F ;
    J -->|No| K[Update Progress Bar and Status];
    K --> L[Export Results];
    L --> M[Save Word Report];
    M --> N[End];

```

---

## 🚀 How to Run

### 🪜 Step-by-Step Process

1. ** Download the Project**\
   Download the ZIP or run:

   ```bash
   https://github.com/DeyArijeet/Basic-Network-Scanner.git
   ```

2. **Install Dependencies**\
   Make sure Python is installed (Python 3.6+). Then install the required package:

   ```bash
   pip install python-docx
   ```

3. **Run the Application**\
   Launch the scanner using:

   ```bash
   python network_scanner_mac_gui.py
   ```

4. **Using the GUI**

   - Enter your local network prefix (e.g., `192.168.1`)
   - Select the number of devices to scan
   - Optionally enable hostname and MAC / WINDOWS address lookup
   - Click `Start Scan` to begin
   - Export results with `Export to Word`

---

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

Built for Kali Linux Edition with a Windows/Mac -compatible interface.

---

## 🛠️ Future Improvements

- CSV/PDF export support
- Port scanning functionality
- MAC vendor lookup from IEEE
- Logging to local file automatically
- Executable packaging for Windows/Mac (.exe)

---

## ✅ License

Open-source and free to use. Attribution appreciated.

