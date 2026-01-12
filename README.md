# Honeypot T-Pot

# 🛡️ T-Pot Honeypot Platform Deployment

A comprehensive, multi-honeypot platform deployed to capture, analyze, and visualize real-time cyber attacks. This project utilizes the **T-Pot Community Edition** to create a high-interaction threat intelligence environment on a cloud-based VPS.

---

## 📝 Overview
This project transforms a standard Ubuntu server into a "threat magnet." By running multiple honeypot services (like **Cowrie**, **Dionaea**, and **Honeytrap**) inside Docker containers, it traps attackers, logs their activities, and provides deep insights into global threat intelligence.

## 🚀 Features
* **Multi-Honeypot Support:** Integrated services for SSH, Telnet, Web, and more.
* **Live Visualization:** Real-time attack tracking via a global "Pew Pew" map.
* **Deep Analysis:** Full ELK Stack (Elasticsearch, Logstash, Kibana) integration.
* **OSINT Tools:** Includes SpiderFoot and CyberChef for incident response.

## 🛠️ Tech Stack
* **OS:** `Ubuntu 24.04 LTS`
* **Platform:** `T-Pot CE`
* **Visualization:** `Kibana`
* **Infrastructure:** `Docker` & `Systemd`

---

## 💻 System Requirements
To ensure stability and performance, the following specs were used:
* **CPU:** 4 vCPUs
* **RAM:** 8GB (Minimum) / 16GB (Recommended)
* **Storage:** 128GB SSD

---

## ⚙️ Installation & Setup

### 1. Update the System
sudo apt-get update && sudo apt-get upgrade -y

### 2. Create a Non-Root User
sudo adduser your-username

sudo usermod -aG sudo your-username

su - your-username

### 3. Clone and Execute Installation

git clone [https://github.com/telekom-security/tpotce](https://github.com/telekom-security/tpotce)
cd tpotce
sudo ./install.sh


📊 Monitoring Dashboards
Kibana: Access hundreds of pre-configured dashboards for attack analysis.

Attack Map: A live, visual representation of incoming threats by country.

CyberChef: The "Cyber Swiss Army Knife" for decoding malicious payloads.


## 🔐 Access Configuration

After installation, T-Pot reconfigures the default ports for security. Use the table below for access:

| Service | Port | Access URL / Command |
| :--- | :--- | :--- |
| **SSH** | `64295` | `ssh -p 64295 user@your_ip` |
| **Web Dashboard** | `64297` | `https://your_ip:64297` |
| **Admin UI** | `64294` | `Cockpit Dashboard` |

> **Important:** Make sure to allow these ports in your Cloud Provider's Firewall (Security Groups).
