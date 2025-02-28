# Authentication System (JWT)  
A secure authentication system using **Node.js, Express, MongoDB, and JWT** for user registration, login, and profile access.

## 🚀 Features  
- **User Registration** (Signup)  
- **User Login** (JWT Authentication)  
- **Protected Route** (Access User Profile)  
- **Password Hashing** (Bcrypt)  
- **JWT-based Authentication** (Secure access)  

## 📁 Folder Structure  
```
backend/
│── config/
│   └── db.js          # MongoDB connection  
│── controllers/
│   └── authController.js  # Handles auth logic  
│── middleware/
│   └── authMiddleware.js  # Protects routes  
│── models/
│   └── User.js        # User schema  
│── routes/
│   └── authRoutes.js  # Auth API routes  
│── server.js         # Main entry point  
│── .env              # Environment variables  
│── package.json      # Dependencies  
```

## 🛠️ Installation  
### 1️⃣ Clone the repository  
```sh
git clone https://github.com/your-username/auth-jwt.git
cd auth-jwt
```
### 2️⃣ Install dependencies  
```sh
npm install
```
### 3️⃣ Configure environment variables  
Create a `.env` file in the root folder and add:  
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000
```
### 4️⃣ Start the server  
```sh
npm start
```

## 📌 API Endpoints  
### ✅ **User Registration**  
**POST** `/api/auth/register`  
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "123456"
}
```
### ✅ **User Login**  
**POST** `/api/auth/login`  
```json
{
  "email": "john@example.com",
  "password": "123456"
}
```
**Response:**  
```json
{
  "token": "your_jwt_token",
  "user": {
    "_id": "65d8abc12345d67890abcdef",
    "name": "John Doe",
    "email": "john@example.com"
  }
}
```
### ✅ **Access User Profile (Protected)**  
**GET** `/api/auth/profile`  
- **Headers** → `Authorization: Bearer your_jwt_token`  
**Response:**  
```json
{
  "user": {
    "_id": "65d8abc12345d67890abcdef",
    "name": "John Doe",
    "email": "john@example.com"
  }
}
```
## 🔥 Technologies Used  
- **Node.js & Express** (Backend API)  
- **MongoDB & Mongoose** (Database)  
- **JWT (JSON Web Token)** (Authentication)  
- **Bcrypt.js** (Password Hashing)  

## ✅ License  
This project is **open-source** under the MIT License.
