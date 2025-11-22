<!-- portfolio -->
<!-- slug: avalon-team-todo-list -->
<!-- title: Avalon Team - Spring Boot Todo List -->
<!-- description: Todo list web application built with Spring Boot, JPA, Thymeleaf, and Spring Security for OOP course project -->
<!-- image: https://github.com/user-attachments/assets/placeholder-avalon-todo -->
<!-- tags: java, spring-boot, jpa, thymeleaf, spring-security, todo-app, maven -->

# Avalon Team - Spring Boot Todo List Application

A full-featured todo list web application built with Spring Boot framework. This project was developed as a group assignment for the Object-Oriented Programming (PBO - Pemrograman Berbasis Objek) course, demonstrating modern Java web development practices.

## 📋 Overview

This todo list application showcases the powerful Spring Boot ecosystem, implementing CRUD operations with JPA for database management, Thymeleaf for server-side templating, Spring Security for authentication, and Bootstrap for responsive UI design.

## 👥 Team Members (Avalon Team)

- **Daffa Fathan** (4522210082) - [GitHub](https://github.com/daffa09)
- **Antonius Valentino** (4522210109) - [GitHub](https://github.com/AtroxMedaTic)
- **Tegar Gemilang** (4522210095) - [GitHub](https://github.com/TegarGemilang02)
- **Naufal Rizky** (4522210112) - [GitHub](https://github.com/TruePal09)

## ✨ Features

### Core Todo Management
- **Create Tasks**: Add new todo items with title and description
- **View Tasks**: Display all tasks in organized lists
- **Update Tasks**: Edit existing task details
- **Delete Tasks**: Remove completed or unwanted tasks
- **Mark Complete**: Toggle task completion status

### Advanced Features
- **User Authentication**: Secure login/logout with Spring Security
- **User Management**: Individual todo lists per user
- **Persistent Storage**: H2 database integration with JPA
- **Responsive Design**: Mobile-friendly interface with Bootstrap 5
- **Real-time Updates**: Dynamic content with jQuery
- **Form Validation**: Client and server-side validation

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| **Spring Boot** | 2.2.2.RELEASE | Application framework |
| **Spring Data JPA** | - | Database ORM |
| **Spring Security** | - | Authentication & authorization |
| **Thymeleaf** | - | Server-side template engine |
| **H2 Database** | - | In-memory/file database |
| **Bootstrap** | 5.3.2 | Frontend framework |
| **jQuery** | 2.1.4 | JavaScript library |
| **Maven** | - | Build automation |
| **Java** | 11 | Programming language |

## 📁 Project Structure

```
avalon-team/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── guru/springframework/
│   │   │       ├── config/          # Security config
│   │   │       ├── controllers/     # MVC controllers
│   │   │       ├── domain/          # Entity models
│   │   │       ├── repositories/    # JPA repositories
│   │   │       └── services/        # Business logic
│   │   └── resources/
│   │       ├── templates/           # Thymeleaf templates
│   │       ├── static/             # CSS, JS, images
│   │       └── application.properties
│   └── test/                        # Unit tests
├── pom.xml                          # Maven dependencies
├── .editorconfig                    # Editor configuration
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- **Java JDK 11** or higher
- **Maven 3.6+** (or use included Maven wrapper)
- **Git** for version control
- **IDE** (IntelliJ IDEA, Eclipse, or VS Code with Java extensions)

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd avalon-team
   ```

2. **Build with Maven**
   
   Using Maven wrapper (recommended):
   ```bash
   ./mvnw clean install
   ```
   
   Or using installed Maven:
   ```bash
   mvn clean install
   ```

3. **Run the Application**
   
   Using Maven wrapper:
   ```bash
   ./mvnw spring-boot:run
   ```
   
   Or using Maven:
   ```bash
   mvn spring-boot:run
   ```

4. **Access the Application**
   
   Open your browser and navigate to:
   ```
   http://localhost:8080
   ```

### Database Configuration

The application uses H2 database by default:

**H2 Console Access:**
- URL: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (leave empty)

To use a file-based database, update `application.properties`:
```properties
spring.datasource.url=jdbc:h2:file:./data/tododb
spring.jpa.hibernate.ddl-auto=update
```

## 💻 Usage Guide

### Registration & Login

1. **Register New User** (if registration enabled)
   - Navigate to registration page
   - Enter username and password
   - Submit to create account

2. **Login**
   - Use Spring Security login page
   - Enter credentials
   - Access your personal todo list

### Managing Todos

#### Adding a Todo
1. Click "Add New Todo" button
2. Enter task title
3. Add optional description
4. Set priority (if implemented)
5. Click "Save"

#### Viewing Todos
- All todos display on main dashboard
- Filter by status: All, Active, Completed
- Sort by date, priority, or alphabetically

#### Editing a Todo
1. Click "Edit" button on todo item
2. Modify title or description
3. Update priority/due date
4. Click "Update"

#### Completing a Todo
- Click checkbox to mark as complete
- Completed todos show with strikethrough

#### Deleting a Todo
1. Click "Delete" button
2. Confirm deletion in modal
3. Todo removed from list

## 🎨 UI Components

### Main Dashboard
- Todo list display
- Add todo button
- Filter/sort controls
- User menu

### Todo Card
- Title and description
- Completion checkbox
- Edit and delete buttons
- Priority indicator
- Creation date

### Forms
- Add/Edit todo forms
- Input validation
- Error messaging
- Success notifications

## 🔒 Security Features

Spring Security provides:
- **Authentication**: User login system
- **Authorization**: Role-based access control
- **CSRF Protection**: Cross-site request forgery prevention
- **Password Encoding**: BCrypt password hashing
- **Session Management**: Secure session handling

## 🗄️ Database Schema

### Todo Entity
```java
@Entity
public class Todo {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    private String title;
    private String description;
    private boolean completed;
    private LocalDateTime createdAt;
    private LocalDateTime updatedAt;
    
    @ManyToOne
    private User user;
    
    // Getters and setters
}
```

### User Entity
```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    private String username;
    private String password;
    private String role;
    
    @OneToMany(mappedBy = "user")
    private List<Todo> todos;
    
    // Getters and setters
}
```

## 🎓 Learning Objectives

This project demonstrates:

### Object-Oriented Programming
- Class design and encapsulation
- Inheritance and polymorphism
- Interface implementation
- Design patterns (MVC, Repository, Service)

### Spring Framework
- Dependency Injection
- Spring MVC architecture
- Spring Data JPA
- Spring Security basics
- Configuration management

### Web Development
- RESTful principles
- Template engines (Thymeleaf)
- Form handling
- Session management
- Frontend integration

## 🔧 Configuration

### Application Properties

```properties
# Server Configuration
server.port=8080

# Database
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

# H2 Console
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# JPA
spring.jpa.hibernate.ddl-auto=create-drop
spring.jpa.show-sql=true

# Thymeleaf
spring.thymeleaf.cache=false
```

## 🐛 Troubleshooting

**Port Already in Use**
```bash
# Change port in application.properties
server.port=8081
```

**Maven Build Fails**
```bash
# Clear Maven cache
./mvnw clean
rm -rf ~/.m2/repository
./mvnw install
```

**Database Connection Issues**
- Check H2 console settings
- Verify JDBC URL
- Ensure no other instances running

**Login Not Working**
- Check Spring Security configuration
- Verify user exists in database
- Check password encoding

## 🚀 Deployment

### JAR File
```bash
./mvnw clean package
java -jar target/spring-boot-web-0.0.1-SNAPSHOT.jar
```

### Docker
```dockerfile
FROM openjdk:11-jre-slim
COPY target/*.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```

Build and run:
```bash
docker build -t avalon-todo .
docker run -p 8080:8080 avalon-todo
```

## 📚 Resources

- [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- [Spring Data JPA Guide](https://spring.io/guides/gs/accessing-data-jpa/)
- [Thymeleaf Documentation](https://www.thymeleaf.org/documentation.html)
- [Spring Framework Guru](https://springframework.guru) - Tutorial inspiration

## 🙏 Acknowledgments

This project was inspired by tutorials from [Spring Framework Guru](https://springframework.guru) and created as part of the Object-Oriented Programming course at Pancasila University.

## 🤝 Contributing

This is an academic group project. Team members contributions:
- Code reviews through pull requests
- Following Java coding conventions
- Comprehensive documentation
- Unit test coverage

##  📄 License

Created for educational purposes as an OOP course project.

## 💭 Team Notes

Developed collaboratively by Avalon Team for the Object-Oriented Programming course. This project helped us understand Spring Boot ecosystem, team collaboration, and real-world Java web development practices.

---

**Developed by Avalon Team** ✅📝  
Spring Boot Todo List for OOP Course Project!
