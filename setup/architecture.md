# Project Architecture

## 📌 Overview

This project is based on a Security Operations Center (SOC) architecture using Wazuh. It follows a centralized monitoring approach where a manager collects and analyzes logs from multiple agents.

---

## 🧱 Components

### 1. Wazuh Manager (Ubuntu Server)

* Acts as the central system
* Collects logs from agents
* Analyzes security events
* Generates alerts
* Provides dashboard visualization

---

### 2. Wazuh Agent (Kali Linux)

* Installed on endpoint system
* Monitors system activities
* Performs File Integrity Monitoring (FIM)
* Sends logs to Wazuh Manager

---

### 3. Wazuh Dashboard (Web Interface)

* Used to visualize alerts
* Displays security events
* Provides filtering and analysis features

---

## 🔄 Data Flow

1. Agent monitors system activity (file changes, login attempts)
2. Logs are generated on the agent
3. Logs are sent to the Wazuh Manager
4. Manager analyzes logs using rules
5. Alerts are generated
6. Alerts are displayed on dashboard

---

## 🖥️ Architecture Diagram (Description)

Kali Linux (Agent) → Ubuntu Server (Wazuh Manager) → Dashboard (Web UI)

---

## 🎯 Key Features

* Centralized log monitoring
* Real-time threat detection
* File Integrity Monitoring (FIM)
* SSH brute-force detection
* MITRE ATT&CK mapping

---

## 📌 Conclusion

The architecture demonstrates a basic SOC setup where multiple endpoints are monitored centrally using Wazuh, enabling efficient detection and analysis of security threats.
