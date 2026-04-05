# Automating-Java-Web-App-Deployment-to-Tomcat-with-GitHub-Actions

---

## 🧠 Introduction

This project demonstrates a **CI/CD pipeline using GitHub Actions** to automatically deploy a Java web application to an **Apache Tomcat server**.

The pipeline performs:
- Code checkout  
- Java setup  
- Build using Maven  
- Testing  
- WAR file creation  
- Deployment to Tomcat  

👉 This removes manual deployment and ensures fast, reliable delivery.

---

## 🛠️ Tools Used

- **GitHub** – Source code management & CI/CD  
- **Maven** – Build tool for Java (WAR file creation)  
- **Apache Tomcat** – Application server  
- **AWS EC2** – Hosting environment  
- **GitHub Actions** – Automation pipeline  

---

## ⚙️ Step-by-Step Implementation

---

### 1️⃣ Create EC2 Instances

- Create **4 EC2 instances** for environments:
  - Tomcat-Dev  
  - Tomcat-Test  
  - Tomcat-Pre-Prod  
  - Tomcat-Prod  

---

### 2️⃣ Install Java and Maven

- Install Java on EC2  
- Install Maven to:
  - Compile code  
  - Run tests  
  - Generate WAR file  

---

### 3️⃣ Install Tomcat

- Install **Tomcat 9** on all EC2 instances  
- Configure to run on port **8080**  
- Update `tomcat-users.xml`:
  - Add roles:
    - `manager-gui`  
    - `manager-script`  

---

### 4️⃣ Configure GitHub Repository

- Push source code to GitHub  
- Create workflow file:
