# Installation Steps

## 📌 Objective

To set up Wazuh Manager and Agent for security monitoring.

---

## 🖥️ System Setup

* Wazuh Manager: Ubuntu Server
* Wazuh Agent: Kali Linux

---

## 🔧 Step 1: Install Wazuh Manager (Ubuntu)

1. Update system:

   ```
   sudo apt update && sudo apt upgrade -y
   ```

2. Install Wazuh:

   ```
   curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
   sudo bash wazuh-install.sh -a
   ```

3. Access dashboard using browser:

   ```
   https://<server-ip>
   ```

---

## 🔧 Step 2: Install Wazuh Agent (Kali)

1. Download agent package:

   ```
   wget https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.7.5-1_amd64.deb
   ```

2. Install agent:

   ```
   sudo dpkg -i wazuh-agent_4.7.5-1_amd64.deb
   ```

3. Configure manager IP:

   * Edit `/var/ossec/etc/ossec.conf`
   * Add manager IP address

---

## 🔄 Step 3: Start Agent

```
sudo systemctl daemon-reload
sudo systemctl enable wazuh-agent
sudo systemctl start wazuh-agent
```

---

## 🔍 Step 4: Verify Connection

* Login to Wazuh Dashboard
* Navigate to "Agents"
* Check if agent is active

---

## 🛠️ Step 5: Enable File Integrity Monitoring

* Modify `ossec.conf`
* Add directories:

  ```
  /etc
  /home
  ```

---

## 🔐 Step 6: Simulate Attacks

* SSH brute-force:

  ```
  ssh fakeuser@localhost
  ```

* File changes:

  ```
  echo "test" >> /home/kali/test.txt
  ```

---

## 📌 Conclusion

The Wazuh Manager and Agent were successfully installed and configured, enabling real-time monitoring and detection of security events.
