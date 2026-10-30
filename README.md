# Dream Shop 🛒

A Spring Boot-based e-commerce backend service designed to manage products, categories, inventory, and product media.

---

## 🚀 Features

- **Product Management:** Manage catalog items with attributes like name, brand, description, price, and inventory tracking.
- **Category Hierarchy:** Organize products into relational categories.
- **Image & Media Storage:** Upload and link product images directly stored or referenced with metadata.
- **JPA / Hibernate ORM:** Automatic schema generation and relational mappings (`OneToMany`, `ManyToOne`).

---

## 🛠️ Tech Stack

- **Language:** Java 17+
- **Framework:** [Spring Boot](https://spring.io/projects/spring-boot)
- **Data Persistence:** Spring Data JPA, Hibernate ORM
- **Database:** PostgreSQL (or MySQL / SQL Server)
- **Productivity Tools:** [Project Lombok](https://projectlombok.org/)
- **Build Tool:** Apache Maven (with Maven Wrapper `mvnw`)

---

## 📋 Prerequisites

Before running the project, ensure you have:

- **Java Development Kit (JDK):** Version 17 or higher installed (`java -version`)
- **Database:** PostgreSQL Server installed and running locally on port `5432` (or configured remotely)
- **Git:** For version control

---

## ⚙️ Configuration

Configure your database connection and server port in [`src/main/resources/application.properties`](src/main/resources/application.properties):

```properties
spring.application.name=dream-shop
server.port=9193

# PostgreSQL Database configuration
spring.datasource.url=jdbc:postgresql://localhost:5432/dream_shop_db
spring.datasource.username=postgres
spring.datasource.password=your_password
spring.datasource.driver-class-name=org.postgresql.Driver

# JPA / Hibernate
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.hibernate.ddl-auto=update
```

> **Note:** Make sure to replace `your_password` with your actual PostgreSQL database password, and create a database named `dream_shop_db` in DBeaver / pgAdmin.

---

## 🏃 Getting Started

### 1. Clone the repository
```bash
git clone <repository-url>
cd dream-shop
```

### 2. Run the application

Using the bundled **Maven Wrapper**:

- **macOS / Linux:**
  ```bash
  ./mvnw spring-boot:run
  ```
- **Windows (Command Prompt / PowerShell):**
  ```cmd
  mvnw.cmd spring-boot:run
  ```

Once started, the application will be listening on:
```
http://localhost:9193
```

---

## 🔨 Useful Maven Commands

| Command | Description |
|---|---|
| `./mvnw clean compile` | Clean build files and compile the source code |
| `./mvnw test` | Execute unit and integration tests |
| `./mvnw clean package` | Build the deployable executable `.jar` in `target/` |
| `java -jar target/dream-shop-0.0.1-SNAPSHOT.jar` | Run the packaged JAR directly |

---

## 📂 Project Structure

```text
dream-shop/
├── src/
│   ├── main/
│   │   ├── java/com/dailycodework/dream_shop/
│   │   │   ├── model/                  # JPA entities (Category, Product, Image)
│   │   │   └── DreamShopApplication.java # Spring Boot main entry point
│   │   └── resources/
│   │       ├── application.properties  # Application and DB properties
│   │       └── static/ & templates/
│   └── test/                           # Unit and integration tests
├── .mvn/                               # Maven wrapper configuration
├── mvnw & mvnw.cmd                     # Maven wrapper scripts
└── pom.xml                             # Project dependencies and build configuration
```

---

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any features, bug fixes, or enhancements.

