
# BookAPI - Book Management REST API

A simple Spring Boot REST API for managing books. This project demonstrates CRUD operations with an H2 in-memory database and is designed for easy testing and extension.

---

## Features

- **CRUD operations** for books: Create, Read, Update, Delete  
- Uses **Spring Data JPA** with **Hibernate** (as the default JPA implementation) for database interaction  
- **H2 in-memory database** for quick setup and testing  
- Clean REST endpoints following best practices  
- Thoroughly tested using **Postman**  

---

## API Endpoints

| Method | Endpoint       | Description               |
|--------|----------------|---------------------------|
| GET    | `/books`       | Retrieve all books         |
| GET    | `/books/{id}`  | Retrieve a book by ID      |
| POST   | `/books`       | Create a new book          |
| PUT    | `/books/{id}`  | Update an existing book    |
| DELETE | `/books/{id}`  | Delete a book by ID        |

---

## Testing

The API endpoints were tested with **Postman** to ensure proper functionality and handling of different scenarios, including:  
- Adding new books  
- Retrieving all or single books  
- Updating existing books  
- Deleting books  

You can use Postman or any HTTP client (like curl) to interact with the API.

---

## Getting Started

### Prerequisites

- Java 17+  
- Maven

### Run Locally

1. Clone the repository  
   ```bash
   git clone https://github.com/freshuno/bookapi.git
   ```
2. Build and run the application  
   ```bash
   ./mvnw spring-boot:run
   ```
3. Access the API at:  
   ```
   http://localhost:8080/home
   ```

---

## Usage Example

### Add a new book (POST)

Request URL: `http://localhost:8080/books`  
Body (JSON):
```json
{
  "title": "The Lord of the Rings",
  "author": "J.R.R. Tolkien",
  "publicationYear": 1954
}
```

Response:
```json
{
  "id": 1,
  "title": "The Lord of the Rings",
  "author": "J.R.R. Tolkien",
  "publicationYear": 1954
}
```
