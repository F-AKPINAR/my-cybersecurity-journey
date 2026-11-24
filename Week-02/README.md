# Week 2 — Networking, Web, LLM Security, OSINT, and Cryptology

## 📖 Topics I Learned

### Networking Basics
- **OSI** and **TCP/IP** layer models; how data travels across the layers.
- The concepts of **IP address, port, protocol**; the difference between TCP and UDP.
- Core protocols: HTTP/HTTPS, DNS, FTP, SSH, Telnet.

### Web Basics
- Client–server architecture, the HTTP request/response cycle.
- HTTP methods (GET, POST...), status codes (200, 404, 500...).
- Introduction to basic web vulnerability logic (the importance of input validation).

### LLM Security
- Risks specific to Large Language Models (LLMs): **prompt injection**, data leakage, untrusted output.
- The idea that user input must never be treated directly as a trusted command.

### OSINT (Open Source Intelligence)
- Gathering information from publicly available sources (web, social media, records).
- Building a footprint of the target during the reconnaissance phase.
- Ethical boundary: only public and authorized information.

### Cryptology
- The difference between **Encoding vs Encryption vs Hashing**:
  - *Encoding* (base64, base32): reversible, provides no confidentiality.
  - *Encryption*: encoding with a key, reversible.
  - *Hashing* (MD5, SHA): one-way, irreversible (password storage, integrity).
- Why weak/old algorithms (MD5, SHA1) are risky.

## 🧪 Practice — Labs
- **Decoding:** practice decoding base64/base32/binary text.
- **Hash cracking:** seeing how weak hashes can be cracked with dictionary/rainbow tables (understanding why passwords must be strong).

> *Note: Lab answers/flags are not shared here for confidentiality — only the method is explained.*

## 💡 Key Takeaways
- Something that is "encoded" is **not encrypted** — base64 provides no confidentiality!
- Weak passwords can be cracked in seconds; a strong password + strong hash is essential.

## ✅ Status
Week 2 tasks completed.
