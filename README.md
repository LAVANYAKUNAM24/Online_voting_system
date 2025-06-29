# Online Voting System

An online voting platform built with Spring Boot, MongoDB, and Thymeleaf. This application allows voters to register, log in, and cast their votes securely. Admins can manage candidates, view analytics, and monitor election results.

## Features

- **Voter Registration & Login:** Secure registration and authentication for voters.
- **Admin Dashboard:** Manage candidates, view voter lists, and monitor voting analytics.
- **Candidate Management:** Add, edit, and delete candidates with party symbols and photos.
- **Voting Window:** Voting is only allowed within a configurable time window.
- **Result Publication:** Results are available to the public 30 minutes after voting ends.
- **Responsive UI:** User-friendly and mobile-responsive design using Thymeleaf templates.
- **File Uploads:** Secure upload and serving of candidate images and party symbols.

## Technologies Used

- Java 17
- Spring Boot 3.x
- Spring Security
- Spring Data MongoDB
- Thymeleaf
- Maven

## Getting Started

### Prerequisites

- Java 17+
- Maven
- MongoDB (cloud or local instance)

### Configuration

Edit `src/main/resources/application.properties` to set your MongoDB URI and voting window:

```properties
spring.data.mongodb.uri=YOUR_MONGODB_URI
voting.start=YYYY-MM-DDTHH:MM:SS
voting.deadline=YYYY-MM-DDTHH:MM:SS
server.port=8091
```

### Build & Run

```sh
mvn clean install
mvn spring-boot:run
```

The application will be available at [http://localhost:8091](http://localhost:8091).

## Usage

- **Home Page:** `/`
- **Voter Registration:** `/voter/register`
- **Voter Login:** `/voter/login`
- **Admin Login:** `/admin/login`
- **Admin Dashboard:** `/admin/dashboard`
- **Public Results:** `/results`

## Project Structure

- `src/main/java/com/example/demo/Controller/` - Controllers for admin, voter, and public endpoints
- `src/main/java/com/example/demo/Entity/` - Entity classes for MongoDB
- `src/main/java/com/example/demo/Repository/` - Spring Data repositories
- `src/main/java/com/example/demo/Service/` - Business logic services
- `src/main/resources/templates/` - Thymeleaf HTML templates
- `uploads/` - Uploaded images for candidates and parties

## Security

- Admin and voter sessions are separated.
- Passwords are currently stored in plain text (for demo purposes). **For production, implement password hashing.**

## License

This project is for educational/demo purposes.

## Contact

For questions or support, please contact:  
**Lavanya Kunam**  
Email: [lavanyakunam29@gmail.com](mailto:lavanyakunam29@gmail.com)
