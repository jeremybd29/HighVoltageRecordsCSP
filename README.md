// EasyShop API

// Overview

EasyShop is a Spring Boot REST API that simulates the backend of an e-commerce application. Users can browse products and categories, while authenticated users and administrators have access to additional functionality such as managing products, categories, and shopping carts.

This project was built using Java, Spring Boot, Spring Security, JWT Authentication, MySQL, JPA/Hibernate, and RESTful API principles.

## Technologies Used

- Java
- Spring Boot<img width="1440" height="900" alt="Screenshot 2026-06-25 at 5 56 44 PM" src="https://github.com/user-attachments/assets/5979af25-fecb-46ee-9862-1de458d106b3" />
<img width="1440" height="900" alt="Screenshot 2026-06-25 at 5 55 52 PM" src="https://github.com/user-attachments/assets/4dbe47fa-e2ce-4e5d-9832-8911f3154914" />
<img width="1440" height="900" alt="Screenshot 2026-06-25 at 5 53 24 PM" src="https://github.com/user-attachments/assets/2b8e02dc-0fb4-43d8-9b7f-3e46554359a8" />

- JWT Authentication
- MySQL
- Maven
- Insomnia
- Git & GitHub

---

## Features

### Products
- View all products
- Search products
- Filter by category
- Filter by price range
- Create products (Admin)
- Update products (Admin)
- Delete products (Admin)

### Categories
- View categories
- View products within a category
- Create categories (Admin)
- Update categories (Admin)
- Delete categories (Admin)

### Shopping Cart
- View shopping cart
- Add products
- Update quantities
- Remove products
- Clear cart

---

## API Testing

The API was tested using Insomnia.

Authentication is handled through JWT tokens.

Regular users are prevented from accessing administrator endpoints.

---

## Project Structure

Controllers
Services
Repositories
Models
Security
JWT
Database

---

## Interesting Code

One of the most interesting parts of this project is the role-based authorization using Spring Security.

Admin endpoints are protected using:

```java
@PreAuthorize("hasRole('ROLE_ADMIN')")
```

while public endpoints use

```java
@PreAuthorize("permitAll()")
```

This ensures only authorized users can modify products and categories while allowing everyone to browse the store.

---

## Future Improvements

- Finish shopping cart edge cases
- Add frontend application
- Product images
- User order history
- Checkout system
