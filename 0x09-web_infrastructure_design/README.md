# Web Infrastructure Design

## Simple Web Stack
A single-server setup hosting **www.foobar.com**.

![Simple Web Stack](https://drive.google.com/uc?export=view&id=1Dwbc1I7g1zknurTp4OaKdy71uPEFhatI)
**Components:**
- **1 Server** (IP: 8.8.8.8)
- **Nginx Web Server**
- **Application Server**
- **Application Files (Code Base)**
- **MySQL Database**
- **Domain Name:** foobar.com with `www` record pointing to server IP (8.8.8.8)

**Key Points:**
- **Server:** Physical/virtual machine hosting services.
- **Domain Name:** Maps human-readable names to IP addresses.
- **DNS Record (www):** CNAME or A record.
- **Roles:**
  - Web Server → Handles HTTP requests, serves static files.
  - Application Server → Executes business logic.
  - Database → Stores and retrieves data.
- **Issues:**
  - **SPOF** (Single Point of Failure)
  - **Downtime during maintenance**
  - **No scalability** for high traffic


## Distributed Web Infrastructure
A three-server setup with **load balancing**.

**Additional Components:**
- **Load Balancer (HAProxy)**
- **2 Application/Web Servers**
- **Primary-Replica (Master-Slave) Database**

**Key Points:**
- **Load Balancer Algorithm:** Round Robin (or another specified algorithm) distributes requests evenly.
- **Active-Active vs Active-Passive:**
  - **Active-Active:** All servers process requests simultaneously.
  - **Active-Passive:** One server is standby, activated if the main fails.
- **Primary-Replica DB:**
  - **Primary:** Handles all writes and syncs to replica.
  - **Replica:** Handles read requests, cannot accept writes.
- **Issues:**
  - **SPOF** at the Load Balancer or Primary DB
  - **Security risks** (no HTTPS/firewall)
  - **No monitoring**


## Secured and Monitored Web Infrastructure
Enhancement of the distributed setup with **security** and **monitoring**.

**Additional Components:**
- **3 Firewalls** (LB, App Server 1, App Server 2)
- **SSL Certificate** for HTTPS traffic
- **3 Monitoring Clients** (Sumo Logic or similar)

**Key Points:**
- **Firewalls:** Filter incoming/outgoing traffic, protect servers.
- **HTTPS:** Encrypts communication, prevents data interception.
- **Monitoring:** Tracks performance, availability, and security events.
- **QPS Monitoring:** Configure monitoring tools to log and alert on queries per second.
- **Issues:**
  - **SSL Termination at Load Balancer:** Internal traffic may be unencrypted.
  - **One Primary DB:** Still a write bottleneck and SPOF.
  - **Identical Components per Server:** Increases attack surface if one server is compromised.
