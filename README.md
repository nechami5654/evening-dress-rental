#  Evening Dress Rental – Fullstack Web App

A fullstack web platform for managing and mediating evening dress rentals. Built with **vanilla JavaScript** on the client side, **Node.js** and **Express.js** on the backend, and **MongoDB** as the database.

Developed entirely through **independent self-learning**, utilizing online resources to master fullstack technologies.

---

##  Project Overview

This platform supports three user roles:

| Role            | Permissions                                                                 |
|-----------------|----------------------------------------------------------------------------|
| Guest           | Browse dresses and use advanced filters by color, price, size, rating, and location |
| Registered User | Rate dresses (1–5 stars), leave verified comments                           |
| Business Owner  | Add, update, delete, and manage their own dresses                           |

---

##  Key Features

- Advanced dress filtering:
  -  Color  
  -  Price Range  
  -  Size Combinations  
  -  Rating  
  -  Geographic Location
- Detailed dress view with image, price, city, sizes, rating & comments
- Secure **JWT-based authentication** & role-based permissions
- Star-based rating system (1–5)
- Business owner dashboard for dress management
- Verified user comments and feedback
- User-friendly, responsive design

---

##  Technologies Used

###  Frontend

- HTML5, CSS3  
- JavaScript (DOM manipulation, Fetch API)

###  Backend

- Node.js with Express.js  
- MongoDB with Mongoose  
- JSON Web Tokens (JWT) – Auth & Authorization  
- dotenv – Environment management  
- Multer – File uploads (e.g., dress images)  
- Custom Middlewares – Error handling, security  

---

##  Project Structure

```
evening-dress-rental/
├── client/
│   ├── css/            # CSS stylesheets
│   ├── html/           # HTML pages
│   └── js/             # Client-side JS
│
├── server/
│   ├── Controller/     # Logic for users, dresses, etc.
│   ├── DB/             # MongoDB connection
│   ├── MiddleWare/     # Authentication & error handling
│   ├── Model/          # Mongoose schemas (User, Dress, Rating)
│   ├── Routes/         # API routing
│   ├── Services/       # Helper services (email, file mgmt)
│   ├── uploads/        # Uploaded dress images
│   ├── express.js      # Server setup
│   └── .env            # Environment config (not committed)
├── .gitignore
├── README.md
```

---

##  Authentication & Authorization

- Users register/login to receive a JWT token  
- Token must be sent via `Authorization: Bearer <token>` header  
- Role-based access ensures protected routes for business users  
- Middleware validation for secure endpoints  

---

##  Getting Started

###  1. Clone the repository

```bash
git clone https://github.com/nechami5654/evening-dress-rental.git
cd evening-dress-rental
```

###  2. Install backend dependencies

```bash
cd server
npm install
```

###  3. Configure environment variables

Configure environment variables
Copy the example environment file and fill in your own credentials:

```bash
cp .env.example .env
```

Edit `.env` and set your MongoDB URI, JWT secret, and PORT. Example `.env.example` contents:

```bash
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/dbname
PORT=4000
JWT_SECRET=your_jwt_secret_here
```

###  4. Run the server

```bash
npm run dev
```

###  5. Open the frontend

Open `client/html/index.html` in your browser  
Or serve using the Live Server extension

---

##  Roles & Permissions

| Role            | Capabilities                                                            |
|-----------------|-------------------------------------------------------------------------|
| Guest           | Browse dresses, use filters                                             |
| Registered User | Rate and comment on dresses                                             |
| Business Owner  | Add/update/delete own dresses                                           |

---

##  Feature Highlights

-  Filter dresses dynamically
-  Upload dress images via Multer
-  Role-based route protection
-  Clean code with separation of concerns
-  Auth middleware for secure access
-  Star rating and comment system with user validation

---

##  License

This project is open-source and available under the **MIT License**.

---

##  About the Developer

Developed as a **self-learning** final project  
 **Contact**: nechami5654@gmail.com  
 Final grade: 100  
Built with passion, real-world architecture, and modern development practices 

---

> _“Learning by doing is the best way to master development.”_
