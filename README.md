
# Student Registration System (Spring Boot + Thymeleaf)

A simple student registration system built using **Spring Boot**, **Thymeleaf**, and **file-based storage**. This application allows you to add, view, edit, and delete student records.

## Features

- Add new students
- View all registered students
- Edit existing student details
- Delete students
- File-based persistent storage (no database required)

---

---

## 📁 Project Structure

```
student-registration/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/registration/
│   │   │       └── RegistrationApplication.java
│   │   └── resources/
│   │       ├── templates/
│   │       │   ├── index.html
│   │       │   └── students.html
│   │       └── application.properties
├── students.txt
└── pom.xml
```

---

## 🛠️ Prerequisites

- Java (JDK 17 or above)
- Maven (see installation below)

---

## 📦 Installing Maven

### 🔧 For macOS:

1. Install [Homebrew](https://brew.sh/) if not already installed:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. Install Maven:
   ```bash
   brew install maven
   ```

3. Verify Maven installation:
   ```bash
   mvn -v
   ```

---

### 🪟 For Windows:

1. Download the latest Maven binary zip from [Apache Maven Downloads](https://maven.apache.org/download.cgi).

2. Extract the downloaded ZIP file to a directory (e.g., `C:\Program Files\Apache\Maven`).

3. Set environment variables:
   - `MAVEN_HOME`: path to your Maven folder
   - Add `%MAVEN_HOME%\bin` to your system's `Path`

4. Verify Maven installation:
   ```cmd
   mvn -v
   ```

---

## 🚀 Running the Project

### Step 1: Clone or Download the Project

Unzip or clone the project from your repository/folder.

```bash
cd student-registration
```

### Step 2: Run with Maven

```bash
mvn spring-boot:run
```

> If port `8080` is already in use, change the port in `src/main/resources/application.properties`:
```properties
server.port=8081
```

---

## 🌐 Access the Application

Once the application is running, visit:

```
http://localhost:8080/
```

### Example Endpoints:
- `GET /` - Home Page
- `GET /students` - List all students
- `GET /students/new` - Form to add a new student
- `POST /students` - Submit a new student
- `GET /students/edit/{id}` - Edit a student
- `POST /students/update/{id}` - Update a student
- `GET /students/delete/{id}` - Delete a student

---

## 📁 File-based Storage

All student data is saved in a simple text file under:
```
src/main/resources/students.txt
```

Each record is stored as a line with comma-separated values:
```
id,name,email,course
```

---

## 🧑‍💻 Technologies Used

- Java
- Spring Boot
- Thymeleaf
- Maven
- File I/O

---


