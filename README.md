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
 - I choose <a href="https://ubuntu.com/download/desktop">Ubuntu 22.04</a> for this.
 - Its open-source, light-weight, also easy to manage as a wazuh server.

&nbsp;

2. Setup the Ubuntu Virtual machine 

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/baec5bcc-bc21-4a6b-9b68-a201c2d8267c)

&nbsp;

3. Open a `Terminal` and paste this code below :

`sudo curl -sO https://packages.wazuh.com/4.8/wazuh-install.sh && sudo bash ./wazuh-install.sh -a`
- It downloads and installs the WAZUH server config files in your system.
- Also after the installation process I got the username and password for the Wazuh Server Dashboard.
- By using my **Ubuntu** system IP address (private IP) I could get get into the Wazuh Dashboard.

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/6ee1990f-79a4-4df5-83e8-e289217fe338)

&nbsp;

# Implementing Wazuh Agents (Endpoints)
### On Linux
1. Access the  Wazuh Dashboard 

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/2e71583f-ca3a-4b90-b8da-afb36ab2c7d2)

2. Click the Add Agent link to add a new endpoint device for monitoring

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/af0df359-00a3-4611-84a1-0528443f9d1b)

3. Here I'm selecting the DEBIAN amd64 for my Kali Linux laptop & setting the IP address of my ubuntu system (wazuh server).

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/d9a12e41-01d7-4d0c-804c-e594d725f6dc)

4. After setting up my agent name and group, i got the bash commands to install Wazuh Agent in my Kali Linux Laptop.

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/1b461eb5-0886-47d0-96ee-57b07095d947)

5. After providing the commands, Wazuh Agent starts to run in my Linux Distro

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/8f98e81d-b049-4275-b3d0-e68749b49db1)

6. Now the endpoint has been added to the server.

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/a2f894bf-79a1-4e38-9371-8ff435d884fc)

&nbsp;

### On Windows
1. Access the Wazuh Dashboard

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/aefa67ef-0561-49d9-a5a4-62a3475a4b74)

2. click on the Add New Agent

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/af0df359-00a3-4611-84a1-0528443f9d1b)

3. I need to install the Wazuh Agent on the Windows, so im selecting the Windows version

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/54863751-bc0f-4b2e-b3f1-378300710eae)

4. Now giving the Agent name and group, After that I get the commands to start Wazuh Agent in Windows.

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/ee42824c-e803-4eb7-9723-7136c7559d95)

5. copy the commands and paste in the windows powershell (Powershell should be run as **administrator**

![Screenshot 2024-07-09 115437](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/4972798b-5899-4469-b973-c3512bb2cc2e)

![Screenshot 2024-07-09 115512](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/4961dc21-3e92-48fa-ad2a-ca2954347644)

6. After that my Windows system has been added to the Wazuh IDS.

![image](https://github.com/fayasmh07/Wazuh-Server/assets/97302873/21b74056-091d-4c43-a20e-5ffc870807ef)











