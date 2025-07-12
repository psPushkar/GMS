
# 🚗 GMS – Garage Management System

A **Garage Management System** built as a **mobile-first application** using **React Native** for the frontend and **Go Lang** for the backend.

This project serves as a journey to explore and learn modern app development across full-stack technologies.

---

## 📚 Learning Resources

### 🟨 Go Lang Tutorials
- [TutorialsPoint GoLang Guide](https://www.tutorialspoint.com/go/index.htm)

#### 🔗 Extra Go Resources
- [Official Go Learn Portal](https://go.dev/learn/)
- [Go Blog](https://go.dev/blog/)
- [Web Service with Gin Tutorial](https://go.dev/doc/tutorial/web-service-gin#:~:text=This%20tutorial%20introduces%20the%20basics...)

---

### 🟦 React Native Tutorials
- [TutorialsPoint React Native Guide](https://www.tutorialspoint.com/react_native/index.htm)

#### 🔗 Extra React Native Resources
- [React Native Basics (YouTube)](https://www.youtube.com/watch?v=ZBCUegTZF7M)
- [React Native Full Playlist (YouTube)](https://www.youtube.com/playlist?list=PLC3y8-rFHvwhiQJD1di4eRVN30WWCXkg1)
- [React Native Crash Course](https://www.youtube.com/watch?v=WDunoPNBxKA&t=1s)
- [Beginner Expo Guide (Dev.to)](https://dev.to/vrinch/getting-started-with-react-native-expo-a-beginners-guide-4ae8)

---

### 🛠 Go Web Framework (Gin)
Gin is the chosen framework for the backend.

- [Gin Crash Course](https://www.youtube.com/watch?v=bj77B59nkTQ&t=20s)

---

## 🧱 Project Architecture

The system supports both **mobile** and **web**, designed using a **Monorepo with Shared Code** approach.

### ✅ Goals
- Web frontend using React
- Mobile app using React Native
- Shared business logic, types, and APIs

### 🗂 Monorepo Folder Structure

```
garage-app/
├── packages/
│   ├── shared/         # Shared code: utils, hooks, types, etc.
│   ├── mobile/         # React Native (Expo or CLI)
│   └── web/            # ReactJS (Vite or CRA)
├── node_modules/
├── package.json
└── turbo.json (if using Turborepo)
```

### 🧰 Tools & Frameworks

| Purpose           | Tool                     |
|-------------------|--------------------------|
| Monorepo mgmt     | Turborepo or Nx          |
| Web frontend      | React + Vite / CRA       |
| Mobile frontend   | React Native + Expo      |
| Shared logic base | TypeScript in packages/  |
| State/API mgmt    | Redux Toolkit + RTK Query|

---

## 🏗️ Project Architecture Patterns

| Pattern Name                       | Description                                                       | Use Case / Where it's Used            |
|------------------------------------|-------------------------------------------------------------------|----------------------------------------|
| **MVC**                            | View, Model, Controller split                                     | Classic Go web apps                    |
| **MVVM**                           | ViewModel binds data to View                                      | Mobile (React Native)                  |
| **Clean Architecture**            | Domain logic is core; outer layers are replaceable                | Scalable Go backend                    |
| **Hexagonal / Ports and Adapters**| Interface-driven structure with clear external boundaries         | Enterprise Go, microservices           |
| **Feature-based / Modular**        | Code organized by feature                                         | React Native & React frontend          |

---

## 📁 Suggested Folder Structures

### 🔧 Go Backend (Modular + Layered)

```
garage-backend/
├── cmd/                  # Entrypoints (main.go)
├── internal/
│   ├── auth/
│   ├── request/
│   └── customer/
├── pkg/                  # Reusable packages
├── api/                  # REST handlers
├── configs/              # Env/config structs
├── scripts/              # Seeds, jobs
└── test/                 # Mocks, integration tests
```

### 📱 React Native (Feature-based UI)

```
garage-app/
├── src/
│   ├── screens/
│   ├── components/
│   ├── api/
│   ├── store/
│   ├── navigation/
│   └── utils/
└── assets/
```

---

## 🧩 Repo Strategy

| Pattern      | What It Is                                  | Use When                                     |
|--------------|----------------------------------------------|----------------------------------------------|
| **Monorepo** | All apps (web, mobile, backend) in one repo  | Shared logic, solo/team dev, consistent stack|
| **Polyrepo** | Each module in separate repo                 | Larger teams, fully isolated builds          |

---

## 📦 Summary

| Layer              | Terminology                   | Example                      |
|--------------------|-------------------------------|------------------------------|
| App architecture   | MVC, MVVM, Clean               | Logic structuring            |
| Folder layout      | Project structure              | cmd/, src/, shared/          |
| Repo strategy      | Monorepo or Polyrepo           | garage-app/, turbo.json      |

---

## 🛢 SQL & Web Resources

### SQL Tutorials
- [W3Schools SQL](https://www.w3schools.com/sql/default.asp)
- [Quackit SQL Guide](http://www.quackit.com/sql/tutorial/)

### HTML / CSS / JS
- [HTML/CSS/JS - W3Schools](https://www.w3schools.com/html/default.asp)
- [Quackit HTML](http://www.quackit.com/html/)
- [Quackit CSS](http://www.quackit.com/css/tutorial/)
- [Quackit JavaScript](http://www.quackit.com/javascript/tutorial/)
- [Quackit jQuery](http://www.quackit.com/jquery/tutorial/)
- [Quackit JSON](http://www.quackit.com/json/tutorial/)

---

## 📽️ YouTube References (General)
- *(Add your handpicked YouTube videos here for quick access later)*

---

## 🛡️ Licensing
This project is proprietary. All rights reserved.  
You may not use, copy, modify, or distribute any part of this code without explicit permission.

---
