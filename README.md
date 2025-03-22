# Hacking-misconfigured-IoT-devices-

## Project Summary:
in this practical we will demonstrate IoT (Internet of Things) devices that are 
misconfigured or using default credentials and exposed to the outside network. 

## Step:1
Use Angry IP Scanner to identify Raspberry Pi IoT (Internet of Things) devices .
![Screenshot 2025-03-21 181011](https://github.com/user-attachments/assets/487d5f3d-1e04-407c-ba35-392bd02df3bb)

## Step:2 
Open the target IP address in a browser and determine if there is a possibility to gain control over the device.



![Screenshot 2025-03-21 182021](https://github.com/user-attachments/assets/9e35ffc3-7693-418f-adc3-05b3b7089c23)


## Step:3 
We can navigate to the /admin directory to access the admin panel.
![Screenshot 2025-03-21 182044](https://github.com/user-attachments/assets/77361d4d-0b54-4f42-8bd8-dc981775538e)

  ● Login with default credentials, to gain unauthorized access which allows us to 
perform several operations remotely. 

## Step:4 
By taking advantage of the forgot password option, we can even reset the 
password for that device

![Screenshot 2025-03-21 224353](https://github.com/user-attachments/assets/00520d6b-1219-41ef-bb74-aad849cec0ad)



## Step:5 
As shown in the above image, we can execute a simple command on the 
terminal to reset the password. To gain terminal access of target device, perform Nmap 
scan to identify the open ports.

![Screenshot 2025-03-21 182640](https://github.com/user-attachments/assets/9333fc16-79ab-43e5-832e-3eccb0927e3e)

## Step:6 
From the above scan results, we observed that the target is running ssh on port 
22 (open port). Now, let us search for default passwords for ssh service. If target 
configured default settings, we can log into ssh service remotely. 
Using the default password, I log into the system and then execute the                           
sudo pihole -a -p                                                                
command to reset the pi-hole password. 
![Screenshot 2025-03-21 183220](https://github.com/user-attachments/assets/e880ad0c-0264-4465-9c10-ed3cbf906c4d)


## Step:7 
We can use the new password to login to the pi-hole web interface.

![Screenshot 2025-03-21 183336 1](https://github.com/user-attachments/assets/58d6ccce-f6c6-4672-82ff-11bd0b7401a3)

## Step:8 
Now, we can observe that we have more control over the target IoT device. 

![Screenshot 2025-03-21 183730](https://github.com/user-attachments/assets/be591c1c-0cd3-4785-9b63-32f49b85f6e3)


● In this way, we can compromise the security misconfiguration of an IoT system to 
take complete control over the IoT device as well as the associated devices.








