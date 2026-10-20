# Wazuh SIEM VM

Desployed a Wazuh SIEM VM to contralize logs and detect vulnerabilities in my homelab.

## Architecture and Technologies
* OS/evironment: Amazon linux, Virtualbox VM
* Core Software: Virtualbox
* Networking: Static Tailscale VPN address
 
 ## prereqs. and installation

 for requirements and setup, visit this link:
 https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html

 to install virtualbox, use your distros repositories and package manager, or use the download page:
 https://www.virtualbox.org/

 ### Deploying an agent

 Before Wazuh can start monitoring devices, that device must have a working agent installed on it.

 To obtain the install script, go to the agent summary menu in the wazuh dashboard, and select the option
 to deploy a new agent. You will be prompted to give the OS, the IP to the wazuh server/VM, and other
 infromation. After giving it said information, copy the script and paste it into the target device to
 install and start the agent, then reboot both devices.

 ## Testing and verification

 Verified alert generation in wazuh dashboard, triggered alert events.

 ## Key learnings and challenges

 Due to the specified Iptable configs made when you install the VM service, you may have to edit the iptable
 configs to accept any tailscale addresses.

