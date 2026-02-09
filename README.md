# Personal Task Manager

A full-stack web application for managing personal tasks with user authentication, built using Spring Boot and modern web technologies.

### User Management
- **User Registration**: Create new accounts with secure password encryption
- **User Login**: Authenticate using Spring Security
- **Session Management**: Secure session handling with logout functionality

### Task Management
- **Create Tasks**: Add new tasks with title, description, due date, and priority levels
- **Read Tasks**: View all tasks in an organized dashboard
- **Update Tasks**: Edit existing task details and mark tasks as completed
- **Delete Tasks**: Remove tasks that are no longer needed
- **Filter Tasks**: Filter tasks by status (pending, completed)
- **Priority Levels**: Organize tasks by Low, Medium, or High priority
- **Status Tracking**: Track task progress with status updates

### User Interface
- **Responsive Design**: Mobile-friendly interface that works across all devices
- **Dynamic Pages**: Server-side rendering using Thymeleaf templates
- **Intuitive Dashboard**: Clean and organized task overview

## 🛠️ Technologies Used

### Backend
- **Spring Boot** - Application framework
- **Spring MVC** - Web layer and request handling
- **Spring Data JPA** - Database operations and ORM
- **Spring Security** - Authentication and authorization
- **Hibernate** - JPA implementation

### Frontend
- **Thymeleaf** - Server-side template engine
- **HTML5/CSS3** - Structure and styling

### Database
- **MySQL** - Production database (configurable)

### Build Tool
- **Maven** or **Gradle** - Dependency management and build automation

## 📦 Prerequisites

Before running this application, ensure you have the following installed:

- **Java Development Kit (JDK) 17** or higher
- **Maven 3.6+** or **Gradle 7.0+**
- **MySQL 8.0+** (if using MySQL instead of H2)
- **Git** - For version control
- **IDE** (recommended): IntelliJ IDEA, Eclipse, or VS Code

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/personal-task-manager.git
   cd personal-task-manager
   ```

2. **Build the project**
   
   Using Maven:
   ```bash
   mvn clean install
   ```
   
   Using Gradle:
   ```bash
   gradle build
   ```

## ⚙️ Configuration

### Database Configuration

#### Option: MySQL Database (Production)

Add to `application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/taskmanager
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
```

Create the database:
```sql
CREATE DATABASE taskmanager;
```

### Application Properties

Additional configurations in `application.properties`:
```properties
server.port=8080
spring.application.name=Personal Task Manager

# Thymeleaf configuration
spring.thymeleaf.cache=false
spring.thymeleaf.prefix=classpath:/templates/
spring.thymeleaf.suffix=.html

# Security
spring.security.user.name=admin
spring.security.user.password=admin123
```

## ▶️ Running the Application

### Using Maven
```bash
mvn spring-boot:run
```

### Using Gradle
```bash
gradle bootRun
```

### Using JAR
```bash
java -jar target/personal-task-manager-0.0.1-SNAPSHOT.jar
```

The application will start on `http://localhost:8080`

## 📖 Usage

1. **Access the Application**
   - Open your browser and navigate to `http://localhost:8080`

2. **Register a New Account**
   - Click on "Register" from the home page
   - Fill in your details and create an account

3. **Login**
   - Use your credentials to log in

4. **Manage Tasks**
   - **Add Task**: Click "Add New Task" and fill in the details
   - **View Tasks**: See all your tasks on the dashboard
   - **Edit Task**: Click the edit button on any task
   - **Delete Task**: Remove tasks using the delete button
   - **Filter Tasks**: Use filters to view pending or completed tasks
   - **Mark Complete**: Check tasks off as you complete them

5. **Logout**
   - Click the logout button to end your session

## 🔌 API Endpoints

### Authentication
- `GET /` - Home page
- `GET /register` - Registration page
- `POST /register` - Create new user
- `GET /login` - Login page
- `POST /login` - Authenticate user
- `POST /logout` - End session

### Task Management
- `GET /dashboard` - User dashboard
- `GET /tasks` - Get all tasks
- `POST /tasks` - Create new task
- `GET /tasks/{id}` - Get task by ID
- `PUT /tasks/{id}` - Update task
- `DELETE /tasks/{id}` - Delete task
- `GET /tasks/filter?status={status}` - Filter tasks by status

## 📁 Project Structure

```
personal-task-manager/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/yourpackage/taskmanager/
│   │   │       ├── controller/
│   │   │       │   ├── HomeController.java
│   │   │       │   ├── TaskController.java
│   │   │       │   └── UserController.java
│   │   │       ├── model/
│   │   │       │   ├── Task.java
│   │   │       │   └── User.java
│   │   │       ├── repository/
│   │   │       │   ├── TaskRepository.java
│   │   │       │   └── UserRepository.java
│   │   │       ├── service/
│   │   │       │   ├── TaskService.java
│   │   │       │   └── UserService.java
│   │   │       ├── security/
│   │   │       │   └── SecurityConfig.java
│   │   │       └── TaskManagerApplication.java
│   │   └── resources/
│   │       ├── templates/
│   │       │   ├── home.html
│   │       │   ├── login.html
│   │       │   ├── register.html
│   │       │   ├── dashboard.html
│   │       │   └── task-form.html
│   │       ├── static/
│   │       │   ├── css/
│   │       │   ├── js/
│   │       │   └── images/
│   │       └── application.properties
│   └── test/
│       └── java/
├── pom.xml (or build.gradle)
└── README.md
```



Project Link: [https://github.com/yourusername/personal-task-manager](https://github.com/yourusername/personal-task-manager)

---

**Happy Task Managing! 📝✅**
