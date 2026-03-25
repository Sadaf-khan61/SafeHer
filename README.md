# 🛡️ SafeHer — AI-Powered Women Safety App

> Protecting Every Woman, Every Step of the Way

![SafeHer](https://img.shields.io/badge/SafeHer-Women%20Safety%20App-be185d?style=for-the-badge)
![Java](https://img.shields.io/badge/Java-Spring%20Boot-orange?style=flat-square)
![HTML](https://img.shields.io/badge/Frontend-HTML%2FCSS%2FJS-blue?style=flat-square)
![MySQL](https://img.shields.io/badge/Database-MySQL-green?style=flat-square)
![Render](https://img.shields.io/badge/Deployed-Render.com-purple?style=flat-square)

---

## 🌐 Live Demo

🔗 **[https://safeher-a-women-saftey-app.onrender.com](https://safeher-a-women-saftey-app.onrender.com)**

---

## 📌 About The Project

SafeHer is a full-stack women safety web application built for working women and daily commuters. It provides real-time safety tools including one-tap SOS alerts, AI danger detection, encrypted evidence recording, AI-generated FIR reports, and a community guardian network.

This repository contains the **Frontend** of the project built with plain HTML, CSS and JavaScript.

The **Backend** is built with Java Spring Boot and deployed separately on Render.com.

---

## ✨ Features

| Feature | Description | Status |
|---|---|---|
| 🆘 SOS Alert | One-tap emergency alert with real GPS location | ✅ Live |
| 🤖 AI Guardian | Voice stress and keyword danger detection | ✅ Live |
| ⚖️ Evidence Vault | Encrypted audio/video/photo recording | ✅ Live |
| 📋 AI FIR Generator | Auto-generates legal police complaint | ✅ Live |
| 🌐 Community Safety | Guardian Angel network + safe spots map | ✅ Live |
| 🎭 Escape Tools | Fake call simulator + escape strategies | ✅ Live |

---

## 📱 Pages

```
index.html      → Login & Register
dashboard.html  → Home Dashboard + SOS Button
ai-guard.html   → AI Danger Detection
community.html  → Guardian Network + Safe Spots
escape.html     → Fake Call + Escape Strategies
evidence.html   → Evidence Vault + FIR Generator
```

---

## 🛠️ Tech Stack

**Frontend**
- HTML5
- CSS3 (Pink gradient theme, mobile-first design)
- JavaScript (Vanilla JS, REST API calls)

**Backend** *(separate repository)*
- Java 21
- Spring Boot 3.5
- Spring Security
- Hibernate / JPA
- Maven

**Database**
- MySQL 8 hosted on Aiven Cloud

**Deployment**
- Docker
- Render.com

---

## 🚀 How To Run Locally

### Prerequisites
- Spring Boot backend running on `http://localhost:8080`
- MySQL database configured

### Steps

```bash
# Clone the repository
git clone https://github.com/Sadaf-khan61/SafeHer-Frontend.git

# Copy all HTML files to Spring Boot static folder
# src/main/resources/static/

# Start Spring Boot backend
mvn spring-boot:run

# Open in browser
http://localhost:8080/index.html
```

---

## 📂 Project Structure

```
SafeHer-Frontend/
│
├── index.html          # Login & Register page
├── dashboard.html      # Main dashboard with SOS
├── ai-guard.html       # AI Guardian detection page
├── community.html      # Community safety page
├── escape.html         # Escape tools page
├── evidence.html       # Evidence vault + FIR page
└── README.md           # Project documentation
```

---

## 🔌 API Endpoints Used

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login user |
| POST | `/api/sos/trigger` | Trigger SOS alert |
| GET | `/api/contacts/{userId}` | Get trusted contacts |
| POST | `/api/contacts/{userId}` | Add trusted contact |
| POST | `/api/evidence/save` | Save evidence |
| POST | `/api/fir/generate` | Generate AI FIR |
| POST | `/api/community/request` | Request community help |

---

## 🗺️ Future Roadmap

- [ ] Android APK using WebView
- [ ] Real voice stress detection using Web Speech API
- [ ] Twilio SMS alerts to trusted contacts
- [ ] Google Places API for real nearby safe spots
- [ ] Flutter rebuild for Android + iPhone both
- [ ] Google Play Store launch

---

## 👩‍💻 Author

**Sadaf Khan**
- 📧 talktosadafk@gmail.com
- 🔗 [LinkedIn](https://linkedin.com)
- 💻 [GitHub](https://github.com/Sadaf-khan61)
- 🏆 [Codolio](https://codolio.com)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">
  Made with ❤️ for Women Safety
  <br/>
  <strong>SafeHer — Because Every Woman Deserves to Feel Safe</strong>
</div>
