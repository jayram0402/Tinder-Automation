# Tinder-Automation
Developed an AI-powered Dating app with a Spring Boot backend, featuring AI-driven swiping, matching, profile creation, image generation, and conversation automation, with a React frontend.

## AI-Powered Dating App

This repository contains the source code for an AI-powered dating application with an AI-driven swiping system, matching algorithm, profile creation, image generation, and automated conversation management. The backend is built using **Spring Boot**, and the frontend uses **React**.

## Features

- **AI-Driven Swiping and Matching**: AI algorithms to recommend and match users based on their preferences.
- **Profile Creation with Image Generation**: Automated profile creation with an AI-powered image generation feature.
- **Real-time Conversations**: Automated conversation starter and response system.
- **Emergency Features**: Swift backend and frontend communication for quick responses.
- **Cloud Deployment**: Deployed on **AWS**, ensuring a scalable infrastructure with high availability.

## Technologies Used

### Backend
- **Java** with **Spring Boot** for RESTful API development
- **MongoDB** for database management
- **Docker** for containerization
- **Jenkins** for CI/CD pipelines
- **AWS** for deployment and cloud services
- **Ansible** & **Terraform** for infrastructure automation
- **Ollama** for LLM integration
- **Git** for version control

### Frontend
- **React** for building user interfaces
- **JavaScript (ES6)** for client-side functionality

---

## Installation and Setup

### Prerequisites

Ensure that you have the following installed:

- **Java 11+** for backend development
- **Node.js** and **npm** for frontend development
- **MongoDB** (local or cloud instance)
- **Docker** (if using containerization)
- **Git** for version control

---

## Backend Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/jayram0402/Tinder-Automation.git
   cd Tinder-Automation/
   ```

2. **Configure MongoDB**:
   In the `application.properties` file (`src/main/resources/application.properties`), update the MongoDB URI to point to your local or cloud MongoDB instance:
   ```properties
   spring.data.mongodb.uri=mongodb://localhost:27017/tinderdb
   ```

3. **Build the Backend**:
   Run the following command to build the backend using Maven Wrapper:
   ```bash
   ./mvnw clean install
   ```

4. **Run the Application**:
   Start the Spring Boot application:
   ```bash
   ./mvnw spring-boot:run
   ```

5. **Swagger API Documentation**:
   After starting the backend, visit `http://localhost:8080/swagger-ui.html` for the API documentation and interactive testing.

6. **Optional Docker Setup**:
   To run the backend in a Docker container:
   ```bash
   docker build -t tinder-backend .
   docker run -p 8080:8080 tinder-backend
   ```

### AWS, Jenkins, and CI/CD Setup

1. **Jenkins for CI/CD**:
   Use **Jenkins** to automate testing and deployment of your code. Configure pipelines to automatically build and deploy changes.

2. **AWS Deployment**:
   Deploy the backend to **AWS EC2** or use **Elastic Beanstalk** for easy scalability. Ensure the **RDS** (Relational Database Service) is properly set up for MongoDB, if applicable.

3. **Infrastructure Automation with Ansible & Terraform**:
   Automate your infrastructure setup using **Terraform** for provisioning resources and **Ansible** for configuration management.

---

## Frontend Setup

1. **Navigate to the Frontend**:
   ```bash
   cd ../frontend
   ```

2. **Install Dependencies**:
   Run the following command to install all the necessary dependencies for the React app:
   ```bash
   npm install
   ```

3. **Configure API Endpoints**:
   Update the API URLs in the React app to point to your backend:
   ```javascript
   const apiUrl = "http://localhost:8080/api"; // Or your deployed backend URL
   ```

4. **Run the Frontend**:
   Start the development server:
   ```bash
   npm start
   ```
   The frontend will be available at `http://localhost:3000`.

5. **Build for Production**:
   To create a production build, use the following command:
   ```bash
   npm run build
   ```

6. **Optional Docker Setup for Frontend**:
   Build and run the frontend using Docker:
   ```bash
   docker build -t tinder-frontend .
   docker run -p 3000:3000 tinder-frontend
   ```

---

## Database Setup

- Use **MongoDB** as the primary database to store user data, conversations, matches, etc. You can host MongoDB locally or use **MongoDB Atlas** for cloud-based services.
- The database schema is automatically handled by Spring Boot through the `@Document` annotation in the entities.

---

## API Endpoints

Here is a brief list of API endpoints available:

- **POST /api/users**: Register a new user
- **GET /api/match**: Get match suggestions for the user
- **GET /api/conversations**: Retrieve conversations between matched users
- **POST /api/images/generate**: Generate profile images using AI

You can interact with these endpoints directly or use the **Swagger UI** for testing.

---

## Deployment

### AWS EC2 Setup

To deploy the backend on an **AWS EC2** instance:

1. Launch an EC2 instance with Java installed.
2. Pull your code from GitHub, build, and run the backend.
3. Set up a security group to allow traffic on port **8080**.

### CI/CD with Jenkins

Set up a **Jenkins** pipeline that automates testing and deployment to the cloud. Configure your Jenkinsfile to pull from the GitHub repository and build the project with Maven.

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.

---

## Contributing

We welcome contributions! Feel free to submit issues and pull requests for bug fixes, features, and improvements.

 

