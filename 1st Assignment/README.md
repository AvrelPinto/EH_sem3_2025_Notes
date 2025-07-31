## **Assignment 11 Report: Ncat Chat Terminal**

**Name:** Avrel Pinto

---

### **Methodology**

To simulate a basic chat between two terminals using network tools, I chose `ncat` (from the Nmap suite). The goal was to create a 10-line script that enables two-way communication between two computers (or terminals on the same machine). One terminal listens on a port, and another connects to it using the IP address.

---

### **Code**

**Terminal A (Listener):**

```bash
#!/bin/bash
# Terminal A - Listening on port 12345
echo "Listening on port 12345..."
ncat -l 12345
```

**Terminal B (Connector):**

```bash
#!/bin/bash
# Terminal B - Connecting to Terminal A
read -p "Enter listener IP: " ip
echo "Connecting to $ip..."
ncat $ip 12345
```

---

### **Findings**

* `ncat` enables instant peer-to-peer communication using TCP.
* Communication works seamlessly over localhost or LAN.
* Each terminal can send and receive text in real time.

---

### **Screenshot**
# Ncat Chat Demo

This project demonstrates a simple terminal chat using Ncat.

![Ncat chat example](images/ncat_chat.png)


### **Conclusions**

* I learned how to use `ncat` to establish basic socket communication.
* The task highlighted how vulnerable plain-text communication is if not encrypted.
* This exercise mirrors how attackers may exploit open ports to snoop on unsecured chats.
* Understanding such tools improves awareness of both networking fundamentals and security risks.

---




