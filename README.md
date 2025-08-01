# Gaming Platform

A comprehensive web-based gaming platform built with Java Spring MVC, MyBatis, and MySQL. This platform allows users to browse, purchase, and manage games with features like user authentication, shopping cart functionality, order management, and admin panel.

## 🎮 Features

### User Features
- **User Registration & Authentication**: Secure user registration with email verification
- **Game Browsing**: Browse games by categories, tags, and search functionality
- **Game Details**: View detailed game information including system requirements
- **Shopping Cart**: Add games to cart and manage purchases
- **Order Management**: Track order history and status
- **User Profile**: Manage personal information and preferences
- **Password Recovery**: Email-based password reset functionality

### Admin Features
- **Game Management**: Add, edit, and manage game listings
- **User Management**: Monitor and manage user accounts
- **Order Management**: Process and track orders
- **Category Management**: Organize games by categories and tags
- **System Monitoring**: View platform statistics and logs

### Technical Features
- **Responsive Design**: Modern UI with CSS styling
- **Email Integration**: Automated email notifications
- **Redis Caching**: Performance optimization with Redis
- **File Upload**: Support for game images and assets
- **AOP Logging**: Comprehensive logging with AspectJ
- **Error Handling**: Custom error pages and exception handling

## 🛠 Technology Stack

### Backend
- **Java 19**: Core programming language
- **Spring Framework 5.3.14**: MVC framework, dependency injection, and AOP
- **MyBatis 3.5.6**: Object-relational mapping framework
- **MySQL 8.0**: Database management system
- **Redis**: Caching and session management
- **Apache Commons**: File upload and utility libraries
- **Jackson**: JSON processing for AJAX requests
- **Log4j**: Logging framework

### Frontend
- **JSP**: Server-side templating
- **CSS**: Styling and responsive design
- **JavaScript**: Client-side interactivity
- **AJAX**: Asynchronous data loading

### Build & Deployment
- **Maven**: Build automation and dependency management
- **Tomcat**: Web application server
- **AspectJ**: AOP implementation

## 📋 Prerequisites

Before running this application, ensure you have the following installed:

- **Java JDK 19** or higher
- **Maven 3.6** or higher
- **MySQL 8.0** or higher
- **Redis** (optional, for caching)
- **Tomcat 9** or higher

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd gaming-platform
```

### 2. Database Setup
1. Create a MySQL database named `shop`
2. Import the database schema and sample data:
```bash
mysql -u your_username -p shop < src/main/resources/dbdata.sql
```

### 3. Configure Database Connection
Edit `src/main/resources/jdbc.properties` with your database credentials:
```properties
jdbc.driver=com.mysql.cj.jdbc.Driver
jdbc.url=jdbc:mysql://localhost:3306/shop?useUnicode=true&characterEncoding=utf8&useSSL=false&serverTimezone=UTC
jdbc.username=your_username
jdbc.password=your_password
```

### 4. Configure Email Settings (Optional)
If you want email functionality, configure email settings in the Spring configuration files.

### 5. Build the Project
```bash
mvn clean compile
```

### 6. Deploy to Tomcat
```bash
mvn clean package
```
Copy the generated `target/shop.war` file to your Tomcat `webapps` directory.

### 7. Start the Application
1. Start Tomcat server
2. Access the application at `http://localhost:8080/shop`

## 📁 Project Structure

```
gaming-platform/
├── src/
│   ├── main/
│   │   ├── java/cn/cie/
│   │   │   ├── controller/     # MVC Controllers
│   │   │   ├── entity/         # Data models
│   │   │   ├── mapper/         # MyBatis mappers
│   │   │   ├── services/       # Business logic
│   │   │   ├── utils/          # Utility classes
│   │   │   ├── aop/           # AspectJ aspects
│   │   │   ├── interceptor/   # Spring interceptors
│   │   │   └── event/         # Event handling
│   │   ├── resources/
│   │   │   ├── mapper/        # MyBatis XML mappings
│   │   │   ├── spring-*.xml   # Spring configuration
│   │   │   └── dbdata.sql     # Database initialization
│   │   └── webapp/
│   │       ├── WEB-INF/
│   │       │   ├── jsp/       # JSP pages
│   │       │   ├── css/       # Stylesheets
│   │       │   ├── js/        # JavaScript files
│   │       │   └── image/     # Static images
│   │       └── web.xml        # Web application configuration
│   └── test/                  # Unit tests
├── pom.xml                    # Maven configuration
└── README.md                  # This file
```

## 🎯 Key Components

### Controllers
- `UserController`: User registration, login, and profile management
- `GameController`: Game browsing and details
- `OrderController`: Order processing and management
- `AdminController`: Administrative functions
- `CommonController`: Common functionality and utilities

### Entities
- `User`: User account information
- `Game`: Game details and metadata
- `Order`: Order information
- `OrderItem`: Individual items in orders
- `Kind`: Game categories
- `Tag`: Game tags for classification

### Services
- User management and authentication
- Game catalog and search
- Order processing
- Email notifications
- File upload handling

## 🔧 Configuration

### Spring Configuration Files
- `spring-dao.xml`: Database and MyBatis configuration
- `spring-service.xml`: Service layer configuration
- `spring-web.xml`: Web layer and MVC configuration

### Logging
Configure logging in `log4j-acc.properties` and `log4j-error.properties`

## 🧪 Testing

Run the test suite:
```bash
mvn test
```

## 📝 API Endpoints

### User Management
- `POST /user/register` - User registration
- `POST /user/login` - User login
- `GET /user/profile` - User profile
- `POST /user/update` - Update user information

### Game Management
- `GET /game/list` - List all games
- `GET /game/{id}` - Get game details
- `GET /game/search` - Search games
- `GET /game/category/{id}` - Games by category

### Order Management
- `POST /order/create` - Create new order
- `GET /order/list` - List user orders
- `GET /order/{id}` - Order details

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. Check the existing issues in the repository
2. Create a new issue with detailed information about your problem
3. Include error logs and steps to reproduce the issue

## 🔮 Future Enhancements

- [ ] RESTful API endpoints
- [ ] Mobile application support
- [ ] Payment gateway integration
- [ ] Social media login
- [ ] Game reviews and ratings
- [ ] Recommendation system
- [ ] Multi-language support
- [ ] Advanced search filters

---

**Note**: This is a demonstration project showcasing Java web development with Spring MVC and MyBatis. For production use, additional security measures, performance optimizations, and comprehensive testing should be implemented. 