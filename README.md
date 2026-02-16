# Azure Active Directory Lab

## Project Overview

This lab demonstrates deployment and configuration of an Azure virtual machine, implementation of SSL/TLS encryption, HTTPS enforcement, OpenSSL key generation, and Active Directory Group Policy configuration.

The objective was to configure a secure web server inside an Azure-hosted Ubuntu virtual machine and apply directory-level security controls.

---

## 1. Azure Virtual Machine Deployment

### Ubuntu VM Running in Azure

![Ubuntu VM Running](unbuntuCapture.JPG)

The Ubuntu 20.04 LTS virtual machine was successfully deployed in Microsoft Azure and accessed through Remote Desktop.

---

## 2. SSL Certificate Generation

### Private Key Generation

![Private Key Generation](Privatekey.JPG)

An RSA private key was generated using OpenSSL with AES-256 encryption.

### Public Key Extraction

![Public Key Generation](Publickey.JPG)

The public key was extracted from the private key for secure encryption processes.

---

## 3. Apache SSL Configuration

### SSL Configuration File

![Apache SSL Configuration](IMG_5770.jpg)

Apache was configured to enable SSL by referencing the generated certificate and key files.

---

## 4. HTTPS Enforcement and Validation

### HTTPS Functioning Properly

![HTTPS Test](Test HTTPS (for Screenshot #2).JPG)

The website loads successfully over HTTPS, confirming SSL configuration is working.

### HTTP Access Blocked After HTTPS Enforcement

![HTTP Blocked](Step 5.4 (HTTP fails after HTTPS-only).JPG)

HTTP access fails after enforcing HTTPS-only configuration, ensuring encrypted communication.

---

## 5. Active Directory Group Policy Configuration

### Group Policy Linked to Students OU

![GPO Linked](linking the GPO.JPG)

The Students Lockdown Policy was successfully linked to the Students Organizational Unit within Active Directory.

---

## 6. Remote Desktop Authentication Test

![RDP Credential Attempt](Screenshot #1 (Step 4.3.c).JPG)

Remote login attempt demonstrating credential authentication and domain enforcement.

---

## Security Concepts Demonstrated

- Azure Virtual Machine Deployment  
- SSL/TLS Encryption  
- Public and Private Key Cryptography  
- HTTPS Enforcement  
- Apache Web Server Configuration  
- Active Directory Organizational Units  
- Group Policy Management  

---
