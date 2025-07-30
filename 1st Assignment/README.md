**Assignment 11 Report: Ncat Chat Terminal**

**Objective**

To create a simple terminal-based chat system using `ncat` to demonstrate how basic network communication works over TCP. This builds foundational understanding of how data flows between machines — a critical concept in cybersecurity.

---

**Tools Used**

* **ncat** (from the Nmap suite)
* **Bash shell** (for scripting)
* **Two terminals or networked computers**

---

**Implementation**

The system uses two scripts:

* `listener.sh`: Runs on Terminal A and listens for TCP connections on port 12345.
* `client.sh`: Runs on Terminal B, connects to Terminal A using its IP and port 12345.

After connection, both terminals can send and receive messages in real time.

---

**Script Overview**

**listener.sh**

```bash
PORT=12345
echo "Waiting for connection..."
ncat -lvp $PORT
```

**client.sh**

```bash
SERVER_IP=192.168.1.100  # Replace with actual IP
PORT=12345
ncat $SERVER_IP $PORT
```

---

**Security Relevance**

* **No encryption**: Data sent via `ncat` is in plaintext, making it vulnerable to packet sniffers.
* **Man-in-the-middle (MITM)**: Demonstrates how easy it is to observe or alter communication without encryption.
* **Learning outcome**: Understanding TCP chat flow helps explain why secure protocols like SSH, HTTPS, or TLS are needed.

---

**Conclusion**

This simple chat simulation using `ncat` helped reinforce the concepts of TCP communication, port listening, and client-server interaction — all essential foundations for cybersecurity professionals.

---



