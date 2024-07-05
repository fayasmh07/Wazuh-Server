<h1>
<p align="center">
  Wazuh - Intrusion Detection System
</p>
</h1>

![wazuh-standard-featured-picture](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/ee9c97a3-b5dc-466d-bd3c-a026f7e50bea)

<p align="center">
Wazuh is an open-source security platform that provides comprehensive intrusion detection system (IDS) capabilities by monitoring systems, networks, and applications for suspicious activity and potential threats.
</p>

![wazuh-dashboard-wide](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/2eede27b-0af1-442b-8618-3c04b0e181d3)

# Setting Up Wazuh System
Setting up Wazuh IDS contains mainly 2 parts :
1. Wazuh Server
2. Wazuh Agent

The **Wazuh Server** acts as the central management and processing hub, collecting, analyzing, and storing security data from various sources, including Wazuh agents and external logs, to provide comprehensive threat detection and response capabilities.

**Wazuh Agents** are lightweight, deployed on endpoint devices, and tasked with collecting and forwarding local logs, system metrics, and security events to the Wazuh server for centralized analysis and alerting.

# Implemneting Wazuh Server
1. For setting up the server its better to use Wazuh Assistant in an Linux Based Operating system than using Wazuh OVA Virtual Machine.

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/03266635-e4b4-4255-b858-0035eaa48463)
 
 - You can choose any of the above Operating System
 - I choose <a href="https://ubuntu.com/download/desktop">Ubuntu</a> for this.
 - Its open-source, also easy to manage as a wazuh server.

&nbsp;

2. Setup the Ubuntu Virtual machine 

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/a25a56d4-8066-48e4-8ef5-c764aaf8f4fd)

&nbsp;

3. Open a `Terminal` and paste this code below :

`sudo curl -sO https://packages.wazuh.com/4.8/wazuh-install.sh && sudo bash ./wazuh-install.sh -a`
- It downloads and installs the WAZUH server config files in your system.
- Also after the installation process I got the username and password for the Wazuh Server Dashboard.
- By using my **Ubuntu** system IP address (private IP) I could get get into the Wazuh Dashboard.

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/d3b46afe-c3a9-4255-827d-03abd54bdfc9)




