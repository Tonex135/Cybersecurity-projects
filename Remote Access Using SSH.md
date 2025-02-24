Remotely accessed Kali Linux through Windows OS

# Objective
This project aims to enable secure and efficient remote access to Kali Linux from a Windows OS using tools such as SSH, RDP, or Virtual Network Computing (VNC). The objective is to establish a stable connection that allows users to perform penetration testing, security assessments, and administrative tasks on Kali Linux from a Windows-based system. The project will focus on configuring remote access securely, ensuring encrypted communication, and optimizing performance for seamless operation.

## Sills Learned
- Profficiency in the use of putty app
- Secure Shell (SSH) configuration on Kali Linux
- Uncompliacated Firewall (UFW) configuration on Kali Linux
- Remote access using Kali Linux OS
- Remote access using Windows OS

## Tools Used
- Putty app for windows
- Uncomplicated Firewall (UFW)
- Kali Linux OS
- Windows OS


## Steps
- **Step 1:** Download Putty app on windows OS
  
![image](https://github.com/user-attachments/assets/f9c4d6d9-e81d-4220-937f-4ebed043efc5)

*Ref 1: Putty app interface*

- **Step 2:** On Kali, download Secure Shell (SSH) and Uncomplicated firewall with the command "sudo apt install openssh-server openssh-client" and "sudo apt install ufw" respectively.

- **Step 3:** Activate and enable SSH with the command "sudo systemctl start ssh" and "sudo systemctl enable ssh".

- **Step 4:** Activate and enable UFW with the command "sudo ufw start" and "sudo ufw enable"

- **Step 5:** Check the status of both UFW and SSH with the command "sudo ufw status" and "sudo systemctl status ssh" respectively.

![image](https://github.com/user-attachments/assets/f3452900-17e2-41b4-8908-5d142b35aa5c)

*Ref 2: status check*
      
- **Step 6:** Allow the port needed which is port 22 which ssh uses using the command "sudo ufw allow 22" and check the status with the command "sudo ufw status".

 ![image](https://github.com/user-attachments/assets/c1c86ce5-22b6-430c-9dc1-adcaa090b1b4)
 
*Ref 3: UFW port status check*
- **Step 7:** On Kali, use the command "ip a" to check for your Ip address.

- **Step 8:** On the windows OS, open the putty app, input the kali Ip address in the input field, set the port to 22 and connection type to ssh, then click on open.

![image](https://github.com/user-attachments/assets/d62a0636-1d11-4cda-a352-bb49d0ee4c0a)

*Ref 4: Putty app interface*
- **Step 9:** Input your login detail and password, then you already have access to your kali, you can use the terminal to do things you would normally do when using your kali terminal.

![image](https://github.com/user-attachments/assets/82b1aa67-8203-44bb-949f-b11b6d1390c2)

*Ref 5: Remote access to kali linux*
## Importance of Remote Connection Using SSH

- **Secure Communication** – SSH encrypts data transmission, protecting credentials and sensitive information from interception and cyber threats like Man-in-the-Middle (MITM) attacks.
- **Remote Administration** – System administrators and cybersecurity professionals can securely manage servers, execute commands, and perform updates from anywhere, improving efficiency and flexibility.
- **Port Forwarding & Tunneling** – SSH enables encrypted tunneling for secure data transfer, allowing safe access to remote services and applications over an unsecured network.
- **File Transfer** – Secure file transfers using SCP (Secure Copy Protocol) and SFTP (Secure File Transfer Protocol) allow encrypted data movement between systems.
- **Automation & Scripting** – SSH facilitates remote automation by enabling secure execution of scripts and commands across multiple servers without direct physical access.
- **Access Control & Authentication** – Supports key-based authentication, reducing the risks associated with password-based logins and improving system security.
- **Lightweight & Efficient** – SSH requires minimal system resources, making it an ideal choice for remote connections, even in low-bandwidth environments.


# Conclusion 
Remotely access provides a flexible and efficient way to perform security testing, ethical hacking, and system administration without the need for direct physical access. By utilizing tools such as Remote Desktop Protocol (RDP), SSH (Secure Shell), or Virtual Network Computing (VNC), users can seamlessly connect to their Kali Linux environment while maintaining security and operational efficiency.

# References
- https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/
- https://www.offensive-security.com/
- https://www.hackingarticles.in/


