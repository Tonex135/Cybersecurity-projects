Transferred files using File Transfer Protocol (FTP) which uses port 21 from my Windows OS to my Kali Linux while monitoring and capturing the Network traffic with WIRESHARK.



# Objective

This project aims to enhance the security of data transmission by implementing encryption techniques and real-time network traffic monitoring. It focuses on detecting and mitigating potential cyber threats, ensuring data integrity, confidentiality, and availability. By leveraging advanced security protocols and intrusion detection systems, the project seeks to safeguard sensitive information from unauthorized access and cyberattacks while maintaining optimal network performance.

## Skills Learned

- Encyption using openssl.
- Firewall configuration on both windows OS and Kali Linux.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Ability to hash files.

## Tools Used

- Filezilla
- Vsftp(Very Secure File Transfer Protocol)
- VMware
- Windows operating system
- Kali Linux operating system
- Wireshark
- UFW(Uncomplicated Firewall)
- Openssl
- Hash calculator

## Steps
- Step 1: **DATA ENCRYPTION AND HASHING:** A file text named (group9ad) was created with the command ‘touch group9ad’ and was encrypted using openssl on kali linux with the command line ‘openssl enc –e –des3 –salt –in group9ad –out group9adec –iter 1000’ which gave an encrypted output of  file text named (group9adec). A hash value was generated for both the encrypted and unencrypted file text on kali linux, using the command line ‘sha256sum <file name>’
![image](https://github.com/user-attachments/assets/a7179dd2-c5a2-4e6d-b98d-bdcba0a935cd)
*Ref 1: Data encryption and hashing*


- Step 2: **FILE TRANSFER OVER NETWORK:** Both the encrypted file text with the name (group9adec) and the unencrypted file text with the name (group9ad) was transferred using File Transfer Protocol(FTP) between windows and a kali linux operating system. This was done by creating an ftp server on the windows OS and hosting it with FILEZILLA. Then also an ftp client was download on Kali linux with the command ‘sudo apt install vsftpd’ and configured with the command ‘sudo nano /etc/vsftpd.conf’. After hosting the server on windows, then moved to kali Linux and used the command ‘ftp <windows Ip address>’ to establish a connection, then the command ‘put <file name>’ was used to transfer the files.
![image](https://github.com/user-attachments/assets/c4c6b4cf-d717-4995-aba0-7cbd5ed3019f)
*Ref 2: File transfer over the network*

- Step 3: **Network Traffic Capture with Wireshark:** Wireshark was used to capture traffic of both the unencrypted file text with the name (group9ad) and encrypted  file text with the name (group9adec) and identify packets during the file transfer process. The Wireshark packet capture was filtered with ‘ftp-data’. And it was discovered after capturing the packets and following the stream that the unencrypted file was able to be read and extracted in plain text while the encrypted file still remained encrypted. 
![image](https://github.com/user-attachments/assets/58f16ade-b403-434c-bbef-99b2fe992eed)
*Ref 3: Network capture with wireshark*


![image](https://github.com/user-attachments/assets/bd08263b-8d01-4ea4-a48c-9ae5a105f66f)
*Ref 4: Network Traffic Capture with Wireshark: Unencrypted file text capture*


![image](https://github.com/user-attachments/assets/0927a10a-85ff-496a-9266-dcb4d4017ffc)
*Ref 5: Network Traffic Capture with Wireshark: Unencrypted file text capture*


## Importance of Encryption and Hashing in Secure communication:
### Encryption:
- **Confidentiality:** Encryption ensures that sensitive information remains private by converting it into unreadable ciphertext. Only authorized parties with the decryption key can revert it back to its original form, ensuring that unauthorized users cannot access the data.
- **Data Integrity:** By encrypting the communication, any tampering with the data can be detected. If someone intercepts the encrypted message and modifies it, decryption will fail or the integrity check will fail.
- **Authentication:** Some encryption schemes, like digital signatures, also authenticate the sender, ensuring that the message comes from the expected source.

### Hashing:
- **Data Integrity:** Hashing provides a unique, fixed-length output (hash) for any given input. In secure communication, a hash can be used to ensure that the message has not been altered in transit. If even a small change occurs, the hash will change significantly.
- **Verification:** When a message is received, the receiver can hash the received data and compare it with the sender's previously generated hash (often sent alongside the message). If the hashes match, the data is intact. 
- **Password Storage:** In secure systems, passwords are often hashed instead of stored in plaintext. This ensures that even if the system is breached, the actual passwords are not compromised.


# CONCLUSION
In today’s interconnected world, securing data transmission and monitoring network traffic are vital for safeguarding sensitive information and preventing cyber threats. Proactive monitoring helps identify vulnerabilities and detect malicious activities in real-time, ensuring a robust defense. During this project, we used encryption and hashing techniques to secure our data from the reach of third parties, and also ensured the integrity of the information. Ultimately, both strategies are essential in securing communication and protecting against unauthorized access and tampering.


# REFERENCES
https://www.okta.com
https://www.clickssl.net
https://filezilla-project.org

