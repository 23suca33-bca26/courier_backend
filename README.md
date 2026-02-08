
# 📦 PARCEL MANAGEMENT SYSTEM

## Spring Boot Backend – Courier / Parcel Tracking

---

## 📋 PROJECT OVERVIEW

This project is a **Courier / Parcel Management Backend System** developed using **Spring Boot**.
It provides RESTful APIs to manage parcel details such as sender, receiver, status, and delivery tracking.
The backend is integrated with a React frontend and follows **DevOps practices** including CI/CD, Docker, Sonar analysis, and cloud deployment.

---

## 🛠️ TECHNOLOGY STACK

### Backend

* Java 17
* Spring Boot 4.0.2
* Spring Web MVC
* Spring Data JPA
* H2 In-Memory Database
* Maven

### DevOps & Tools

* GitHub Actions (CI/CD)
* SonarCloud (Code Quality)
* Docker
* GitHub Organization
* GitHub Student Developer Pack

### Frontend (Integrated)

* React
* Deployed using Vercel

---

## 🗂️ PROJECT STRUCTURE

```
courier_tracking/
├── .github/
│   └── workflows/
│       └── build.yml
├── Dockerfile
├── pom.xml
├── mvnw
├── mvnw.cmd
├── src/
│   ├── main/
│   │   ├── java/com/example/
│   │   │   ├── courier_tracking/
│   │   │   │   └── CourierTrackingApplication.java
│   │   │   └── parcelmanagement/
│   │   │       ├── controller/
│   │   │       │   └── ParcelController.java
│   │   │       ├── model/
│   │   │       │   └── Parcel.java
│   │   │       ├── repository/
│   │   │       │   └── ParcelRepository.java
│   │   │       └── service/
│   │   │           ├── ParcelService.java
│   │   │           └── impl/ParcelServiceImpl.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/com/example/courier_tracking/
│           └── CourierTrackingApplicationTests.java
├── Devops/
│   ├── Backend Build.png
│   ├── backend execution.png
│   ├── Docker image Build.png
│   ├── sonarcube backend analysis.png
│   ├── vercel frontend deployment.png
│   └── custom domain name.png
└── presentation/
  ├── Parcel_Management_Presentation.pptx
  └── Parcel_Management_Presentation.pdf
```

---

## 🚀 INSTALLATION & SETUP

### Prerequisites

* Java 17
* Maven 3.9+ (or Maven Wrapper)
* Docker (optional)

### Run Locally

```bash
cd d:\courier_tracking\courier_tracking
mvn spring-boot:run
```

or

```bash
.\mvnw.cmd spring-boot:run
```

---

## 🌐 APPLICATION URLS

### Local Development

* Backend API: `http://localhost:8080`
* H2 Console: `http://localhost:8080/h2-console`

### Production Deployment

* Backend API (Render): [https://courier-backend-2-0.onrender.com](https://courier-backend-2-0.onrender.com)
* Frontend (Vercel): [https://couriertracking.vercel.app/](https://couriertracking.vercel.app/)

---

## ⚙️ H2 DATABASE CONFIGURATION

```
spring.datasource.url=jdbc:h2:mem:parceldb
spring.datasource.username=sa
spring.datasource.password=
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
```

**H2 Login**

* JDBC URL: `jdbc:h2:mem:parceldb`
* Username: `sa`
* Password: (empty)

---

## 📡 API ENDPOINTS

**Base Path:** `/api/parcels`

| Method | Endpoint          | Description        |
| ------ | ----------------- | ------------------ |
| POST   | /api/parcels      | Create new parcel  |
| GET    | /api/parcels      | Fetch all parcels  |
| GET    | /api/parcels/{id} | Fetch parcel by ID |
| PUT    | /api/parcels/{id} | Update parcel      |
| DELETE | /api/parcels/{id} | Delete parcel      |

### Sample JSON

```json
{
  "senderName": "John Doe",
  "receiverName": "Jane Smith",
  "parcelDescription": "Electronics",
  "receivedDate": "2026-01-31",
  "status": "RECEIVED",
  "contactNumber": "9876543210"
}
```

---

## 🧪 BUILD & TESTING

### Local Build

```bash
mvn clean verify
```

📸 **Screenshot:**
![Build success](Devops/Backend%20Build.png)

---

## 🔁 CI/CD PIPELINE (GitHub Actions)

* CI workflow located at `.github/workflows/build.yml`
* Triggers on:

  * Push to `main`
  * Pull Requests

Pipeline stages:

* Maven build
* Unit testing
* Sonar analysis

📸 **Screenshot:**
![CI/CD pipeline run](Devops/backend%20execution.png)

---

## 🔍 SONAR ANALYSIS (SONARCLOUD)

* Organization: `23suca33-bca26`
* Project Key: `23suca33-bca26_courier_backend`
* Quality Gate enforced

Command used:

```bash
mvn verify sonar:sonar
```

📸 **Screenshot:**
![Sonar analysis](Devops/sonarcube%20backend%20analysis.png)

---

## 🔀 PULL REQUEST WORKFLOW

* Feature branches created
* Pull Request raised to `main`
* CI + Sonar executed before merge

📸 **Screenshot:**
![Backend pull request](Devops/backend%20pull%20request.png)

---

## 🐳 DOCKER IMAGE BUILD

### Build Image

```bash
docker build -t courier-backend .
```

### Run Container

```bash
docker run -p 8080:8080 courier-backend
```

📸 **Screenshot:**
![Docker image build](Devops/Docker%20image%20Build.png)

---

## 🌍 DEPLOYMENT

### Backend Deployment (Render)

* Backend deployed on Render
* Live URL: [https://courier-backend-2-0.onrender.com](https://courier-backend-2-0.onrender.com)
* Automatically deploys from GitHub repository
* CORS configured for frontend communication

### Frontend Deployment (Vercel)

* Frontend deployed using Vercel
* Live URL: [https://couriertracking.vercel.app/](https://couriertracking.vercel.app/)
* Backend integrated via REST APIs
* SSL automatically enabled

📸 **Screenshot:**
Vercel Deployment
![Vercel deployment](Devops/vercel%20frontend%20deployment.png)
Custom Domain:
![Custom domain](Devops/custom%20domain%20name.png)

---

## 🎥 PROJECT DEMO

* Live demonstration includes:

  * API testing
  * CI/CD pipeline
  * Sonar dashboard
  * Docker container
  * Frontend integration

🎬 **Demo Video:**
[Watch Project Demo](https://drive.google.com/file/d/1pZXtoj6_CTyNvB9nz8Y2Q6aP2SSHIIw5/view?usp=sharing)

---

## 📑 PRESENTATION (COMPLETED ✅)

Presentation prepared and submitted:

* [presentation/Parcel_Management_Presentation.pdf](presentation/Parcel_Management_Presentation.pdf)
* [Devops/courier tracking project presentation.pdf](Devops/courier%20tracking%20project%20presentation.pdf)

Includes:

* Architecture
* Tools used
* DevOps workflow
* Challenges faced
* Conclusion

---

## 🎓 GITHUB STUDENT DEVELOPER PACK

Used for:

* SonarCloud access
* CI/CD tooling
* Cloud integrations

📸 **Screenshot:**
![Student pack](Devops/student%20pack.png)

---

## ⚡ CHALLENGES FACED & SOLUTIONS

* CI failures due to dependency mismatch
* Docker port conflicts
* Repository transfer to organization
* Environment variable issues
* Deployment permission errors

All issues were resolved using best DevOps practices and are documented in this project.

