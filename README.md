# Azure Active Directory Lab

## Project Overview

This lab demonstrates the deployment and secure configuration of an Azure-hosted Ubuntu virtual machine. The project includes SSL/TLS certificate generation, Apache web server hardening, HTTPS enforcement, and Active Directory Group Policy configuration.

The objective was to configure a secure Apache web server inside an Azure virtual machine and apply directory-based security controls using Active Directory.

---

## 1. Azure Virtual Machine Deployment

### Ubuntu VM Running in Azure

![Ubuntu VM](unbuntucapture.JPG)

The Ubuntu virtual machine was successfully deployed in Microsoft Azure and accessed remotely through secure authentication.

This confirms proper cloud resource provisioning and remote connectivity.

---

## 2. SSL Certificate Generation

### Private Key Generation

![Private Key](privatekey.JPG)

An RSA private key was generated using OpenSSL with AES-256 encryption to protect the key material.

### Public Key Extraction

![Public Key](publickey.JPG)

The corresponding public key was extracted from the private key to support encrypted communication.

This establishes the foundation for SSL/TLS encryption.

---

## 3. Apache SSL Configuration

### Apache SSL Configuration File

![Apache SSL Config](apachesslconfig.JPG)

Apache was configured within:

/etc/apache2/sites-available/default-ssl.conf

The configuration references the generated certificate and private key files to enable secure HTTPS communication.

SSL was enabled using:

a2enmod ssl  
a2ensite default-ssl  

This ensures encrypted web traffic.

---

## 4. HTTPS Enforcement and Validation

### HTTPS Working Properly

![HTTPS Working](httpworking.JPG)

The web server loads successfully over HTTPS, confirming SSL configuration is active and functioning.

### HTTP Blocked After HTTPS Enforcement

![HTTP Blocked](httpblocked.JPG)

HTTP access was disabled or redirected to HTTPS, preventing unencrypted communication.

This enforces transport layer security and protects data in transit.

---

## 5. Remote Desktop Authentication Test

### RDP Credential Enforcement

![RDP Authentication](rdp-authentication.JPG)

A remote login attempt demonstrates credential-based authentication enforcement within the Azure environment.

This validates identity-based access control.

---

## 6. Active Directory Group Policy Configuration

### Group Policy Linked to Students OU

![GPO Linked](linkingthegpo.JPG)

The Students Lockdown Policy was successfully linked to the Students Organizational Unit within Active Directory.

This confirms centralized policy enforcement at the directory level.

---

## Security Concepts Demonstrated

- Azure Virtual Machine Deployment  
- SSL/TLS Encryption  
- Public and Private Key Cryptography  
- Apache Web Server Hardening  
- HTTPS Enforcement  
- Identity-Based Access Control  
- Active Directory Organizational Units  
- Group Policy Management  
