# Securing Data with Encryption Software

This guide provides a detailed walkthrough of securing sensitive data using **VeraCrypt**, an open-source disk encryption software. You will learn how to create, mount, and manage encrypted file containers to protect your files in a controlled environment.

---

## Project Link

[Securing Data with Encryption Software](https://github.com/StephVergil/-Securing-Data-with-Encryption-Software/blob/main/%20Securing%20Data%20with%20Encryption%20Software.docx)

---

## Objectives

1. Create a VeraCrypt encrypted file container to secure sensitive data.
2. Mount and manage the encrypted container for file access.
3. Understand the significance of encryption key randomness and password strength.

---

## Step-by-Step Guide

### 1. Creating a VeraCrypt Container

#### **1.1 Launch VeraCrypt**
1. Start the **Kali VM** and log in using the provided credentials.
2. Right-click on an empty desktop space and select **Open Terminal Here**.
3. Create a text file named `billing.txt`:
   ```bash
   touch billing.txt
   ```
4. Launch VeraCrypt:
   ```bash
   veracrypt
   ```

#### **1.2 Create an Encrypted Container**
1. In the VeraCrypt application, click **Create Volume**.
2. In the VeraCrypt Volume Creation Wizard:
   - Select **Create an encrypted file container** and click **Next**.
   - Choose **Standard VeraCrypt volume** and click **Next**.
   - For **Volume Location**, click **Select File**, navigate to the desktop, select `billing.txt`, and click **Save**. Confirm the file replacement.
3. Confirm that the file location (`/home/kali/Desktop/billing.txt`) is displayed and click **Next**.
4. On the **Encryption Options** step:
   - Use the default settings: **AES** for encryption and **SHA-512** for hashing. Click **Next**.
5. On the **Volume Size** step:
   - Set the size to `50 MB` and click **Next**.
6. On the **Volume Password** step:
   - Enter a strong password (e.g., `password`) and confirm it. Click **Next**.
7. If prompted with a warning about short passwords, click **Yes** to proceed.
8. On the **Format Options** step:
   - Leave the default file system as **FAT** and click **Next**.
9. On the **Volume Format** step:
   - Move your mouse within the window to increase randomness for key generation.
   - Once the randomness level is sufficient, click **Format**.
10. Confirm replacing the file when prompted.
11. Upon successful creation, click **OK** and then **Exit** the wizard.

---

### 2. Opening and Viewing Data within a VeraCrypt Container

#### **2.1 Mount the VeraCrypt Container**
1. In VeraCrypt, click **Select File** and locate the encrypted container (`billing.txt`) on the desktop.
2. Select an available drive slot and click **Mount**.
3. Enter the password (`password`) and click **OK**.
4. If prompted for administrative privileges, enter `kali` and click **OK**.

#### **2.2 Access Encrypted Files**
1. Verify that the container is mounted as a virtual drive (e.g., `/media/veracrypt1`).
2. Open the mounted drive and copy files into it as needed.
3. Paste files from the desktop or other locations into the container.

#### **2.3 Unmount the Container**
1. Return to VeraCrypt.
2. Select the mounted container and click **Dismount**.
3. Verify that the virtual drive disappears from the desktop.

---

## Key Considerations

1. **Password Strength**:
   - Use a long, complex password to enhance security.
   - Avoid common words or patterns.
2. **Encryption Algorithm**:
   - AES (Advanced Encryption Standard) is a reliable choice for most use cases.
3. **Randomness**:
   - Increasing randomness during key generation improves encryption strength.

---

## Resources

- **VeraCrypt Official Documentation**: [VeraCrypt User Guide](https://www.veracrypt.fr/en/Documentation.html)
- **Encryption Basics**: [OWASP Cryptographic Storage Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html)
- **Data Security Best Practices**: [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- **Linux File Management**: [Linux Command Line Guide](https://linuxcommand.org/)
- **Kali Linux Tools**: [Kali Linux Documentation](https://www.kali.org/docs/)

---

## Key Takeaways

1. **Secure Data Handling**:
   - Learn to encrypt and manage sensitive files securely using VeraCrypt.
2. **Encryption Essentials**:
   - Understand the importance of randomness and strong passwords in securing data.
3. **Hands-On Practice**:
   - Develop practical skills in encryption and file management within a controlled environment.

---

### Disclaimer
This project was conducted in a controlled environment. Unauthorized use of these techniques or tools outside such an environment may violate ethical guidelines and legal regulations.

---

> **Author**: Stephanie Vergil
