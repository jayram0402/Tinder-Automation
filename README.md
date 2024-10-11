# 🚀 Tinder-Automation - Dating App
**Developed an AI-powered dating application featuring an intelligent swiping system, matching algorithm, profile creation, image generation, and conversation automation. The backend is powered by Spring Boot, while the frontend utilizes React.**

![Tinder-Automation Logo](https://upload.wikimedia.org/wikipedia/en/thumb/a/a0/Tinder_logo.svg/1200px-Tinder_logo.svg.png) <!-- Tinder app logo -->

---

## 💡 Overview

This repository contains the source code for an **AI-Powered Dating Application** that utilizes advanced algorithms for a seamless user experience. With features like AI-driven swiping and automated conversation management, this application aims to enhance the way users connect.

---

## 📈 Key Features

- **AI-Driven Swiping & Matching**: Tailored user recommendations based on individual preferences using sophisticated AI algorithms.
- **Profile Creation with AI Image Generation**: Automatically create profiles complemented by AI-generated images, ensuring a personalized touch.
- **Real-time Conversations**: An automated system for initiating and managing conversations, making interactions smoother.
- **Emergency Features**: Rapid communication between the backend and frontend for immediate user support.
- **Cloud Deployment**: Hosted on **AWS** to guarantee scalability and high availability.

---

## 🛠️ Technologies Used

### Backend
- ☕ **Java** with **Spring Boot** for RESTful API development
- 🗄️ **MongoDB** for database management
- 🐳 **Docker** for containerization
- 🔧 **Jenkins** for CI/CD pipelines
- ☁️ **AWS** for cloud services
- ⚙️ **Ansible** & **Terraform** for infrastructure automation
- 🧠 **Ollama** for LLM integration
- 🥇 **Git** for version control

### Frontend
- ⚛️ **React** for dynamic user interfaces
- 📜 **JavaScript (ES6)** for interactive client-side functionality

---

## 📦 Installation and Setup

### Prerequisites

Ensure you have the following installed:

- **Java 11+** for backend development
- **Node.js** and **npm** for frontend development
- **MongoDB** (local or cloud instance)
- **Docker** (if using containerization)
- **Git** for version control

---

### 🚀 Backend Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/jayram0402/Tinder-Automation.git
   cd Tinder-Automation/
   ```

2. **Configure MongoDB**:
   In `src/main/resources/application.properties`, update the MongoDB URI:
   ```properties
   spring.data.mongodb.uri=mongodb://localhost:27017/tinderdb
   ```

3. **Build the Backend**:
   Use the Maven Wrapper to build the backend:
   ```bash
   ./mvnw clean install
   ```

4. **Run the Application**:
   Start the Spring Boot application:
   ```bash
   ./mvnw spring-boot:run
   ```

5. **API Documentation**:
   Access Swagger UI at `http://localhost:8080/swagger-ui.html` for API interaction and testing.

6. **Optional Docker Setup**:
   To run the backend in a Docker container:
   ```bash
   docker build -t tinder-backend .
   docker run -p 8080:8080 tinder-backend
   ```

---

### ☁️ AWS, Jenkins, and CI/CD Setup

1. **Jenkins for CI/CD**: 
   Automate testing and deployment. Configure Jenkins pipelines for continuous integration and delivery.

2. **AWS Deployment**: 
   Deploy the backend on **AWS EC2** or **Elastic Beanstalk** for scalability. Ensure **RDS** (if applicable) is properly set up for MongoDB.

3. **S3 for Static Files**: 
   Host static assets (images, CSS, JS) in **Amazon S3**:
   - Create an S3 bucket via the AWS Management Console.
   - Upload static files from your React app's build folder.
   - Configure CORS for frontend access.

4. **Infrastructure Automation with Ansible & Terraform**:
   Automate infrastructure setup for ease of management.

5. **EC2 Instance Setup**:
   Deploy your application on an **AWS EC2** instance:
   - **Instance Type**: Choose based on your needs (e.g., `t2.micro` for low traffic).
   - **Security Groups**: Configure inbound rules to allow traffic on port **8080**.
   - **Elastic IP**: Use for a static public IP address.
   - **VPC**: Deploy within a Virtual Private Cloud for enhanced security.

---

### 🎨 Frontend Setup

1. **Navigate to the Frontend**:
   ```bash
   cd ../frontend
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Configure API Endpoints**:
   Update API URLs in your React app:
   ```javascript
   const apiUrl = "http://localhost:8080/api"; // Or your deployed backend URL
   ```

4. **Run the Frontend**:
   Start the React development server:
   ```bash
   npm start
   ```
   Access the frontend at `http://localhost:3000`.

5. **Build for Production**:
   To create a production build:
   ```bash
   npm run build
   ```

6. **Optional Docker Setup for Frontend**:
   ```bash
   docker build -t tinder-frontend .
   docker run -p 3000:3000 tinder-frontend
   ```

---

### 🗄️ Database Setup

- Use **MongoDB** as the primary database for user data, matches, and conversations.
- Schema management is handled by Spring Boot with the `@Document` annotation.

---

### 🔌 API Endpoints

Here’s a brief overview of the available API endpoints:

- 🆕 **POST /api/users**: Register a new user
- 💡 **GET /api/match**: Retrieve match suggestions
- 💬 **GET /api/conversations**: Access conversations between users
- 📸 **POST /api/images/generate**: Generate AI profile images

Interact with these endpoints via the **Swagger UI**.

---

## 🌐 Deployment

### AWS EC2 Setup

To deploy on an **AWS EC2** instance:

1. Launch an instance with Java installed.
2. Pull your code, build, and run the backend.
3. Set up security groups to allow traffic on port **8080**.

### CI/CD with Jenkins

Set up a Jenkins pipeline to automate testing and deployment, pulling changes from GitHub and building the project with Maven.

---

## 📜 License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.

---

## 🤝 Contributing

We welcome contributions! Feel free to submit issues and pull requests for bug fixes, features, and improvements.

---

**Thank you for checking out the Tinder-Automation project! Happy journey!** 🚀
