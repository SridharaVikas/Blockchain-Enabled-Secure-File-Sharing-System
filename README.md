# 🔐 Blockchain-Enabled Secure File Sharing System Using QR Code Encryption

## 📌 Project Overview

The **Blockchain-Enabled Secure File Sharing System** is a web-based application developed to provide secure file sharing through AES encryption, QR code authentication, SHA-256 hashing, and blockchain-based integrity verification.

The application allows users to upload files, encrypt them using a secret key, and generate unique QR codes containing secure file access links. Authorized recipients can scan the QR code, enter the required secret key, and securely download the original file.

To enhance security, the system implements access restrictions such as maximum download limits and time-based expiration. Additionally, SHA-256 hashing is used to generate a unique digital fingerprint for each uploaded file. This fingerprint is recorded in a blockchain-based ledger to detect unauthorized modifications.

The application also provides a **Blockchain Explorer** that displays block details, transaction events, file information, timestamps, previous hashes, and current block hashes. It continuously validates the integrity of the blockchain to identify invalid or tampered records.

## 🎯 Project Objectives

- Provide secure and reliable file-sharing functionality.
- Protect confidential files using AES encryption.
- Implement QR code-based file access.
- Maintain file integrity using SHA-256 hashing.
- Record file activities through blockchain-based records.
- Prevent unauthorized downloads through access restrictions.
- Detect file modifications and suspicious activities.

## ✨ Key Features

### 1. AES File Encryption
- Encrypts uploaded files using the AES encryption algorithm.
- Requires a secret key for file decryption.
- Protects confidential information against unauthorized access.
- Keeps the decryption key separate from server-side file storage.

### 2. QR Code Generation
- Automatically generates a unique QR code after successful encryption.
- Provides a secure link for accessing the encrypted file.
- Allows recipients to scan or copy the generated link.
- Provides QR code download and sharing options.

### 3. Time-Based Access Control
- Allows users to configure file access duration in minutes.
- Automatically expires file access after the configured time.
- Displays a countdown timer showing the remaining access period.
- Prevents access after expiration.

### 4. Download Restrictions
- Allows users to configure the maximum number of downloads.
- Tracks file download activities.
- Restricts additional downloads after the permitted limit is reached.

### 5. SHA-256 File Integrity Verification
- Generates a SHA-256 hash of the original file during upload.
- Records the file fingerprint in the blockchain.
- Recalculates the hash before downloading.
- Compares the calculated hash with the recorded hash.
- Identifies unauthorized file modifications through hash mismatches.

### 6. Blockchain Integration
- Maintains a sequence of hash-linked blocks.
- Each block contains its own hash and the previous block's hash.
- Records important file-sharing events, including:
  - GENESIS
  - FILE_UPLOAD
  - FILE_DOWNLOAD
  - TAMPER_ALERT
- Uses SHA-256 hashing to maintain the integrity of blockchain records.
- Detects changes in block data through chain validation.

### 7. Blockchain Explorer
- Displays all blockchain records in a structured table.
- Shows block numbers and block hashes.
- Displays previous block hashes.
- Identifies file upload, download, and tampering events.
- Displays filenames, file SHA-256 fingerprints, and timestamps.
- Provides chain integrity status to indicate whether all blocks are valid.

### 8. Tamper Detection
- Verifies the downloaded file against its original SHA-256 fingerprint.
- Identifies unauthorized file modifications.
- Records detected tampering activities as blockchain events.
- Helps maintain transparency and accountability.

## ⚙️ How the Project Works

**Step 1: File Upload**
- The user selects a file to upload.
- Enters a secret encryption key.
- Configures the maximum download count and access duration.

**Step 2: File Encryption**
- The system encrypts the selected file using AES encryption.
- The encrypted file is stored on the server.
- The original file's SHA-256 fingerprint is generated.

**Step 3: Blockchain Recording**
- A new blockchain record is created for the file upload.
- The file fingerprint, filename, event type, and timestamp are recorded.
- The block is linked to the previous block using its hash.

**Step 4: QR Code Generation**
- A unique QR code is generated containing the secure file access link.
- The user can scan, copy, download, or share the QR code.
- The recipient needs the secret key to decrypt the file.

**Step 5: File Access and Decryption**
- The recipient scans the QR code or opens the shared link.
- The system checks whether the access link is valid and has not expired.
- The download limit is verified.
- The encrypted file is retrieved and decrypted using the correct secret key.

**Step 6: Integrity Verification**
- The system calculates the SHA-256 hash of the file.
- Compares it with the original fingerprint recorded during upload.
- If both hashes match, the file passes integrity verification.
- If they differ, a tampering alert is generated.

**Step 7: Blockchain Explorer**
- Users can view the blockchain records.
- The explorer displays upload, download, and tampering activities.
- Chain validation checks whether all blocks are correctly linked and their hashes are valid.

## 🛠️ Technologies Used

| Category | Technologies |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Encryption | AES |
| Hashing | SHA-256 |
| Authentication | QR Code |
| File Upload | Multer |
| Additional Packages | Axios, QR Code |
| Development Tools | VS Code, npm |

## 🏗️ System Architecture

The application follows a client-server architecture:

1. **Client Layer:** Handles file selection, secret key input, QR code display, and file access.
2. **Application Layer:** Manages encryption, decryption, file uploads, download restrictions, and access validation.
3. **Storage Layer:** Stores encrypted files and related metadata.
4. **Blockchain Layer:** Maintains hash-linked records of file activities and integrity information.
5. **Verification Layer:** Performs SHA-256 comparison and blockchain validation.

## 🔒 Security Benefits

- Confidentiality through AES encryption.
- File integrity through SHA-256 hashing.
- Controlled access through expiration and download limits.
- Tamper detection through fingerprint verification.
- Traceability through blockchain-based event records.
- Reduced exposure of sensitive information through separate key management.

## 🚀 Future Enhancements

- User registration and authentication.
- Role-based access control.
- Distributed blockchain integration.
- Cloud-based encrypted file storage.
- Email notifications for file access and expiration.
- Advanced audit logs and security monitoring.

## 📚 Learning Outcomes

This project provided practical experience in cryptography, blockchain concepts, backend development, database management, QR code generation, file handling, secure access control, and data integrity verification.
