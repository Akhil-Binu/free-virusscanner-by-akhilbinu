# 🛡️ Terminal Antivirus & Threat Scanner (VirusTotal API)

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![API: VirusTotal](https://img.shields.io/badge/Threat%20Intel-VirusTotal%20v3-3949AB.svg?style=for-the-badge&logo=virustotal&logoColor=white)](https://www.virustotal.com/)
[![CLI: Colorama](https://img.shields.io/badge/CLI-PyFiglet%20%26%20Colorama-magenta.svg?style=for-the-badge)](#features)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

<p align="center">
  <b>A lightweight, cross-platform security CLI scanner that calculates cryptographic file digests (SHA-1, SHA-256) and performs real-time threat intelligence queries across 70+ antivirus engines via VirusTotal.</b>
</p>

</div>

---

## 📌 Overview

**Terminal Antivirus Scanner** provides instant malware verification for suspicious files without uploading sensitive payloads across arbitrary web forms. By hashing target binaries locally using chunked memory-efficient buffers, the scanner verifies the file's digital fingerprint against VirusTotal's global malware intelligence database.

---

## ✨ Features

- 🔐 **Local Hash Computation**: Calculates SHA-1 and SHA-256 hashes using 64KB chunked buffers, accommodating large binaries without RAM exhaustion.
- 🌐 **VirusTotal Integration**: Queries over 70 premier antivirus engines (Kaspersky, CrowdStrike, Microsoft Defender, BitDefender, etc.).
- 💻 **Cross-Platform Compatibility**: Fully functional across Linux, Windows, and macOS environments.
- 🎨 **Visual Terminal Interface**: Styled terminal output featuring dynamic ASCII banners and color-coded threat statuses.

---

## 📸 Detection Screenshots

<div align="center">

### Malicious File Identified
![Virus Detected](results%20screenshot/detected.png)

### Clean File Verified
![Clean File](results%20screenshot/not%20detected.png)

</div>

---

## 🛠️ Installation & Setup

### 1. Clone & Set Up Environment
```bash
git clone https://github.com/Akhil-Binu/free-virusscanner-by-akhilbinu.git
cd free-virusscanner-by-akhilbinu

# Create and activate virtual environment
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Configure Your VirusTotal API Key
1. Obtain a free API key from [VirusTotal Community](https://www.virustotal.com/).
2. When launching the scanner for the first time, input your API key when prompted, or create a `.env` / `VirusTotal_APIKey.txt` file:

```bash
# Add your key (ensure this file is added to .gitignore)
echo "YOUR_VIRUSTOTAL_API_KEY" > VirusTotal_APIKey.txt
```

---

## 🚀 Usage

Run the scanner in your terminal:

```bash
python virus-scanner.py
```

Enter the full or relative path to any suspicious executable, archive, document, or script to inspect its security posture.

---

## ⚠️ Security Notice: Credential Safety

> [!CAUTION]
> Never commit active API keys, secrets, or production tokens to public GitHub repositories. Always include `VirusTotal_APIKey.txt` and `.env` in your `.gitignore` file. If a key is accidentally committed, immediately revoke and regenerate it via the [VirusTotal User Settings](https://www.virustotal.com/gui/user).

---

## 📄 License

Distributed under the [MIT License](LICENSE). Developed by [Akhil Binu](https://akhilbinu.in/).
