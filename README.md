# Defender-TryHackMe
</br>
<img width="853" height="617" alt="image" src="https://github.com/user-attachments/assets/aa26f188-2247-4aef-8456-e602c4a0c560" </br></br></br>

-Start with the incident overview

I see this is a High-severity, active, multi-stage incident involving privilege escalation.


<img width="1882" height="997" alt="image" src="https://github.com/user-attachments/assets/57d3d001-0b7c-4797-bf21-9d69ed59c309" /></br></br>

-Identify the affected entities

Device: vm-evil-xdr
Users: 2 users
External IP: 82.69.34.93
Processes: 8
Files: 59
Registry values: 2

<img width="523" height="492" alt="image" src="https://github.com/user-attachments/assets/bc40abfb-69a5-440c-9dba-5d30d178b848" /></br></br>

-I would then review each of the 21 alerts, starting with the action that established initial access

<img width="1340" height="604" alt="image" src="https://github.com/user-attachments/assets/22dd1cc7-93da-4e8b-a462-737f209bb491" /></br></br>

-An attempt was made to disable Defender antivirus, also looked at the Mitre attack ID for more information regarding this technique **(Mitre ID: T1562.001)**

<img width="1762" height="450" alt="image" src="https://github.com/user-attachments/assets/7af55036-eb93-4970-876f-aa9145ce7f33" /></br>



<img width="1848" height="737" alt="image" src="https://github.com/user-attachments/assets/c970cc4c-886e-4beb-8978-320cb7509a7e" /></br>

-Malcious tool named Meterpreter, was deployed onto the target machine (vm-evil-xdr) via a dynamic link library injection **(Mitre ID: T1055.001)**
</br></br>
<img width="1357" height="225" alt="image" src="https://github.com/user-attachments/assets/aec7c144-fc20-425e-a384-7c825aabe2e0" /></br>

-Attacker was able to bypass UAC prompt/pop up by edigin registry files 

<img width="378" height="109" alt="image" src="https://github.com/user-attachments/assets/d7c43f98-c9e2-4155-81a0-55b95fd88bc0" /></br>

<img width="1840" height="507" alt="image" src="https://github.com/user-attachments/assets/d6eabbd8-b0f1-468f-af5c-7b921dcedec6" /></br>

### Conclusion ###

I have confirmed that this is a true positive. The affected endpoint is vm-evil-xdr, the compromised user account is evil-xdr, privilege escalation occurred, and there were multiple IPs, files and processes involved. The incident contains 21 alerts and Defender has already isolated the device and contained the account. I have documented the timeline and actions taken. This incident therefore will be escalated to L2 for further investigation</br>

Serious indicators of a true positive
-High severity
-Attempted to disable defender
-Meterpreter deployed onto the machine via DLL injection
-UAC pop up was bypassed by configuring Windows Registry 
-There was lateral movement via remote logon that was blocked






