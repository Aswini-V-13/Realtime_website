# 🛍️ Kartl – E-Commerce Web Application

A modern, responsive e-commerce web application developed as the final project of the **15-Day Full Stack Development Training Program at Doodleblue Innovations**.

Kartl provides a complete shopping experience with product browsing, user authentication, favourites, cart management, checkout, and order tracking. It combines a React frontend with a Node.js and Express backend, using MongoDB for database management.

## ✨ Features

### 1. Product Browsing
- Browse products across different categories.
- Search products by name and description.
- Filter products based on categories.
- View product details, prices, ratings, and discounts.

### 2. User Authentication
- User registration and login.
- Secure password hashing using bcrypt.
- JWT-based authentication.
- Forgot password functionality.
- OTP-based password reset through the user's registered email address.
- OTP expiration and single-use validation.

### 3. Shopping Cart
- Add products to the cart.
- Increase or decrease product quantities.
- Remove products from the cart.
- Automatic price and total calculation.
- Cart synchronization for logged-in users.

### 4. Favourites
- Add products to favourites.
- Remove products from favourites.
- View saved favourite products.

### 5. Checkout & Orders
- Checkout form with customer details.
- Delivery address and contact information.
- Payment method selection.
- Automatic subtotal, delivery charge, and total calculation.
- Order placement and success notification.
- Order history with order details and status.

### 6. Email Integration
- OTP delivery through email using Nodemailer.
- Password reset verification through a six-digit OTP.
- OTP expires after 10 minutes.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| React.js | Frontend development |
| JavaScript | Application functionality |
| HTML5 | Web page structure |
| CSS3 | Styling and responsive design |
| Vite | Frontend development and build tool |
| Node.js | Backend runtime environment |
| Express.js | REST API development |
| MongoDB | Database management |
| JWT | User authentication |
| bcrypt.js | Password hashing |
| Nodemailer | Email integration |
| DummyJSON API | Product data source |

## 🏗️ Project Architecture

The application follows a client-server architecture.

**Frontend (React + Vite)**
- Displays products and user interfaces.
- Handles user interactions and shopping cart operations.
- Communicates with the backend through REST APIs.

**Backend (Node.js + Express.js)**
- Handles authentication and authorization.
- Manages product and cart APIs.
- Generates and verifies password reset OTPs.
- Integrates email services using Nodemailer.

**Database (MongoDB)**
- Stores registered user accounts.
- Stores product information.
- Maintains password reset OTP records.
- Stores carts for authenticated users.

## 📂 Project Structure

```text
Kartl/
│
├── server/
│   └── index.js
│
├── src/
│   ├── App.jsx
│   ├── main.jsx
│   └── styles.css
│
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
├── .env.example
├── .gitignore
└── README.md
```

## ⚙️ Installation & Setup

### Prerequisites

Make sure you have the following installed:

- Node.js
- MongoDB (local installation or MongoDB Atlas)
- Visual Studio Code
- Git

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Step 2: Navigate to the Project Folder

```bash
cd Kartl
```

### Step 3: Install Dependencies

```bash
npm install
```

### Step 4: Configure Environment Variables

Create a `.env` file in the root directory and add:

```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_random_secret_key_at_least_32_characters
PORT=3001

SMTP_HOST=smtp.gmail.com
SMTP_PORT=465
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_google_app_password
SMTP_FROM=your_email@gmail.com
```

Replace the values with your own MongoDB connection string, JWT secret, and email configuration.

**Note:** Never upload your `.env` file or email app passwords to GitHub.

### Step 5: Start the Backend Server

Open a terminal and execute:

```bash
npm run server
```

The backend API will run at:

```text
http://localhost:3001
```

### Step 6: Start the Frontend

Open another terminal and execute:

```bash
npm run dev
```

Open the local URL displayed in the terminal to access the application.

## 🔗 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/health` | Check server status |
| GET | `/api/categories` | Retrieve product categories |
| GET | `/api/products` | Retrieve and search products |
| POST | `/api/auth/signup` | Register a new user |
| POST | `/api/auth/login` | Authenticate a user |
| POST | `/api/auth/forgot-password` | Generate and send OTP |
| POST | `/api/auth/reset-password` | Verify OTP and reset password |
| GET | `/api/cart` | Retrieve authenticated user's cart |
| PUT | `/api/cart` | Update authenticated user's cart |

## 🔐 Security Implementation

- Passwords are hashed using bcrypt.js before storing them.
- JWT tokens are used to authenticate protected API requests.
- OTPs are stored as SHA-256 hashes instead of plain text.
- Password reset codes expire after 10 minutes.
- Used OTPs cannot be reused.
- Protected cart APIs require valid JWT authentication.

## 📌 Important Project Notes

- Product information is fetched from DummyJSON and synchronized with MongoDB.
- Product prices are displayed in Indian Rupees using a demo currency conversion rate.
- Authenticated users' carts are stored in MongoDB.
- Guest carts, favourites, and order history are currently stored in browser local storage.
- Checkout and payment selection are demonstration functionalities; no live payment gateway is integrated.
- Order confirmation is currently displayed within the application.

## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

- Developing responsive user interfaces using React.js.
- Building REST APIs using Node.js and Express.js.
- Connecting frontend applications with backend services.
- Performing CRUD operations using MongoDB.
- Implementing authentication and authorization.
- Integrating email services using Nodemailer.
- Managing application state and browser local storage.
- Understanding the complete workflow of a full stack web application.

## 🙏 Acknowledgement

This project was developed as the final task of the **15-Day Full Stack Development Training Program conducted by Doodleblue Innovations**.

I sincerely thank our trainers **Dhanush N and Vijayaraghavan K** for their guidance, support, and valuable knowledge throughout the training.

Special thanks to the **Department of MCA** for providing this wonderful opportunity to enhance my technical skills and gain practical development experience.

---

**Developed with ❤️ as part of my Full Stack Development learning journey.**
