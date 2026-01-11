# XOR Shellcode Encryptor (AI-Assisted Educational Project)

> **Note:** This project was created for educational purposes with the assistance of AI (ChatGPT). It demonstrates basic XOR-based obfuscation techniques commonly used in security research, red teaming, and loader development. Do not use it for malicious purposes.

---

## 📌 Overview

This tool reads raw shellcode from a file, XOR-encrypts it with a user-provided key, and outputs the encrypted version in multiple formats:

- `raw` (binary file)
- `python` (Python byte array)
- `c` (C-style unsigned char array)

This mirrors how real-world red teamers and malware researchers obfuscate payloads before a loader decrypts them in memory.

---

## 🎯 Features

✔ Reads raw shellcode from file  
✔ XOR encryption with 1-byte or string key  
✔ Supports multiple output formats (raw, Python, C)  
✔ Built using `argparse`  
✔ Fully CLI‑based  
✔ Simple and educational  
✔ AI‑assisted development  

---

## ⚙ Requirements

Only Python 3 is needed.

Optional virtual environment installation:

```bash
python3 -m venv venv
source venv/bin/activate


/
├── xorcrypt.py
├── raw.bin
├── encrypted.bin
├── encrypted.py
├── encrypted.h
├── requirements.txt (optional)
└── README.md

Generating Shellcode Example
msfvenom -p windows/exec CMD=calc.exe -f raw -o raw.bin

Usage Instructions 
python3 xorcrypt.py --in INPUT_FILE --out OUTPUT_FILE --key KEY --format FORMAT

Example Raw Encrypted Binary
python3 xorcrypt.py --in raw.bin --out encrypted.bin --key 0x42 --format raw
Output Python Array
python3 xorcrypt.py --in raw.bin --out encrypted.py --key 0x42 --format python

Output C-Array
python3 xorcrypt.py --in raw.bin --out encrypted.h --key 0x42 --format c


⚠ Legal & Ethical Disclaimer

This tool is for educational and research purposes only. Do not use on systems you do not own or have explicit permission to test.

