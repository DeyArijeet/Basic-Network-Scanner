# Basic-Network-Scanner
A Python-based multithreaded network scanner with a modern Tkinter GUI. Scan IP ranges, detect active devices, resolve hostnames, and export results to  DOCX. Features real-time updates, sound alerts, timestamps, and a responsive, interactive interface. Great for learning Python networking.



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



📄 Export Options

DOCX: Formatted Word document with colored fonts and structure

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

📚 License
This project is licensed under the MIT License.

👨‍💻 Author
Arijeet Dey
Cybersecurity & Networking Projects | Python Developer




---

Let me know if you'd like me to add:
- Your GitHub repo link
- Screenshot placeholders
- Specific command-line usage examples
- PDF/CSV export code updates (if implemented)

I can also generate a `requirements.txt` file for you if needed.
