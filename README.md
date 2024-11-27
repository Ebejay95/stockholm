# Cybersecurity Piscine – Stockholm

**A harmless educational exploration into ransomware mechanics.**

---

## Summary

**Stockholm** is a project in the Cybersecurity Piscine designed to deepen your understanding of malware, specifically ransomware. You will develop a program that encrypts and decrypts files in a controlled environment. The project emphasizes safe experimentation, secure encryption practices, and error handling.

---

## Features

### Core Functionality

1. **File Encryption**:
   - Encrypts files in the `~/infection` directory using a secure algorithm.
   - Adds the `.ft` extension to encrypted files.

2. **Decryption**:
   - Reverts the encrypted files back to their original state using the same key.

3. **Command-Line Interface**:
   - **`--help` / `-h`**: Displays usage instructions.
   - **`--version` / `-v`**: Shows the program version.
   - **`--reverse` / `-r`**: Decrypts files using the provided key.
   - **`--silent` / `-s`**: Suppresses output during encryption or decryption.

4. **Controlled Execution**:
   - Operates only in the `~/infection` directory.
   - Targets file extensions affected by the Wannacry ransomware.

5. **Error Handling**:
   - Gracefully handles errors without unexpected termination.

---

## Requirements

### Mandatory Part

1. **Encryption**:
   - Encrypts files using a secure algorithm (e.g., AES-256).
   - Ensures the encryption key is at least 16 characters long.

2. **File Renaming**:
   - Adds the `.ft` extension to encrypted files.
   - Skips files that already have the `.ft` extension.

3. **Decryption**:
   - Reverts encrypted files back to their original state using the provided key.

4. **Environment**:
   - Operates exclusively in the `~/infection` folder in the user’s home directory.

5. **Command-Line Options**:
   - Implements the required options (`--help`, `--version`, `--reverse`, `--silent`).

6. **Documentation**:
   - Includes a `README.md` with usage instructions (max 50 lines).
   - Provides a `Makefile` to configure the program for execution.

7. **Security**:
   - Uses a justified, secure encryption library (e.g., OpenSSL or Libsodium).

---

## Structure

### Directory Layout

Your repository should include:
. ├── Makefile # Automates setup and execution ├── README.md # Usage instructions and compilation guide ├── src/ # Source code for the Stockholm program │ ├── stockholm.c # Main program logic │ └── ...

yaml
Code kopieren

---

## Usage

### Build the Program

1. **Build the Docker Image**:
   ```bash
   docker build -t stockholm .
   ```
Run the Program:
```
docker run -it --rm -v $(pwd):/app stockholm
Test the Setup:

bash
Code kopieren
docker ps -a
docker images
```

## Command Examples
### Display Help:
```
./stockholm --help
```
### Encrypt Files:
```
./stockholm
```
### Decrypt Files:
```
./stockholm --reverse <key>
```
### Silent Mode:
```
./stockholm --silent
```

## Learning Outcomes
### Understanding Ransomware:
Learn how ransomware encrypts and manipulates files.
### File Encryption Basics:
Gain experience with secure encryption algorithms.
### Error Handling:
Build robust software with graceful failure modes.

Stockholm – Safely exploring the mechanics of encryption and ransomware! 🔒
