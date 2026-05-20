# SkyTakeout Project

## Project Overview

SkyTakeout is an online food delivery ordering system tailored for catering businesses such as restaurants and food chains. The project aims to provide an efficient and convenient takeaway solution for both merchants and consumers, covering the complete business workflow from dish management and order processing to delivery tracking.

The system adopts a frontend-backend separated architecture:

- Frontend: Vue.js
- Backend: Spring Boot
- Database: MySQL

---

# Technology Stack

## Backend Technologies

- Framework: Spring Boot 2.7.x (integrated with Spring MVC and MyBatis)
- Security: Spring Security + JWT (authentication and authorization)
- Database: MySQL 8.0.x
- Cache: Redis 6.2+
- API Documentation: Swagger / Knife4j

### Additional Tools

- Apache HttpClient
- Apache POI
- Alibaba Cloud OSS
- WebSocket
- Spring Task

---

## Frontend Technologies

### Admin Panel
- Vue.js
- ElementUI

### User Application
- WeChat Mini Program

### State Management
- Pinia

### HTTP Client
- Axios

### Build Tool
- Vite

---

## Deployment & Operations

- Nginx
- Docker
- Kubernetes
- ELK Stack

---

# Functional Modules

The SkyTakeout system mainly consists of:

1. Admin Management System
2. Customer WeChat Mini Program
3. Courier/Rider Mini Program

---

# Admin Management Features

## Employee Management
- Query employees
- Add employees
- Edit employee information
- Enable/Disable employees
- Permission management

## Category Management
- Dish category management
- Set meal category management

## Dish Management
- Dish CRUD
- Flavor management
- Availability management

## Set Meal Management
- Combo meal management
- Pricing management
- Availability management

## Order Management
- Order query
- Cancel orders
- Delivery management
- Complete orders
- Export reports

## Data Statistics
- Revenue reports
- User growth analysis
- Order trend analysis

## Real-Time Notifications
WebSocket-based order reminder system.

---

# Customer Features (WeChat Mini Program)

## WeChat Login
Quick login through WeChat authorization.

## Dish Browsing
- Browse dishes by category
- View specifications
- Favorite dishes
- Add to cart

## Shopping Cart
- Add items
- Update quantities
- Remove items
- Clear cart

## Order Payment
- WeChat Pay integration
- Checkout
- Refund support

## Personal Center
- Address management
- Order history
- Account settings

## Order Reminder
Users can remind merchants to process delayed orders.

---

# Courier Features

## Order Delivery
- Accept orders
- Deliver orders
- Route planning

## Smart Dispatching
Automatically dispatches orders to nearby riders.

---

# System Architecture

## User Layer
- Admin Web Application
- Customer Mini Program
- Rider Mini Program

## Gateway Layer
- Nginx reverse proxy
- Load balancing
- Static resource hosting

## Application Layer
- Controller Layer
- Service Layer
- Mapper Layer

## Data Layer
- MySQL
- Redis

---

# Database Design

Database name:

```sql
sky_take_out
```

Core tables:

| Table Name | Description |
|---|---|
| employee | Employee information |
| category | Category information |
| dish | Dish information |
| dish_flavor | Dish flavor information |
| setmeal | Set meal information |
| setmeal_dish | Set meal-dish relationship |
| user | User information |
| address_book | Address information |
| shopping_cart | Shopping cart |
| orders | Order information |
| order_detail | Order details |

---

# Environment Requirements

- JDK 11+
- MySQL 8.0+
- Redis 6.0+
- Node.js 16+
- Maven 3.6+

---

# Database Configuration

Modify `application-dev.yml`:

```yaml
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://your-host:port/sky_take_out?serverTimezone=Asia/Shanghai&useUnicode=true&characterEncoding=utf-8&zeroDateTimeBehavior=convertToNull&useSSL=false&allowPublicKeyRetrieval=true
    username: your_username
    password: your_password
```

---

# Redis Configuration

```yaml
spring:
  redis:
    host: localhost
    port: 6379
    password:
    database: 0
```

---

# Project Startup

## Backend Startup

```bash
cd sky-server
mvn spring-boot:run
```

API Documentation:

```text
http://localhost:8080/doc.html
```

---

## Frontend Startup

Run:

```bash
nginx.exe
```

---

# Project Highlights

- Frontend-backend separated architecture
- WeChat Mini Program integration
- Real-time WebSocket communication
- Smart order dispatching
- Redis caching optimization
- JWT authentication
- Scheduled task processing

---

# Important Notes

1. Redis must be running before backend startup.
2. Start backend services before frontend services.
3. Disable Swagger in production.
4. Secure database and Redis credentials.
5. Some features rely on third-party APIs.

---

# Contribution Guide

```bash
git checkout -b feature/xxx
git commit -m "Add xxx feature"
git push origin feature/xxx
```

Then create a Pull Request.

---

# Contact

- Maintainer: yucheng
- Email: zyucheng2004@gmail.com
- Issue Feedback: Submit issues through GitHub Issues.