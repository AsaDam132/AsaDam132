# TurogTechnologies - Customer Account Management API

This is a **Spring Boot REST API** for managing customers and their bank accounts.  
It allows you to:

- Create customers  
- Create accounts for customers  
- View customers and accounts  
- Deposit and withdraw money from accounts  

---

## 🛠 Tech Stack
- Java 17
- Spring Boot 3.5.6
- Spring Data JPA
- Spring Web
- Lombok
- MySQL

---

## 📌 Endpoints

### Customers
- **Create Customer**  
  `POST /api/customers`  
  **Request Body (JSON):**
  ```json
  {
    "firstname": "John",
    "lastname": "Doe",
    "email": "john.doe@example.com",
    "phonenumber": "1234567890"
  }
Get Customer by ID
GET /api/customers/{id}

Accounts
Create Account for a Customer
POST /api/accounts?customerId=1&accountNumber=1234567890

Get Account by ID
GET /api/accounts/{id}

Transactions
Deposit Money
PATCH /api/{accountId}/deposit?amount=500

Withdraw Money
PATCH /api/accounts/{id}/withdraw?amount=200

▶️ Running the Project
Clone the repo:

bash
Copy code
git clone https://github.com/AsaDam132/AsaDam132.git
Open in your IDE (IntelliJ, Eclipse, or VS Code).

Configure MySQL database in application.properties:

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/turog_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
Run the project:

bash
Copy code
mvn spring-boot:run
Test endpoints with Postman or cURL.

📖 Example Flow
Create a customer (POST /api/customers)

Create an account for that customer (POST /api/accounts)

Deposit money (PATCH /api/{accountId}/deposit)

Withdraw money (PATCH /api/accounts/{id}/withdraw)

✅ Status
This is a basic demo API for educational purposes.
You can extend it with:

Authentication (Spring Security + JWT)

Transaction history tracking

Multiple account types

👩🏽‍💻 Author
Damilola Asaolu
GitHub: AsaDam132
