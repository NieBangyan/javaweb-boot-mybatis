# Javaweb-boot-mybatis

## Tech Stack
Springboot 4.0.6

MyBatis 4.0.1

MySQL 8.0+

Java 17

Maven 3.8+

## Project Introduction
A Spring Boot 4.0 + MyBatis user management and file upload system.
 
## Project Structure
ˋˋˋbush
javaweb-boot-03-mybatis/
├── src/main/java/com/woxueit/boot/
│   ├── config/
│   │   └── WebConfig.java              # CORS & file upload config
│   ├── controller/
│   │   ├── UploadController.java       # File upload API
│   │   └── UserController.java         # User CRUD API
│   ├── mapper/
│   │   ├── UserMapper.java             # Data access interface
│   │   └── UserMapper.xml              # MyBatis SQL mappings
│   ├── pojo/
│   │   ├── Dept.java                   # Department entity
│   │   └── User.java                   # User entity
│   ├── service/
│   │   ├── UserService.java            # Business logic interface
│   │   └── UserServiceImpl.java        # Business logic implementation
│   ├── utils/
│   │   └── CommonResult.java           # Unified response wrapper
│   └── JavawebBoot03MybatisApplication.java  # Main entry point
├── src/main/resources/
│   ├── static/                         # Static assets
│   ├── templates/                      # Template files
│   └── application.properties          # App configuration
├── uploads/                            # Uploaded files directory
├── test/                               # Test directory
├── target/                             # Compiled output
├── pom.xml                             # Maven dependencies
├── .gitignore
└── mvnw / mvnw.cmd                     # Maven Wrapper scripts
ˋˋˋ
## API Endpoints

| Function | Method | Endpoint | Parameters | Response Format |
|----------|--------|----------|------------|-----------------|
| Create User | POST | `/user` | JSON body | `CommonResult` |
| Update User | PUT | `/user` | JSON body | `CommonResult` |
| Delete User | DELETE | `/user/{id}` | Path variable `id` | `CommonResult` |
| Get User By ID | GET | `/user/{id}` | Path variable `id` | `CommonResult` |
| Get All Users | GET | `/user` | None | `CommonResult` |
| Upload File | POST | `/upload` | `multipart/form-data` | `CommonResult` |

## The problem I met
#### 1.MyBatis BindingException
<img height="200" alt="image" src="https://github.com/user-attachments/assets/f6903f4d-84ba-4cbc-b4bb-9ce3fd67f4d7" />

### Reason

### Solution
