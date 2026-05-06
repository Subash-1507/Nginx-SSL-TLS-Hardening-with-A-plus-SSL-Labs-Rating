# Nginx SSL/TLS Hardening with A+ SSL Labs Rating

## 📌 Project Overview

This project demonstrates the implementation of a secure HTTPS-enabled Nginx web server on Ubuntu 22.04 hosted on a DigitalOcean Virtual Machine. The server was configured using a trusted Let's Encrypt SSL certificate and hardened with modern TLS security practices to achieve an **A+ rating** on SSL Labs.

The project focuses on practical Secure System Engineering concepts including SSL/TLS certificate generation, HTTPS configuration, strong cipher suite enforcement, HSTS implementation, and secure web server deployment.

---

# 🛠️ Technologies Used

* Nginx
* Ubuntu 22.04
* OpenSSL
* Let's Encrypt
* Certbot
* TLS 1.2 / TLS 1.3
* DigitalOcean
* SSL Labs
* Linux
* HTTPS
* Secure System Engineering

---

# 🎯 Objectives

* Configure Nginx web server on Ubuntu
* Generate and install SSL/TLS certificates
* Enable HTTPS communication
* Redirect HTTP traffic to HTTPS
* Implement strong TLS configurations
* Achieve A+ rating in SSL Labs
* Understand practical web server hardening techniques

---

# ⚙️ Project Setup

## 1️⃣ Update Ubuntu Server

```bash
sudo apt update
sudo apt install nginx -y
```

---

## 2️⃣ Install Certbot

```bash
sudo apt install certbot python3-certbot-nginx -y
```

---

## 3️⃣ Generate SSL Certificate

```bash
sudo certbot --nginx -d <your-domain>
```

---

## 4️⃣ Configure Nginx Security Settings

```nginx
ssl_protocols TLSv1.2 TLSv1.3;
ssl_prefer_server_ciphers on;
ssl_ciphers EECDH+AESGCM:EDH+AESGCM;
ssl_session_cache shared:SSL:10m;
ssl_session_timeout 1d;
ssl_session_tickets off;
add_header Strict-Transport-Security "max-age=63072000; includeSubDomains; preload" always;
ssl_stapling on;
ssl_stapling_verify on;
```

---

## 5️⃣ Restart Nginx

```bash
sudo nginx -t
sudo systemctl restart nginx
```

---

# 🔒 Security Features Implemented

* HTTPS Enforcement
* TLS 1.2 and TLS 1.3 Support
* Strong Cipher Suite Configuration
* HSTS (HTTP Strict Transport Security)
* OCSP Stapling
* HTTP to HTTPS Redirection
* Secure Session Management
* Trusted Let's Encrypt SSL Certificate

---

# 📊 SSL Labs Result

The configured Nginx server successfully achieved:

## 🏆 SSL Labs Rating: A+

This confirms:

* Strong TLS configuration
* Secure certificate chain
* Proper HTTPS implementation
* Compliance with modern web security standards

# 📚 Learning Outcomes

Through this project, practical knowledge was gained in:

* SSL/TLS certificate generation
* Secure web server deployment
* HTTPS communication
* Nginx configuration management
* TLS hardening techniques
* Linux server administration
* Cloud-based security implementation

---

# 🧠 Conclusion

This project successfully demonstrated the secure deployment and hardening of an Nginx web server using SSL/TLS on Ubuntu 22.04. By implementing strong TLS protocols, secure cipher suites, HSTS, and trusted certificates from Let's Encrypt, the server achieved an A+ rating in SSL Labs. The project provided hands-on experience in web server security, HTTPS implementation, and modern security best practices.

---

# 👨‍💻 Author

Subash Chandra Bose Murugan

---

# ⭐ If you found this project useful

Give this repository a star ⭐
