# Money Manager - Fullstack Application

A comprehensive fullstack money management application built with React and Spring Boot.

## Features

- User registration and login (auto-activated)
- JWT-based authentication
- Income and expense tracking
- Category management with emoji support
- Dashboard with charts and financial overview
- Excel report generation and download
- Responsive UI with Tailwind CSS

## Tech Stack

### Backend
- Java 21
- Spring Boot 3.2.0
- Spring Security with JWT
- Spring Data JPA
- MySQL
- Apache POI (Excel generation)

### Frontend
- React 18
- Vite
- Tailwind CSS
- React Router
- Axios
- Recharts (data visualization)
- Emoji Picker React
- Lucide React (icons)
- Moment.js (date formatting)

## Prerequisites

- JDK 21
- Maven 3.9+
- Node.js 18+
- MySQL 8.0+

## Quick Setup

### 1. Database Setup

Create MySQL database:
```sql
CREATE DATABASE money_manager;
```

### 2. Backend Configuration

Update `backend/src/main/resources/application.properties`:
```properties
spring.datasource.username=YOUR_MYSQL_USERNAME
spring.datasource.password=YOUR_MYSQL_PASSWORD
```

### 3. Run Backend

Open Command Prompt:
```bash
cd backend
"C:\Program Files\Apache\maven\bin\mvn.cmd" spring-boot:run
```

Or double-click: `backend/run.bat`

Backend runs on: http://localhost:8080

### 4. Run Frontend

Open NEW Command Prompt:
```bash
cd frontend
npm install
npm run dev
```

Frontend runs on: http://localhost:3000

## Usage

1. Register a new account at http://localhost:3000/register
2. Login with your credentials
3. Create income/expense categories
4. Add income and expense transactions
5. View dashboard for financial overview
6. Download Excel reports

## API Endpoints

- `POST /api/v1.0/register` - Register user
- `POST /api/v1.0/login` - Login
- `GET /api/v1.0/profile` - Get profile
- `GET /api/v1.0/categories` - Get categories
- `POST /api/v1.0/categories` - Create category
- `GET /api/v1.0/incomes` - Get incomes
- `POST /api/v1.0/incomes` - Create income
- `GET /api/v1.0/incomes/excel` - Download Excel
- `GET /api/v1.0/expenses` - Get expenses
- `POST /api/v1.0/expenses` - Create expense
- `GET /api/v1.0/dashboard` - Get dashboard data

## Project Structure

```
expence_manager/
├── backend/
│   ├── src/main/java/com/moneymanager/
│   │   ├── entity/
│   │   ├── repository/
│   │   ├── service/
│   │   ├── controller/
│   │   ├── security/
│   │   └── config/
│   ├── pom.xml
│   ├── run.bat
│   └── Dockerfile
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── context/
    │   └── utils/
    └── package.json
```

## License

MIT License
