# 🔐 AES Encrypted Multi Client-Server in Python

## Overview

This project demonstrates a simple but powerful **client-server chat application** built in Python. It uses **AES-256 encryption** in **EAX mode** to ensure **confidentiality, integrity, and authenticity** of all exchanged messages between the server and the client.

The main features:

- Encrypted communication using `pycryptodome`
- Real-time chat over local network
- Easy to use and understand
- Demonstrated network visibility with Wireshark before and after encryption

---

## 🌐 Network Setup

- **Server** runs on a **host PC**.
- **Client** runs inside a **VMware virtual machine**.
- Both systems are connected via the same **LAN**.
- **Wireshark** is used to inspect traffic:
  - 🔓 Before AES: Messages are visible in plaintext.&#x20;
  - 🔐 After AES: Messages appear as ciphertext and are unreadable.&#x20;

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/hexsecteam/AES-Encrypted-Multi-Client-Server-in-Python-DEMO-.git
cd AES-Encrypted-Multi-Client-Server-in-Python-DEMO--main
```

Install the required Python module:

```bash
pip install pycryptodome
```

---

## 🛠 Running the Chat

### On the Server:

```bash
python serv.py
```

### On the Client (in VMware or another PC):

```bash
python client.py
```

---

## 📁 File Structure

### `serv.py` (Server)

This script acts as the server. It generates the AES key, listens for a client connection, and handles sending and receiving encrypted messages.


### `client.py` (Client)

The client connects to the server and uses the shared key to securely exchange messages.


---

## 🎓 How It Works

1. **Key Generation**: Server generates a 256-bit AES key using `get_random_bytes()`.
2. **Key Exchange**: The key is sent once to the client when it connects.
3. **Encryption Process**:
   - Uses AES in EAX mode to encrypt and generate a `tag`.
   - Final data = `nonce + tag + ciphertext`
4. **Decryption Process**:
   - Extracts `nonce`, `tag`, and actual message.
   - Uses same AES key and nonce to decrypt and verify integrity.

---

## 🔧 Future Features

- Implement **RSA** or **Diffie-Hellman** for secure key exchange
- Add a **GUI** using Tkinter or PyQt
- Allow multiple clients (multi-threaded server)
- Add **user authentication** and **logging**

---

## 💪 Credits

Developed with ❤️ by **Hacker Pyush Singh**

> 🧠 This tool is meant for **educational** and **ethical hacking** research only. Always use responsibly.

---

## 🤝 Support the HexSec Community

If you appreciate our work and want to help us grow, you can contribute by making a donation. Your support allows us to keep creating secure, innovative tools for the community.

### 🪙 Donate

- **ETH:** `0x2a8fDa085984508b15AfA9E6796E4fB62Ecb533c`
- **BTC:** `bc1qu0cf3ptq37dtau2znltq9k4aw7q5dyfw7sxga9`

### 📞 Contact

- Telegram Contact: [@Hexsecteam](https://t.me/cyberforenx)
- Telegram Group: [@hexsec\_tools](https://t.me/hackingspottelugu)

---

🔹 Cybersecurity | Secure Development | Ethical Research | Security Engineering

