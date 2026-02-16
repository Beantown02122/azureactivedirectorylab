# Azure Active Directory Lab

## Project Overview

This lab demonstrates deployment and configuration of an Azure virtual machine, SSL/TLS encryption setup, HTTPS enforcement, OpenSSL key generation, and Active Directory Group Policy configuration.

The objective was to configure a secure Apache web server inside an Azure-hosted Ubuntu virtual machine and apply directory-level security controls.

---

## 1. Azure Virtual Machine Deployment

### Ubuntu VM Running in Azure

![Ubuntu VM](unbuntucapture.JPG)

The Ubuntu virtual machine was successfully deployed in Microsoft Azure and accessed remotely.

---

## 2. SSL Certificate Generation

### Private Key Generation

![Private Key](privatekey.JPG)

An RSA private key was generated using OpenSSL with AES-256 encryption.

### Public Key Extraction

![Public Key](publickey.JPG)

The public key was extracted from the private key for encryption processes.

---

## 3. Apache SSL Configuration

### Apache SSL Configuration File

![Apache SSL Config](apachesslconfig.JPG)

Apache was configured inside `/etc/apache2/sites-available/default-ssl.conf` to enable SSL by referencing the certificate and key files.

---

## 4. HTTPS Enforcement and Validation

### HTTPS Working Properly

![HTTPS Working](httpworking.JPG)

The website loads successfully over HTTPS, confirming SSL configuration is operational.

### HTTP Blocked After HTTPS Enforcement

![HTTP Blocked](httpblocked.JPG)

HTTP access fails after enforcing HTTPS-only configuration, ensuring encrypted communication.

---

## 5. Remote Desktop Authentication Test

### RDP Credential Enforcement

![RDP Authentication](rdp-authentication.JPG)

Remote login attempt demonstrating credential authentication enforcement within the Azure environment.

---

## 6. Active Directory Group Policy Configuration

### Group Policy Linked to Students OU

![GPO Linked](linkingthegpo.JPG)

The Students Lockdown Policy was successfully linked to the Students Organizational Unit within Active Directory.

---

## Security Concepts Demonstrated

- Azure Virtual Machine Deployment  
- SSL/TLS Encryption  
- Public and Private Key Cryptography  
- Apache Web Server Configuration  
- HTTPS Enforcement  
- Remote Desktop Authentication Controls  
- Active Directory Organizational Units  
- Group Policy Management  

---
