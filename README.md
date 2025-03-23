# 📄 README - Automated Ubuntu Installation

## 📌 About this file
This `autoinstall.yaml` file is a configuration for **automated installation** of Ubuntu, using the **Autoinstall** system available from Ubuntu 20.04 onwards. It allows the system to be installed without manual intervention, applying predefined settings such as language, user, packages, and more.

## 🚀 Configured Features
This file automatically sets up:
- 📌 **User and password**: Creates the `leonardo` user with a predefined password
- 🌍 **Language and timezone**: Sets the system to **Portuguese (Brazil)** and **São Paulo timezone**
- ⌨️ **Keyboard**: Configured for **Brazilian (ABNT2) layout**
- 📦 **Pre-installed packages**:
  - `libreoffice` (Office suite)
  - `gimp` (Image editor)
  - `git` (Version control system)
  - `wget` (Command-line download tool)
- 🔗 **Applications installed via Snap**:
  - **Spotify** (Music streaming)
  - **VS Code** (Code editor)
  - **Brave Browser** (Web browser)
- 🎞️ **Multimedia codecs**: Installation enabled
- 🎛️ **Proprietary drivers**: Installation enabled
- 🔄 **Updates**: Configured to install all available updates
- 🔌 **Automatic reboot** after installation

## 🛠️ How to use this file?
### 1️⃣ Create an HTTP server to host the file
Ubuntu can fetch this file over the network. To do this:
```bash
python3 -m http.server 8000
```
Then, start the installation with:
```bash
autoinstall ds=nocloud-net;s=http://<SERVER-IP>:8000/
```

### 2️⃣ Embed it in a custom ISO
If you want to include this file in an Ubuntu ISO, create a `autoinstall/` directory and add `autoinstall.yaml`.

## ⚠️ Important Note
🔐 **The password is stored in plain text** in the file! For better security, use a SHA-512 hash:
```bash
mkpasswd -m sha-512
```
Then replace the password in the file with the generated hash.

## 📢 Contribution
If you want to add more features or packages, edit the `autoinstall.yaml` file and customize it as needed!



