# How I Work with Nmap on Windows

## 1. Downloading and Installing Nmap

To get started with **Nmap**, I first download it from the official website:

- **Website:** [https://nmap.org/download.html](https://nmap.org/download.html)
- I choose the **Windows** version and install it by following the on-screen instructions.

## 2. Running Nmap on Windows

After installation, I can run Nmap in two ways:

- **Using Command Prompt (cmd)**
- **Using Zenmap (GUI for Nmap)**


### Using Zenmap (GUI)

1. Open **Zenmap** from the Start menu.
2. Enter a target (e.g., `scanme.nmap.org`).
3. Choose a scan type (e.g., **Intense Scan**).
4. Click **Scan** to start.


## 3. Common Nmap Commands I Use

### Scanning TCP/UDP ports with Nmap on windows




-  **Network Mapping**

`nmap -T4 -A -v 127.0.0.1`
  
To check the devices present on a network including all the routers, servers, and switches, and to verify how they are connected physically.
   
![image](https://github.com/user-attachments/assets/86013742-eac5-4eab-8bf4-108c8a7f3f85)


- **Scanning all ports**

  `nmap -p- 127.0.0.1`

![image](https://github.com/user-attachments/assets/1fa35674-0a84-47a6-b882-50ef2ab4a78f)


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
 

   - **** 


