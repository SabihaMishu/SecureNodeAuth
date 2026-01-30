# 🔐 SecureNodeAuth

A secure and scalable authentication REST API built with **Node.js, Express, MongoDB, and JWT**, featuring role-based access control and refresh token support.

---

## 🚀 Features

* ✅ User Registration & Login
* 🔐 JWT-based Authentication
* ♻️ Refresh Token System
* 🛡️ Protected Routes with Middleware
* 📦 MVC Architecture
* 🔑 Password Encryption (bcrypt)
* 📊 MongoDB with Mongoose
* ⚙️ Environment-based Configuration

---

## 🛠️ Tech Stack

| Technology | Usage                 |
| ---------- | --------------------- |
| Node.js    | Backend Runtime       |
| Express.js | Web Framework         |
| MongoDB    | Database              |
| Mongoose   | ODM                   |
| JWT        | Authentication        |
| Bcrypt     | Password Hashing      |
| Dotenv     | Environment Variables |

---

## 📁 Project Structure

```
SecureNodeAuth
│
├── server.js
├── package.json
├── .env
│
└── app
    ├── config
    ├── controllers
    ├── models
    ├── routes
    └── middlewares
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/SecureNodeAuth.git
cd SecureNodeAuth
```

### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Configure Environment Variables

Create a `.env` file in the root directory:

```env
PORT=8080
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
REFRESH_SECRET=your_refresh_secret
```

### 4️⃣ Run the Server

```bash
npm start
```

Server will run at:

```
http://localhost:8080
```

---

## 📌 API Endpoints

### 🔑 Authentication

| Method | Endpoint          | Description   |
| ------ | ----------------- | ------------- |
| POST   | /api/auth/signup  | Register User |
| POST   | /api/auth/signin  | Login User    |
| POST   | /api/auth/refresh | Refresh Token |
| POST   | /api/auth/logout  | Logout        |

### 🔒 Protected Routes

| Method | Endpoint             | Description      |
| ------ | -------------------- | ---------------- |
| GET    | /api/user/profile    | Get User Profile |
| GET    | /api/admin/dashboard | Admin Access     |

---

## 🔄 Authentication Flow

1️⃣ User registers using `/signup`

2️⃣ User logs in using `/signin`

3️⃣ Server returns:

* Access Token
* Refresh Token

4️⃣ Client uses Access Token to access protected routes

5️⃣ When token expires, Refresh Token is used to generate a new Access Token

---

## 🧩 Middleware Security

* `verifyToken` → Validates JWT
* `isAdmin` → Checks admin role
* `authJwt` → Protects routes

All protected routes pass through middleware before reaching controllers.

---

## 🏗️ Architecture (MVC Pattern)

```
Model      → Database Schema
View       → API Response (JSON)
Controller → Business Logic
```

This ensures:

* Clean Code
* Scalability
* Maintainability

---

## 📈 Future Improvements

* 🚀 OAuth (Google, Facebook Login)
* 📱 Frontend Integration (React)
* 📊 Logging System
* 🧪 Unit Testing
* ☁️ Cloud Deployment

---

## 📝 Example Request (Login)

```http
POST /api/auth/signin
Content-Type: application/json

{
  "email": "user@gmail.com",
  "password": "123456"
}
```

---

## 📄 Example Response

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIs...",
  "refreshToken": "eyJhbGciOiJIUzI1NiIs...",
  "user": {
    "id": "12345",
    "username": "demoUser"
  }
}
```

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License.

---

## 👩‍💻 Author

**Sabiha Jahan Mishu**
Backend Developer (Node.js)

GitHub: [[https://github.com/your-username](https://github.com/your-username)](https://github.com/SabihaMishu)

---

## ⭐ Support

If you found this project helpful, please give it a ⭐ on GitHub!

---

> "Learning by building real-world projects is the best way to become a great developer." 🚀
