# 🔐 Secure Image Steganography Using AES Encryption

> A web-based steganography application that securely hides encrypted messages inside images using AES encryption and Least Significant Bit (LSB) image steganography.

![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)
![HTML5](https://img.shields.io/badge/HTML5-Web%20Application-orange)
![CSS3](https://img.shields.io/badge/CSS3-Frontend-blue)
![CryptoJS](https://img.shields.io/badge/CryptoJS-AES%20Encryption-green)

---

# 📖 Project Overview

This project combines **Cryptography** and **Steganography** to provide a secure way of transmitting secret messages.

Before hiding a message inside an image:

1. The message is encrypted using AES encryption.
2. The encrypted text is embedded into the image using LSB (Least Significant Bit) steganography.
3. The modified image appears visually identical to the original image.
4. Only users with the correct secret key can extract and decrypt the hidden message.

---

# 🌟 Features

✅ Hide Secret Messages Inside Images

✅ AES Encryption for Enhanced Security

✅ LSB-Based Image Steganography

✅ Password-Protected Message Extraction

✅ PNG Image Support

✅ Browser-Based Processing

✅ No Server Required

✅ Fast and Lightweight

---

# 🛠 Technologies Used

| Technology     | Purpose               |
| -------------- | --------------------- |
| HTML5          | User Interface        |
| CSS3           | Styling               |
| JavaScript     | Application Logic     |
| CryptoJS       | AES Encryption        |
| Canvas API     | Image Processing      |
| FileReader API | Image Upload Handling |

---

# 🔒 Security Architecture

```text
User Message
      │
      ▼
AES Encryption
      │
      ▼
Encrypted Cipher Text
      │
      ▼
LSB Steganography
      │
      ▼
Image Embedding
      │
      ▼
Stego Image
```

### Extraction Process

```text
Stego Image
      │
      ▼
LSB Extraction
      │
      ▼
Encrypted Cipher Text
      │
      ▼
AES Decryption
      │
      ▼
Original Secret Message
```

---

# 🧠 How It Works

## Step 1: Message Encryption

The user enters:

* Secret Message
* Encryption Key

The message is encrypted using:

```javascript
CryptoJS.AES.encrypt(message, key)
```

Example:

```text
Original Message:
Hello World

Encrypted:
U2FsdGVkX19aP4mXx....
```

---

## Step 2: Binary Conversion

The encrypted message is converted into binary format.

Example:

```text
A = 01000001
B = 01000010
```

---

## Step 3: LSB Embedding

The binary message is hidden inside image pixels.

Original Pixel:

```text
11001010
```

After Embedding:

```text
11001011
```

Only the least significant bit changes, making the modification invisible to the human eye.

---

## Step 4: Image Generation

The modified image is generated and made available for download.

The visual appearance remains unchanged while carrying hidden encrypted data.

---

## Step 5: Message Extraction

The receiver uploads the stego image.

The application:

* Reads pixel data
* Extracts hidden bits
* Reconstructs encrypted text
* Detects message termination marker

---

## Step 6: AES Decryption

Using the correct secret key:

```javascript
CryptoJS.AES.decrypt(cipherText, key)
```

The original message is recovered.

---

# 📂 Project Structure

```bash
Secure-Steganography/
│
├── index.html
├── embed.js
├── extract.js
├── style.css
│
├── images/
│   ├── sample.png
│   └── output.png
│
└── README.md
```

---

# 🚀 Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/secure-image-steganography.git
```

## Open Project

Simply open:

```bash
index.html
```

in your browser.

No server setup is required.

---

# 📋 Usage Guide

## Embed a Secret Message

### Step 1

Upload an image.

### Step 2

Enter a secret message.

### Step 3

Enter an encryption key.

### Step 4

Click:

```text
Embed Message
```

### Step 5

Download the generated image.

---

## Extract a Secret Message

### Step 1

Upload the stego image.

### Step 2

Enter the correct decryption key.

### Step 3

Click:

```text
Extract Message
```

### Step 4

View the decrypted secret message.

---

# 🔑 Encryption Details

Algorithm Used:

```text
AES (Advanced Encryption Standard)
```

Mode:

```text
ECB Mode
```

Library:

```javascript
CryptoJS
```

Key Features:

* Fast Encryption
* Strong Security
* Password-Based Access
* Secure Message Storage

---

# 📊 Advantages

✔ Dual Security Layer

✔ Data Hidden Inside Images

✔ Encrypted Before Embedding

✔ Difficult to Detect

✔ Browser-Based Processing

✔ No Data Stored on Server

---

# 📸 Screenshots

## Home Page

Add Screenshot Here

```text
screenshots/home.png
```

## Message Embedding

Add Screenshot Here

```text
screenshots/embed.png
```

## Message Extraction

Add Screenshot Here

```text
screenshots/extract.png
```

---

# 🔮 Future Enhancements

* Multiple Image Formats Support
* Drag-and-Drop Upload
* Audio Steganography
* Video Steganography
* AES-256 Encryption
* Dark Mode UI
* Image Compression Detection
* Mobile Application Version

---

# 🎯 Applications

* Secure Communication
* Military Information Transfer
* Digital Watermarking
* Cybersecurity Projects
* Privacy Protection
* Educational Research

---

# 👨‍💻 Developer

**Kavin S**

B.E Computer Science and Engineering

Coimbatore Institute of Technology

---

# 📜 License

This project is licensed under the MIT License.

⭐ If you found this project useful, consider giving it a star on GitHub!
