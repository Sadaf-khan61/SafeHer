# 🛡️ SafeHer — AI-Powered Women Safety App

> Protecting Every Woman, Every Step of the Way

![SafeHer](https://img.shields.io/badge/SafeHer-Women%20Safety%20App-be185d?style=for-the-badge)
![Java](https://img.shields.io/badge/Java-21-orange?style=flat-square)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5-brightgreen?style=flat-square)
![MySQL](https://img.shields.io/badge/Database-MySQL-blue?style=flat-square)
![Render](https://img.shields.io/badge/Deployed-Render.com-purple?style=flat-square)

A full-stack AI-powered women safety web application built with Spring Boot & vanilla JavaScript

---

## 🌐 Live Demo

🔗 **[https://safeher-a-women-saftey-app.onrender.com](https://safeher-a-women-saftey-app.onrender.com)**

⚠️ **Note:** This project is currently under development. Some features are still being worked on and improvements are being made regularly. Stay tuned for updates!

---

## 📌 About

SafeHer is a full-stack women safety web application designed for working women and daily commuters. It provides real-time AI-powered safety tools to help women stay protected at all times.

The platform offers:

- 👩 **Users** — Register, trigger SOS, record evidence, generate FIR and request community help

---

## ✨ Features

### 🆘 SOS Emergency Alert
- One-tap SOS button with 3-second countdown to cancel
- Real-time GPS location capture and automatic logging
- SOS history saved to database

### 🤖 AI Guardian Mode
- Voice stress detection and danger keyword monitoring
- Panic gesture recognition simulation
- Route deviation detection
- Auto SOS triggering when multiple danger signals detected

### ⚖️ Evidence Vault
- Secret audio, video and photo recording
- AES-256 encrypted storage
- Evidence usable as legal proof in court

### 📋 AI FIR Generator
- Describe incident in simple words
- AI generates formal police complaint with correct legal format
- Submit directly to police station

### 🌐 Community Safety
- Guardian Angel mode — volunteer to help nearby women
- Nearest safe spots — police stations, hospitals, pharmacies
- Send and receive anonymous help requests

### 🎭 Escape Tools
- Fake incoming call simulator (Mom, Boss, Police)
- Customizable ring delay (Now, 5 sec, 10 sec, 30 sec)
- Smart exit strategies — nearest cab, metro, safe spot

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java 21, Spring Boot 3.5, Spring Security |
| Authentication | BCrypt Password Encoding |
| Database | MySQL 8 with Hibernate ORM on Aiven Cloud |
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Deployment | Docker, Render.com |
| Build Tool | Maven |

---

## ⚙️ Local Setup & Running

### Prerequisites
- Java 21 — [Download](https://jdk.java.net/21/)
- Maven 3.8+ — [Download](https://maven.apache.org/download.cgi)
- MySQL 8.0+ — [Download](https://dev.mysql.com/downloads/)
- Git — [Download](https://git-scm.com/downloads)

### 1. Clone the Repository

```bash
git clone https://github.com/Sadaf-khan61/SafeHer-Frontend.git
cd SafeHer-Frontend
```

### 2. Configure the Database

```sql
CREATE DATABASE safher_db;
```

Open `src/main/resources/application.properties` and update:

```properties
# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/safher_db?useSSL=false&serverTimezone=UTC&allowPublicKeyRetrieval=true
spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password

# JPA / Hibernate
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=false
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect

# Server Port
server.port=8080
```

### 3. Build the Project

```bash
mvn clean install -DskipTests
```

### 4. Run the Application

```bash
mvn spring-boot:run
```

Or run the JAR directly:

```bash
java -jar target/safher-backend-0.0.1-SNAPSHOT.jar
```

### 5. Access the Application

Open your browser and go to:

```
http://localhost:8080/index.html
```

---

## 📡 API Endpoints

Base URL: `https://safeher-a-women-saftey-app.onrender.com/api` or `http://localhost:8080/api` locally

### 🔐 Authentication

**Register User**
```
POST /api/auth/register
```
```json
{
  "fullName": "Sadaf Khan",
  "email": "sadaf@gmail.com",
  "password": "password123",
  "phone": "9876543210",
  "homeAddress": "Lajpat Nagar",
  "workAddress": "Connaught Place"
}
```

**Login**
```
POST /api/auth/login
```
```json
{
  "email": "sadaf@gmail.com",
  "password": "password123"
}
```

### 🆘 SOS

**Trigger SOS Alert**
```
POST /api/sos/trigger
```
```json
{
  "userId": 1,
  "latitude": 28.6139,
  "longitude": 77.2090,
  "locationName": "Connaught Place",
  "triggeredBy": "MANUAL"
}
```

**Get SOS History**
```
GET /api/sos/history/{userId}
```

### 👥 Trusted Contacts

**Get Contacts**
```
GET /api/contacts/{userId}
```

**Add Contact**
```
POST /api/contacts/{userId}
```
```json
{
  "name": "Mom",
  "phone": "9876543210",
  "relation": "Mother"
}
```

### ⚖️ Evidence

**Save Evidence**
```
POST /api/evidence/save
```
```json
{
  "userId": 1,
  "evidenceType": "AUDIO",
  "fileUrl": "local://audio_123.aac",
  "locationName": "Current Location",
  "durationSeconds": 45
}
```

**Get Evidence**
```
GET /api/evidence/{userId}
```

### 📋 FIR

**Generate FIR**
```
POST /api/fir/generate
```
```json
{
  "userId": 1,
  "incidentType": "Harassment",
  "location": "Connaught Place Metro",
  "description": "I was harassed by an unknown person at 9PM"
}
```

**Submit FIR**
```
POST /api/fir/submit/{firId}
```

### 🌐 Community

**Request Help**
```
POST /api/community/request
```
```json
{
  "userId": 1,
  "latitude": 28.6139,
  "longitude": 77.2090,
  "message": "I need help near Metro Station"
}
```

---

## ❗ Error Responses

| Status Code | Meaning |
|---|---|
| 400 Bad Request | Invalid input or missing fields |
| 401 Unauthorized | Authentication failed |
| 404 Not Found | Resource does not exist |
| 409 Conflict | Duplicate entry |
| 500 Internal Server Error | Server-side error |

---

## 🏗 Project Structure

```
SafeHer/
├── src/main/java/com/safher/safher_backend/
│   ├── controller/        # REST API endpoints
│   ├── service/           # Business logic
│   ├── model/             # Database entities
│   ├── repository/        # Data access layer
│   ├── dto/               # Data transfer objects
│   └── config/            # Security configuration
├── src/main/resources/
│   ├── static/            # Frontend HTML files
│   └── application.properties
├── Dockerfile
└── pom.xml
```

---

## 👩‍💻 Author

| Member | GitHub |
|---|---|
| Sadaf Khan | [@Sadaf-khan61](https://github.com/Sadaf-khan61) |

---

## 📄 License

This project is licensed under the MIT License.

---

<div align="center">
  Made with ❤️ for Women Safety
  <br/>
  <strong>SafeHer — Because Every Woman Deserves to Feel Safe</strong>
</div>
