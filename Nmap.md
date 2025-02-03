# How I Work with Nmap on Windows

## 1. Downloading and Installing Nmap

To get started with **Nmap**, I first download it from the official website:

- **Website:** [https://nmap.org/download.html](https://nmap.org/download.html)
- I choose the **Windows** version and install it by following the on-screen instructions.

## 2. Running Nmap on Windows

After installation, I can run Nmap in two ways:

- **Using Command Prompt (cmd)**
- **Using Zenmap (GUI for Nmap)**

Always should run this as an administrator. 


## 3. Common Nmap Commands I Use

Host IP : 192.168.101.120
Default Gateway : 192.168.101.1
Target IP : 192.168.101.124 (firwall is turned off)


### Identified the devices connected to the wifi adapter 

  `nmap -T4 -F 192.168.101.0/24`

  ![image](https://github.com/user-attachments/assets/f994131e-0246-4314-8cb9-3770db809da2)


### Ping from host to target

  ![image](https://github.com/user-attachments/assets/0223f4e7-7fd3-4fbd-b1cc-3fd097137248)


### Quick scan of the target IP

  `nmap -T4 -F 192.168.101.124`

  ![image](https://github.com/user-attachments/assets/b98832e1-8bb8-4931-b5ed-da95aa57a654)



### Scanning TCP/UDP ports with Nmap on windows

-  **Network Mapping**

  `nmap -T4 -A -v 192.168.101.124`
  
  To check the devices present on a network including all the routers, servers, and switches, and to verify how they are connected physically.
   

  ![image](https://github.com/user-attachments/assets/1433778e-d2bf-4c0a-be83-c5112828aa1f)




  ![image](https://github.com/user-attachments/assets/ba3b7d53-9fd3-4f63-be56-cdd2cbcf9e22)



- **Scanning all ports**

  `nmap -p- 192.168.101.124`

  ![image](https://github.com/user-attachments/assets/da3041d9-ee2a-41b4-ba9f-9937bbf2f238)



- **Scanning specific TCP ports within a range**

    `nmap -p1-500 192.168.101.124`
   
  - In Nmap, we can specify the port range by using the “-p” option. If we want to scan all TCP ports, then we can use -p1-10 option:


      ![image](https://github.com/user-attachments/assets/f45f2ea6-8ff6-46da-90db-fab092de1ea9)



- **Faster Scan option**

        `nmap -p- -T5 192.168.101.124`

  - We can use -T5 parameter for the quickest level scan of Nmap. The regular scan will consume a lot of time, whereas a fast scan option will do it in less time.


      ![image](https://github.com/user-attachments/assets/79cf1a84-ecd6-412b-81ef-ffbad5fa3ef7)


      

    Port ranges are categorized into three main groups based on their usage and allocation:

    1. **Well-Known Ports (0-1023)**  
       - These are assigned by the **Internet Assigned Numbers Authority (IANA)** for common services and protocols.  
       - Examples:
     - **HTTP** (Port 80)
     - **HTTPS** (Port 443)
     - **FTP** (Port 21)
     - **SSH** (Port 22)
     - **SMTP** (Port 25)

    2. **Registered Ports (1024-49151)**  
       - These ports are registered by IANA for specific applications and services but are not as universally reserved as well-known ports.  
       - Examples:
     - **MySQL** (Port 3306)
     - **PostgreSQL** (Port 5432)
     - **Docker** (Port 2375)

    3. **Dynamic or Private Ports (49152-65535)**  
       - These are usually used for **temporary or ephemeral connections**.  
       - When a client application connects to a server, it typically uses an ephemeral port assigned dynamically from this range.  
       - Example:  
         - When you visit a website, your browser might use a random port from this range for the outgoing request.

