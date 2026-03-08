🔐 Hashing & Cryptography 101

Interactive web-based learning platform that explains hashing, encoding, encryption, salting, and password cracking through live demos and practical cybersecurity examples.

This project is inspired by hands-on cybersecurity labs similar to those found on TryHackMe, but implemented as an interactive browser tool.

🌐 Live Website:

https://naveenkumar-arch.github.io/hashing-crypto-101
🧠 What You Will Learn

This project demonstrates core cryptography concepts used in real-world cybersecurity:

🔑 Hashing

One-way functions

Fixed-length outputs

Avalanche effect

Collision resistance

🔄 Encoding

Base64

Hex

ROT13

URL encoding

Binary

🔐 Encryption

Symmetric encryption (AES)

Asymmetric encryption (RSA)

Public and private keys

🧂 Salting

Prevents rainbow table attacks

Ensures unique password hashes

⚔️ Password Cracking

Identifying hash types

Cracking hashes using wordlists

Understanding attack workflows

🚀 Features

✨ Interactive learning interface
✨ Live hash generator (MD5, SHA-1, SHA-256)
✨ Avalanche effect visualization
✨ Encoding & decoding playground
✨ Kali Linux command examples
✨ Password cracking challenges
✨ Step-by-step cybersecurity workflow

🛠 Technologies Used

HTML5

CSS3

JavaScript

Web Crypto API

The project runs fully in the browser, with no backend required.

🧪 Hashing Demo Example

Input:

password

Outputs:

MD5
5f4dcc3b5aa765d61d8327deb882cf99

SHA1
5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8

SHA256
5e884898da28047151d0e56f8dc6292773603d0d6aabbdd62a11ef721d1542d8

Even a single character change completely changes the hash.

Example:

password
Password

This demonstrates the Avalanche Effect.

🐧 Kali Linux Commands

You can reproduce many concepts using Kali Linux.

Generate Hashes
# MD5
echo -n "password" | md5sum

# SHA-1
echo -n "password" | sha1sum

# SHA-256
echo -n "password" | sha256sum

# SHA-512
echo -n "password" | sha512sum
Base64 Encoding / Decoding
# Encode
echo -n "hello world" | base64

# Decode
echo "aGVsbG8gd29ybGQ=" | base64 -d
Hex Encoding
# Encode
echo -n "hello" | xxd -p

# Decode
echo "68656c6c6f" | xxd -r -p
🔓 Password Cracking Examples
Using John the Ripper
echo "5f4dcc3b5aa765d61d8327deb882cf99" > hash.txt

john hash.txt --wordlist=/usr/share/wordlists/rockyou.txt --format=raw-md5

john hash.txt --show
Using Hashcat
hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt

Example result:

5f4dcc3b5aa765d61d8327deb882cf99:password
🧂 Example of Salting

Same password with different salts produces different hashes.

password123 + salt1 → hashA
password123 + salt2 → hashB
password123 + salt3 → hashC

Salting prevents rainbow table attacks.

🎯 Challenges Included

The project includes practice hashes similar to CTF exercises.

Examples:

Type	Hash
MD5	482c811da5d5b4bc6d497ffa98491e38
SHA1	aaf4c61ddcc5e8a2dabede0f3b482cd9aea9434d
SHA256	8d969eef6ecad3c29a3a629280e686cf...

Try cracking them using:

John the Ripper

Hashcat

Kali Linux tools

🎓 Educational Purpose

This project was created to help cybersecurity students understand cryptography concepts through practice.

Topics covered include:

Password hashing

Encoding detection

Encryption basics

Password cracking techniques

Kali Linux security tools

👨‍💻 Author

Naveen Kumar K

🎓 Cyber Security Student
💻 Web Development & Security Enthusiast
