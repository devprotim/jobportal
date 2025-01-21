# Job Board Application

A full-featured job board platform built with Spring Boot that connects employers and job seekers. The application provides a robust platform for posting jobs, searching positions, and managing applications.

## 🚀 Features

- **For Employers:**
  - Post and manage job listings
  - Review and track applications
  - Manage company profile
  - Access applicant information
  - Dashboard with analytics

- **For Job Seekers:**
  - Search and filter job listings
  - Easy application process
  - Profile and resume management
  - Track application status
  - Save favorite jobs

## 🛠️ Technical Stack

- **Backend:**
  - Java 17
  - Spring Boot 3.x
  - Spring Security
  - Spring Data JPA
  - PostgreSQL
  - Hibernate
- **Frontend:**
  - Angular 16
  - Bootstrap 5
  - Jasmin 4.6
  - Karma 6.4

- **Security:**
  - JWT Authentication
  - Role-based authorization
  - Password encryption

- **Storage:**
  - AWS S3 for resume storage
  - Database for user data and job listings

## 📋 Prerequisites

- JDK 17 or later
- Maven 3.6+
- PostgreSQL 12+
- AWS Account (for S3 storage)

## 🔧 Configuration

1. Clone the repository:
```bash
git clone https://github.com/yourusername/job-board.git
cd job-board
```

2. Configure database in `application.properties`:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/jobboard
spring.datasource.username=your_username
spring.datasource.password=your_password
```

3. Configure AWS credentials:
```properties
aws.access.key.id=your_access_key
aws.secret.access.key=your_secret_key
aws.s3.bucket=your_bucket_name
```

## 🚀 Running the Application

1. Build the project:
```bash
mvn clean install
```

2. Run the application:
```bash
mvn spring-boot:run
```

The application will be available at `http://localhost:8080`

## 📝 API Documentation

### Jobs

```
GET /api/jobs - List all jobs
GET /api/jobs/search - Search jobs with filters
POST /api/jobs - Create a new job posting
GET /api/jobs/{id} - Get job details
PUT /api/jobs/{id} - Update job posting
DELETE /api/jobs/{id} - Delete job posting
```

### Applications

```
POST /api/jobs/{id}/apply - Apply for a job
GET /api/applications - List user's applications
GET /api/applications/{id} - Get application details
PUT /api/applications/{id} - Update application status
```

### Users

```
POST /api/auth/register - Register new user
POST /api/auth/login - User login
GET /api/users/profile - Get user profile
PUT /api/users/profile - Update user profile
```

## 🔒 Security

- JWT-based authentication
- Password encryption using BCrypt
- Role-based access control (EMPLOYER, JOB_SEEKER, ADMIN)
- Secure file upload handling

## 🗄️ Database Schema

The application uses the following main entities:
- Users (both employers and job seekers)
- Jobs
- Applications
- Companies
- Skills
- Categories

## 🔄 Future Enhancements

- [ ] Advanced search with filters
- [ ] Email notifications
- [ ] Resume parser
- [ ] Interview scheduling
- [ ] Job recommendations
- [ ] Analytics dashboard
- [ ] Mobile application

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## 👥 Authors

- Your Name - *Initial work* - [YourGithub](https://github.com/yourusername)

## 🙏 Acknowledgments

- Spring Boot Documentation
- AWS Documentation
- PostgreSQL Documentation

## 📧 Contact

Your Name - your.email@example.com

Project Link: [https://github.com/yourusername/job-board](https://github.com/yourusername/job-board)
