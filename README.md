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



<img width="1848" height="737" alt="image" src="https://github.com/user-attachments/assets/c970cc4c-886e-4beb-8978-320cb7509a7e" />

-Malcious tool named Meterpreter, was deployed onto the target machine (vm-evil-xdr) via a dynamic link library injection **(Mitre ID: T1055.001)**




