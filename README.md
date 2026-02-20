# E-Commerce-Website


## 🛍️ What is ShopNest?

> **ShopNest** is a fully functional, production-ready e-commerce website built completely from scratch as a major web development project. It works just like **Amazon** or **Flipkart** — customers can register, browse products, add to cart, place orders, and track them in real time. A separate **Admin Panel** lets the store owner manage everything from products to orders to customers.

---

## ✨ Features

<div align="center">

| 🧑‍💼 User Features | 🔐 Admin Features | ⚙️ Backend Features |
|:---|:---|:---|
| ✅ Register & Login | ✅ Admin Login (Separate) | ✅ REST API (12 Endpoints) |
| ✅ Browse Product Catalog | ✅ Add / Delete Products | ✅ JWT Authentication |
| ✅ Search & Filter Products | ✅ Live Product Preview | ✅ bcrypt Password Hashing |
| ✅ Product Detail Page | ✅ View All Orders | ✅ Role-Based Access Control |
| ✅ Add to Cart | ✅ Update Order Status | ✅ MongoDB with Mongoose |
| ✅ Checkout & Place Order | ✅ View All Customers | ✅ dotenv Secret Management |
| ✅ My Orders History | ✅ Search Customers | ✅ nodemon Auto-Restart |
| ✅ Notifications Page | ✅ Revenue & Stats Dashboard | ✅ CORS Enabled |

</div>

---

## 🚀 Tech Stack

<div align="center">

| Layer | Technology | Purpose |
|:---:|:---:|:---|
| 🎨 **Frontend** | HTML5 | Structure of all 15 pages |
| 🎨 **Frontend** | CSS3 | Dark theme, responsive layout, animations |
| 🎨 **Frontend** | Vanilla JavaScript | API calls, DOM manipulation, localStorage |
| ⚙️ **Backend** | Node.js | Server-side JavaScript runtime |
| ⚙️ **Backend** | Express.js | REST API routing and middleware |
| 🗄️ **Database** | MongoDB | NoSQL document storage |
| 🗄️ **Database** | Mongoose | Schema modeling and validation |
| 🔐 **Security** | JWT | Stateless authentication tokens |
| 🔐 **Security** | bcryptjs | One-way password hashing |
| 🛠️ **Dev Tools** | dotenv | Secure environment variables |
| 🛠️ **Dev Tools** | nodemon | Auto server restart on changes |

</div>

---

## 📁 Project Structure

```
📦 ecommerce/
├── 📂 backend/
│   ├── 📂 middleware/
│   │   └── 📄 auth.js           # JWT verification middleware
│   ├── 📂 models/
│   │   ├── 📄 User.js            # User schema (name, email, password, role)
│   │   ├── 📄 Product.js         # Product schema (name, price, category, stock)
│   │   └── 📄 Order.js           # Order schema (items, address, status)
│   ├── 📂 routes/
│   │   ├── 📄 auth.js            # Register & Login endpoints
│   │   ├── 📄 products.js        # Product CRUD endpoints
│   │   ├── 📄 orders.js          # Order placement & history
│   │   └── 📄 admin.js           # Admin-only endpoints
│   ├── 📄 server.js              # Main entry point
│   ├── 📄 seed.js                # Database seeder (admin + sample products)
│   ├── 📄 package.json           # NPM dependencies
│   └── 📄 .env                   # Environment variables (secret)
│
└── 📂 frontend/
    ├── 📂 css/
    │   └── 📄 style.css          # Shared stylesheet for all pages
    ├── 📂 user/
    │   ├── 📄 register.html      # Create new account
    │   ├── 📄 login.html         # Sign in to account
    │   ├── 📄 dashboard.html     # Browse all products
    │   ├── 📄 product.html       # Single product detail
    │   ├── 📄 cart.html          # Shopping cart
    │   ├── 📄 payment.html       # Checkout & place order
    │   ├── 📄 orders.html        # My order history
    │   └── 📄 notification.html  # Order notifications
    └── 📂 admin/
        ├── 📄 login.html         # Admin sign in
        ├── 📄 dashboard.html     # Stats & recent orders
        ├── 📄 add-product.html   # Add / delete products
        ├── 📄 view-orders.html   # Manage all orders
        └── 📄 view-customers.html # View all customers
```

---

## 🔌 API Reference

<div align="center">

| Method | Endpoint | Access | Description |
|:---:|:---|:---:|:---|
| `POST` | `/api/auth/register` | 🌐 Public | Register a new user account |
| `POST` | `/api/auth/login` | 🌐 Public | User login — returns JWT token |
| `POST` | `/api/auth/admin-login` | 🌐 Public | Admin login — returns JWT token |
| `GET` | `/api/products` | 🔒 User | Get all products |
| `GET` | `/api/products/:id` | 🔒 User | Get single product by ID |
| `POST` | `/api/products` | 👑 Admin | Add new product |
| `DELETE` | `/api/products/:id` | 👑 Admin | Delete product |
| `POST` | `/api/orders` | 🔒 User | Place a new order |
| `GET` | `/api/orders/my` | 🔒 User | Get my orders |
| `GET` | `/api/admin/orders` | 👑 Admin | Get all orders |
| `PATCH` | `/api/admin/orders/:id/status` | 👑 Admin | Update order status |
| `GET` | `/api/admin/customers` | 👑 Admin | Get all customers |

</div>

---

## ⚡ Getting Started

### Prerequisites

Make sure the following are installed on your machine:

- ![Node.js](https://img.shields.io/badge/Node.js-v18+-339933?style=flat-square&logo=nodedotjs)
- ![MongoDB](https://img.shields.io/badge/MongoDB-v6+-47A248?style=flat-square&logo=mongodb)
- ![VSCode](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode)

---

### 🛠️ Installation

**Step 1 — Clone the Repository**
```bash
git clone https://github.com/yourusername/shopnest.git
cd shopnest
```

**Step 2 — Install Backend Dependencies**
```bash
cd backend
npm install
```

**Step 3 — Set Up Environment Variables**

Create a `.env` file inside the `backend/` folder:
```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/shopnest
JWT_SECRET=your_super_secret_key_here
```

**Step 4 — Seed the Database** *(Run Once Only)*
```bash
node seed.js
```
> This creates the admin account and adds 6 sample products.

**Step 5 — Start the Server**
```bash
npm run dev
```

You should see:
```
✅ MongoDB Connected
🚀 Server running on http://localhost:5000
```

**Step 6 — Launch the Frontend**

Open `frontend/user/register.html` in VS Code → Right-click → **Open with Live Server**

---

## 🔑 Default Credentials

<div align="center">

| Role | Email | Password |
|:---:|:---:|:---:|
| 👑 **Admin** | `admin@shopnest.com` | `admin123` |
| 🧑‍💼 **User** | Register via `/user/register.html` | Your choice |

</div>

---

## 🧪 Testing the Full Flow

```
1. 📝  Register a new customer account
2. 🔐  Login → Dashboard opens with 6 products
3. 🛍️  Click any product → View detail page
4. 🛒  Add to Cart → Navigate to Cart
5. 💳  Proceed to Checkout → Fill address → Place Order
6. 📦  Open Admin Panel → View Orders → Update status to "Shipped"
7. 🔔  Check Notifications → Status updated in real time
```

---

## 🗄️ Database Schema

<div align="center">

### 👤 Users Collection
| Field | Type | Description |
|:---|:---:|:---|
| `name` | String | Full name of the user |
| `email` | String | Unique login email |
| `phone` | String | Phone number |
| `password` | String | bcrypt hashed — never plain text |
| `role` | String | `"user"` or `"admin"` |
| `createdAt` | Date | Auto-generated timestamp |

### 📦 Products Collection
| Field | Type | Description |
|:---|:---:|:---|
| `name` | String | Product name |
| `description` | String | Detailed description |
| `price` | Number | Price in Indian Rupees ₹ |
| `category` | String | Electronics / Clothing / Books / Sports / Home |
| `image` | String | Public image URL |
| `stock` | Number | Available units |

### 🛒 Orders Collection
| Field | Type | Description |
|:---|:---:|:---|
| `user` | ObjectId | Reference to User |
| `items` | Array | Products with name, price, quantity |
| `deliveryAddress` | Object | Full shipping address |
| `paymentMethod` | String | Cash on Delivery |
| `totalAmount` | Number | Total cost of the order |
| `status` | String | Pending / Processing / Shipped / Delivered / Cancelled |

</div>

---

## 📊 Project Stats

<div align="center">

| 📄 Total Pages | ⚙️ Backend Files | 🗄️ DB Models | 🔌 API Endpoints |
|:---:|:---:|:---:|:---:|
| **15** | **12** | **3** | **12** |

</div>

---

## 🛑 Stopping the Server

```bash
# In the terminal where the server is running:
Ctrl + C
```

---

## 🙌 Skills Demonstrated

- ✅ Full-Stack Web Development (Frontend + Backend + Database)
- ✅ RESTful API Design with Express.js
- ✅ JWT Authentication & Role-Based Access Control
- ✅ MongoDB Schema Design with Mongoose
- ✅ Password Security with bcryptjs
- ✅ Responsive UI with CSS Variables & Dark Theme
- ✅ Browser localStorage for Cart State Management
- ✅ Async JavaScript with fetch() API

---

**Made with ❤️ as a Major Web Development Project — February 2026**

