# Aircrack-ng-WPA-WPA2-
Drescription: I will be showing how to crack WPA/WPA2 networks which use pre shared keys(psk).
In this section I will be using wireshark and aircrack-ng in kali linux. 




![image](https://github.com/user-attachments/assets/3aef9eab-d75d-47b6-84fa-d924df7bfc61)             ![image](https://github.com/user-attachments/assets/814724d9-641c-4470-9030-3d86f6c5de8f)






WPA/WPA2 networks




WPA/WPA2 networks use pre-shared keys and aircrack-ng can only crack
pre-shared keys. 



what is WPA 


WPA(Wi-Fi protected access) is imporved data encryption compared to WEP.



what is WPA2



WPA2 networks are more secure and are what most people use for there networks as well. WPA2 networks provide stronger data protection and network access control. As well WPA2 supports AES(Advanced Encryption Standard) encryption, wich is more secure tham TKIP.



Equitment used

-> TPLink Router

-> Kali linux

-> wireshark

-> aircrack-ng

-> long range usb adapter(ALFA)



Example attack on a WPA/WPA2 network


before you do the following make sure you enable monitor mode

Im using wireshark as a sniffer to sniff the network tarffic on
the TPLink router. As well im first going to start up aircrack-ng
and start up the wlan.



![image](https://github.com/user-attachments/assets/29eeae14-39c1-406a-838c-4970b998469e)



The one im using is wlan0mon, make sure you enable the monitor mode
and type check-kill to kill other processes.


![image](https://github.com/user-attachments/assets/c32a0809-0c72-4efe-b720-fdfdccd92c97)






Now we need to scann the networks around us to see the wireless traffic in the area. This command allows us to see the network names in our area and the mac addresses of where thats coming from.

BSSID: Mac address


SSID: Network name


ch: channle number the networks on


psk: pre shared key


encryption: it also tells us the encryption type






![image](https://github.com/user-attachments/assets/b2efab32-9ea2-4f27-8fef-ccccaf20d474)



once thats done and you find your network that you are on then
you can use this command to collect the authentication handshake. The purpose of this is to capture the 4-way authentication handshake for the network we are intrestend in.


Now im going to open up wireshark and type 'eapol' in the top search bar in wireshark. Eapol is 



there are two things that you should see...


first is the 4-wayhanshake in the terminal.




![image](https://github.com/user-attachments/assets/9fa0228c-14f1-4360-bef0-a994e73b0b1b)




Second is to make sure at least one device is connected to the specified network and to make sure that the eapol command works like this...



![image](https://github.com/user-attachments/assets/bc6988be-b47e-4be3-8c70-4b3e1967af5e)




















































































