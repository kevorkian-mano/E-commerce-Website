# LUCINE Application

A complete MERN stack e-commerce platform with a modern UI, secure authentication, shopping cart, order management, and admin dashboard — built using Layered (3-Tier) Architecture and SOLID principles.

## Project Overview
LUCINE is a full-stack e-commerce solution featuring both imperative and declarative programming styles.
It provides full user and admin functionality, including product management, order processing, and analytics.

### Features

- User Authentication (Register, Login, Logout)
- Product Browsing & Advanced Search
- Shopping Cart Management
- Order Placement & History
- Email Notifications
- Admin Dashboard
- Product Management (CRUD)
- Sales Analytics & Reports
- Responsive Design
- Secure & Scalable

## Project Structure

```
Testing Project/
backend/
├── server.js                 # Main server file
├── package.json              # Dependencies
├── .env.example             # Environment variables template
├── API_DOCUMENTATION.md     # API endpoint documentation
├── IMPLEMENTATION_SUMMARY.md # This file
└── src/
    ├── config/
    │   └── db.js            # Database connection
    ├── models/
    │   ├── User.js          # User model with password hashing
    │   ├── Product.js       # Product model with indexes
    │   ├── Order.js         # Order model
    │   └── Cart.js          # Cart model
    ├── repositories/
    │   ├── userRepository.js
    │   ├── productRepository.js
    │   ├── cartRepository.js
    │   └── orderRepository.js
    ├── services/
    │   ├── authService.js
    │   ├── productService.js
    │   ├── cartService.js
    │   └── orderService.js
    ├── controllers/
    │   ├── authController.js
    │   ├── productController.js
    │   ├── cartController.js
    │   └── orderController.js
    ├── routes/
    │   ├── userRoutes.js
    │   ├── productRoutes.js
    │   ├── cartRoutes.js
    │   └── orderRoutes.js
    ├── middlewares/
    │   ├── auth.js          # Authentication & authorization
    │   └── errorHandler.js  # Error handling
    └── utils/
        ├── jwt.js           # JWT token utilities
        ├── emailService.js  # Email sending service
        ├── asyncHandler.js  # Async error wrapper
        └── validators.js    # Validation utilities

frontend/
├── index.html
├── package.json
├── vite.config.js
└── tailwind.config.js
└── src/
    ├── components/
    │   └── layout/
    │       ├── Navbar.jsx          # Navigation bar with cart count
    │       ├── Footer.jsx           # Footer component
    │       ├── ProtectedRoute.jsx   # Route protection
    │       └── AdminRoute.jsx       # Admin route protection
    │
    ├── context/
    │   ├── AuthContext.jsx          # Authentication state
    │   └── CartContext.jsx          # Shopping cart state
    │
    ├── pages/
    │   ├── Home.jsx                 # Landing page
    │   ├── Products.jsx             # Product listing
    │   ├── ProductDetails.jsx      # Product details
    │   ├── Cart.jsx                # Shopping cart
    │   ├── Checkout.jsx            # Checkout process
    │   ├── Orders.jsx              # Order history
    │   ├── OrderDetails.jsx        # Order details
    │   ├── Login.jsx               # Login page
    │   ├── Register.jsx            # Registration page
    │   └── admin/
    │       ├── AdminDashboard.jsx  # Admin dashboard
    │       ├── AdminProducts.jsx   # Product management
    │       ├── AdminOrders.jsx     # Order management
    │       └── AdminAnalytics.jsx  # Sales analytics
    │
    └── utils/
        └── api.js                   # API client with interceptors

---

## Tech Stack

### Backend
- **Node.js** with **Express**
- **MongoDB** with **Mongoose**
- **JWT** for authentication
- **bcrypt** for password hashing
- **Nodemailer** for emails
- **Layered Architecture** (3-tier)

### Frontend
- **React 18** with **Vite**
- **React Router** for navigation
- **Tailwind CSS** for styling
- **Axios** for API calls
- **Context API** for state management
- **React Icons** & **React Toastify**

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud)
- npm 

### Backend Setup

1. Navigate to backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create `.env` file:
   ```env
   PORT=5000
   NODE_ENV=development
   MONGO_URI=mongodb://localhost:27017/ecommerce
   JWT_SECRET=your_secret_key_here
   JWT_EXPIRE=7d
   SMTP_HOST=smtp.gmail.com
   SMTP_PORT=587
   SMTP_USER=your_email@gmail.com
   SMTP_PASS=your_app_password
   ```

4. Start the server:
   ```bash
   npm run dev
   ```

   Backend will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. (Optional) Create `.env` file:
   ```env
   VITE_API_URL=http://localhost:5000/api
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

   Frontend will run on `http://localhost:3000`



## Functional Requirements

- **FR1:** User registration, login, and logout
- **FR2:** Product browsing and search (by category, name, price)
- **FR3:** Shopping cart management (add/remove items)
- **FR4:** Order placement and order history
- **FR5:** Email notifications for orders
- **FR6:** Admin product management and sales analytics

## Non-Functional Requirements

- **NFR1:** Performance (indexed queries, optimized responses)
- **NFR2:** Reliability (error handling, transactions)
- **NFR3:** Security (bcrypt, JWT, RBAC)
- **NFR4:** Maintainability (SOLID principles, modular code)
- **NFR5:** Concurrency (atomic operations, transactions)
- **NFR6:** Usability (responsive design, accessible UI)

## Architecture

The application follows **Layered (3-Tier) Architecture**:

1. **Presentation Layer** (Frontend)
   - React components and pages
   - User interface and interactions

2. **Business Logic Layer** (Backend Services)
   - Service classes with business rules
   - Transaction management
   - Email notifications

3. **Data Access Layer** (Repositories & Database)
   - Repository pattern
   - MongoDB with Mongoose
   - Data models and schemas

## Security Features

- Password hashing with bcrypt
- JWT-based authentication
- Role-based access control (Admin/Customer)
- Input validation
- Protected routes
- Secure API endpoints

## Responsive Design

The frontend is fully responsive and works seamlessly on:
- Desktop computers
- Tablets
- Mobile devices

## Testing the Application

    later on ...

## Code Quality

- SOLID principles applied
- Separation of concerns
- Modular architecture
- Clean code practices
- Error handling throughout
- Input validation
- No syntax errors

## Deployment

### Backend Deployment

    later on ...
### Frontend Deployment

    later on ...
    
## 📄 License

This project is created for educational purposes.

---

**Status:** ✅ **Beta Version Complete - Ready for Testing**
