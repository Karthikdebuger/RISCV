# ⚡ OpenLane Installation Guide

<div align="center">

![OpenLane](https://img.shields.io/badge/OpenLane-RTL%20to%20GDSII-purple?style=for-the-badge&logo=chip)
![Docker](https://img.shields.io/badge/Docker-Containerized-darkblue?style=for-the-badge&logo=docker)
![Ubuntu](https://img.shields.io/badge/Ubuntu-WSL%20Ready-brown?style=for-the-badge&logo=ubuntu)

</div>

This guide provides step-by-step instructions to install Docker and OpenLane on an Ubuntu-based system running under WSL (Windows Subsystem for Linux).

<div align="center">

🐧 Linux Setup → 🐋 Docker Engine → 🏗️ OpenLane Build → 🚀 Design Ready


</div>

---

## 🐧 **Install WSL and Ubuntu (for Windows Users)**

<details>
<summary><b>Skip this step if you're already using native Ubuntu or Linux.</b></summary>

This section is specifically for Windows users who need to set up a Linux environment for OpenLane development.

</details>

### **Step 1: Enable WSL**
1. Open **PowerShell as Administrator** and run:
    ```powershell
    wsl --install
    ```

### **Step 2: Complete Setup**
2. Restart your system when prompted.  
3. Once installed, open **Ubuntu** from the Start Menu and complete the setup (username, password, etc.).  
4. Update your package list:
    ```bash
    sudo apt-get update
    sudo apt-get upgrade
    ```

<div align="center">

✅ **WSL and Ubuntu Setup Done**

</div>

---

## 🐋 **Installing Docker**

<details>
<summary><b>Purpose:</b> Docker provides containerized environment for OpenLane tools.</summary>

Docker ensures consistent tool behavior across different systems and simplifies the installation process.

</details>

### **Step 1: Set Up Docker Repository**
```bash
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

Add Docker's official repository:
```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo \"$VERSION_CODENAME\") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
Step 2: Install Docker Engine
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
Step 3: Verify Installation

Run the test image:
```bash
sudo docker run hello-world
```
<div align="center">

🎉 Docker Installed Successfully

</div>

🔑 Fixing Docker Permissions
<details> <summary><b>Important:</b> Required if you encounter "permission denied" errors.</summary>

This step allows running Docker commands without sudo, which is essential for OpenLane operation.

</details>

If you encounter a "permission denied" error related to Docker socket access:

Add Your User to the Docker Group
```bash
# Create the docker group (if it doesn't exist)
sudo groupadd docker

# Add your user to the docker group
sudo usermod -aG docker $USER

# Log out and back in for group changes to take effect
```
💡 Tip: After running these commands, you need to log out and back in, or restart your terminal session.

<div align="center">

🔓 Docker Permissions Fixed

</div>
🏗️ Installing OpenLane
<details> <summary><b>Purpose:</b> Complete RTL-to-GDSII automated flow for digital ASIC design.</summary>

OpenLane is an automated RTL to GDSII flow that includes synthesis, placement, routing, and physical verification.

</details>
Step 1: Verify Prerequisites
| Tool           | Purpose              | Check Command              |
| -------------- | -------------------- | -------------------------- |
| 🌀 **Git**     | Version control      | `git --version`            |
| 🐋 **Docker**  | Containerization     | `docker --version`         |
| 🐍 **Python3** | Scripting            | `python3 --version`        |
| 📦 **Pip**     | Package manager      | `python3 -m pip --version` |
| ⚙️ **Make**    | Build automation     | `make --version`           |
| 📂 **Venv**    | Virtual environments | `python3 -m venv -h`       |

</div>

Ensure the following tools are installed:
```bash
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
python3 -m venv -h
```
Step 2: Update & Install Required Packages
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip python3-tk curl make git
```
Step 3: Clone and Build OpenLane
```bash
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test
```
<div align="center">

✅ OpenLane Installed Successfully

</div>
<div align="center">


## 🎉 **Installation Complete!**

### **Verification Commands**

```bash
# Test Docker
docker --version

# Test OpenLane
cd $HOME/OpenLane
make test
```

| Component | Status | Version Check |
|-----------|--------|---------------|
| 🐧 **WSL/Ubuntu** | ✅ Ready | `lsb_release -a` |
| 🐳 **Docker** | ✅ Ready | `docker --version` |
| 🧰 **OpenLane** | ✅ Ready | `cd OpenLane && make test` |

### 🚀 **Ready for RTL-to-GDSII Flow!**

</div>

---

</div>


