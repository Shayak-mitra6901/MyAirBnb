# AirBnB App

A Spring Boot-based backend application for an AirBnB-like platform, providing hotel and room management, booking, user authentication, and payment integration.

## Features
- User authentication and authorization (JWT-based)
- Hotel and room management (CRUD operations)
- Hotel browsing and search
- Room booking and inventory management
- Stripe payment integration
- Webhook support for payment events
- RESTful API endpoints (under `/api/v1`)

## Technologies Used
- Java 21+
- Spring Boot
- Spring Data JPA (Hibernate)
- PostgreSQL
- Stripe API
- JWT for security

## Getting Started

### Prerequisites
- Java 21 or higher
- Maven
- PostgreSQL database

### Configuration
All sensitive configuration is managed via environment variables. Example `application.properties`:

```properties
spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
jwt.secretKey=${JWT_SECRET_KEY}
frontend.url=${FRONTEND_URL}
stripe.secret.key=${STRIPE_SECRET_KEY}
stripe.webhook.secret=${STRIPE_WEBHOOK_SECRET}
```

Set these environment variables in your deployment environment or CI/CD pipeline (e.g., GitHub Actions).

### Build & Run

```bash
mvn clean install
java -jar target/airBnbApp-0.0.1-SNAPSHOT.jar
```

The API will be available at `http://localhost:8080/api/v1` (or as configured).

## API Endpoints
- `/api/v1/auth/*` – Authentication endpoints
- `/api/v1/hotels/*` – Hotel management
- `/api/v1/rooms/*` – Room management
- `/api/v1/bookings/*` – Booking operations
- `/api/v1/webhook/*` – Stripe webhook

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License.

