
# 🔍 Basic Network Scanner with GUI

A Python-based multithreaded network scanner with a modern **Tkinter** interface. It allows users to scan a range of IP addresses on a local network, check their online status, resolve hostnames, and export the results in multiple formats  (DOCX ).

---

## 📌 Features

- ✅ Ping multiple devices concurrently (using `ThreadPoolExecutor`)
- 💬 Resolve hostnames automatically
- 📋 Display live status in a scrollable text box
- 📁 Export scan results to  `.docx`
- 📡 Real-time timestamp tracking
- 🔊 Sound alerts on scan completion
- 📊 Display scanned device count dynamically
- ⚡ Auto-scroll toggle
- 🪟 Responsive and clean modern GUI

---

## 🛠️ Technologies Used

- **Python 3.x**
- `Tkinter` – for GUI
- `concurrent.futures` – for multithreading
- `socket` – for hostname resolution
- `subprocess` – to execute system pings
- `platform` – to detect OS (Windows/Linux/Mac)
- `winsound` – for alerts (Windows only)
- `docx` – for Word export (`python-docx`)
- `datetime` – for timestamping

---


Install Dependencies:

Install required libraries (if not already installed):

bash
pip install python-docx
Run the Program:

bash
python network_scanner.py



📸 UI Snapshot
![Screenshot 2025-07-06 231342](https://github.com/user-attachments/assets/c5176a94-0a03-4346-a9f0-80cae902a252)


![Screenshot 2025-07-06 231407](https://github.com/user-attachments/assets/156e8ed2-c179-4329-a444-12abce04a22a)


![Screenshot 2025-07-06 231423](https://github.com/user-attachments/assets/41039087-509b-45c8-94a7-6b1d5a97f76c)


![Screenshot 2025-07-06 231539](https://github.com/user-attachments/assets/62a9aff5-a8f1-4ee6-b138-c62788397bb2)


![Screenshot 2025-07-06 231618](https://github.com/user-attachments/assets/3782e214-8d04-487f-a1a7-03d2f9235cdb)


![Screenshot 2025-07-06 231739](https://github.com/user-attachments/assets/1e52df28-96f3-471e-b27b-b0591e03dd46)


📄 Export Options

DOCX: Formatted Word document with colored fonts and structure

![Screenshot 2025-07-06 231801](https://github.com/user-attachments/assets/8bf42432-fc72-470d-8bf4-fe8df17a9ea5)


![Screenshot 2025-07-06 231851](https://github.com/user-attachments/assets/ebf253d1-e08c-4d0b-aa18-0e449c9bd953)

CSV (optional) : Can be added with csv module for spreadsheet exports



⚙️ Customization
Thread Count: Easily adjustable in ThreadPoolExecutor(max_workers=X)

IP Range: User-defined via GUI

Sound Alerts: Use winsound.Beep() or disable for cross-platform compatibility


📌 Future Improvements (Ideas)
Add PDF export with reportlab

Platform-independent sound alerts

Integrated network map visualization

Schedule scan feature

IP and MAC address retrieval



👨‍💻 Author
Arijeet Dey
Cybersecurity & Networking Projects | Python Developer




---



I can also generate a `requirements.txt` file for you if needed.
