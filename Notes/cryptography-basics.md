# 🔐 Cryptography Basics

Understanding cryptography is essential for securing communication, protecting data, and ensuring authentication.

---

## 1️⃣ Symmetric Encryption
- Uses **one key** for both encryption 🔒 and decryption 🔑.  
- Faster but less secure for large-scale communication.  

### Examples:
- **AES (Advanced Encryption Standard)**
- **DES (Data Encryption Standard)**
- **3DES (Triple DES)**

✅ Best for encrypting **large amounts of data** quickly.  
⚠️ Key distribution is a challenge (must be securely shared).

---

## 2️⃣ Asymmetric Encryption
- Uses **two keys**:  
  - **Public Key** (used for encryption)  
  - **Private Key** (used for decryption)  
- Slower but more secure for key exchange and digital signatures.  

### Examples:
- **RSA (Rivest–Shamir–Adleman)**
- **ECC (Elliptic Curve Cryptography)**
- **Diffie-Hellman** (for secure key exchange)

✅ Solves the **key distribution problem**.  
⚠️ Slower than symmetric encryption, not ideal for bulk data.

---

## 3️⃣ Hashing
- One-way cryptographic function 🔄  
- Converts input (message/file) into a fixed-length string (hash value).  
- Cannot be reversed back to original input.  

### Uses:
- Password storage 🗝️
- Data integrity verification ✅
- Digital signatures ✍️

### Common Hash Algorithms:
- **MD5** – Fast but **not secure** ❌ (collision attacks possible).  
- **SHA-1** – Deprecated ❌.  
- **SHA-2 (SHA-256, SHA-512)** – Secure & widely used.  
- **SHA-3** – Latest standard, highly secure.  

---

## 4️⃣ SSL/TLS
- **SSL (Secure Sockets Layer)** and **TLS (Transport Layer Security)** are protocols for secure communication over the internet 🌐.  
- Use a combination of **symmetric + asymmetric encryption** + **hashing**.  

### How It Works:
1. **Handshake Phase** 🤝  
   - Client & server exchange keys using **asymmetric encryption**.  
2. **Session Phase** 🔑  
   - A **shared symmetric key** is established for faster communication.  
3. **Data Transfer** 🔒  
   - Data is encrypted with the symmetric key.  
   - Integrity ensured via hashing (e.g., HMAC).  

### Real-World Example:
- HTTPS websites use **TLS certificates** for secure browsing.  
- 🔑 Padlock icon in browser = Encrypted connection.  

---

## 📌 Summary
- **Symmetric Encryption** → Fast, one key, best for bulk data.  
- **Asymmetric Encryption** → Secure key exchange, two keys.  
- **Hashing** → One-way, ensures integrity.  
- **SSL/TLS** → Combines all three for secure communication.  

---
