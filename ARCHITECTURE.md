
# DevTrack — Architecture

## 1. Architectural Style

Modular Monolith.

The application will initially be developed as one deployable backend application, organized into independent business modules.

## 2. Technology Choices

| Concern | Technology |
|---|---|
| Programming language | Go |
| HTTP server | net/http |
| API style | REST |
| Database | PostgreSQL |
| Database driver | pgx |
| API documentation | OpenAPI / Swagger |
| Authentication | Server-side sessions |
| Password hashing | Argon2id |
| Testing | Go testing |
| Containerization | Docker |

## 3. Main Modules

- Identity
- Projects
- Tasks
- Collaboration
- Learning
- Notifications
- Analytics

## 4. Application Layers

- HTTP layer: routing, middleware, request handling.
- Application layer: use cases and business rules.
- Infrastructure layer: database and external integrations.

## 5. Database

PostgreSQL will be the primary relational database.

Database schema changes will be managed through migrations.

## 6. API

- RESTful endpoints.
- JSON request and response bodies.
- URL versioning: /api/v1.
- Consistent error responses.
- OpenAPI documentation.

## 7. Security

- Passwords hashed with Argon2id.
- Server-side session management.
- Role-based authorization.
- Input validation.
- CSRF protection for cookie-authenticated state-changing requests.
