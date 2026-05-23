# 🏡 Wanderlust 

[![Node.js](https://img.shields.io/badge/Node.js-v22.12-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-v4.21-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![EJS](https://img.shields.io/badge/EJS-Views-B4CA65?logo=html5&logoColor=white)](https://ejs.co/)
[![Cloudinary](https://img.shields.io/badge/Cloudinary-Media_Upload-3448C5?logo=cloudinary&logoColor=white)](https://cloudinary.com/)
[![Vercel](https://img.shields.io/badge/Vercel-Deployment-000000?logo=vercel&logoColor=white)](https://vercel.com/)

**Wanderlust** is a premium, full-featured **Airbnb Clone** built using the MVC architecture with **Node.js**, **Express.js**, **EJS**, and **MongoDB**. It delivers a fully responsive, secure web experience that allows users to seamlessly explore global vacation rental listings, submit detailed reviews, post their own listings with cloud-based image hosting, and manage content under robust authentication guards.

---

## 🔗 Live Demo

Experience the live application hosted on Vercel:  
👉 **[[Visit Wanderlust Website](https://airbnb-lilac-seven.vercel.app/listings)]**

---

## ✨ Features

- 🔐 **Robust Authentication:** Secure registration, login, logout, and session persistence powered by **Passport.js** and Local Strategy.
- 🏡 **Listing Management (CRUD):** 
  - Dynamic listing creation with fields for Title, Description, Price, Location, and Country.
  - Interactive property editing and deletion with strict owner authorization guards.
- ☁️ **Cloud Image Storage:** Secure image file uploading, resizing, and hosting integrated with **Cloudinary Storage API** via `multer`.
- 💬 **Review & Rating System:**
  - Standardized feedback forms allowing authenticated users to rate listings on a 1-5 scale and leave reviews.
  - Quick review removal for authenticated authors.
- 🎨 **Responsive UI/UX:** Styled using fluid CSS frameworks and EJS-mate layouts to ensure beautiful display across smartphones, tablets, and desktops.
- 🛡️ **Session & Security Guards:** Session storage utilizing **Mongo Store** for high performance, custom route-protecting middleware, validation using **Joi** schemas, and sanitization.

---

## 🛠️ Tech Stack & Dependencies

- **Frontend Templating Engine:** [EJS (Embedded JavaScript Templates)](https://ejs.co/) & [EJS-Mate](https://github.com/JacksonTian/ejs-mate) for layouts
- **Runtime Environment:** [Node.js](https://nodejs.org/)
- **Server Framework:** [Express.js](https://expressjs.com/)
- **Database (BaaS):** [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) & [Mongoose ORM](https://mongoosejs.com/)
- **Authentication Engine:** [Passport.js](https://www.passportjs.org/) & [passport-local-mongoose](https://github.com/screamitch/passport-local-mongoose)
- **Session & Flash Storage:** [express-session](https://www.npmjs.com/package/express-session), [connect-mongo](https://www.npmjs.com/package/connect-mongo), and [connect-flash](https://www.npmjs.com/package/connect-flash)
- **Media Upload Manager:** [Multer](https://github.com/expressjs/multer) & [multer-storage-cloudinary](https://github.com/cpseager/multer-storage-cloudinary)
- **Data Validation:** [Joi Schema Validation](https://joi.dev/)

---

## 📂 Project Architecture

The application is structured following the **MVC (Model-View-Controller)** pattern:

```bash
Airbnb/
├── controllers/          # Business logic handlers for core routes
│   ├── listings.js       # CRUD logic for rental properties
│   ├── reviews.js        # Logic for creating and deleting ratings/reviews
│   └── users.js          # Authentication handlers (signup, login, logout)
├── init/                 # Seed scripts for initial database configuration
│   ├── data.js           # Static listing dataset
│   └── index.js          # Execution script to clean and seed MongoDB collections
├── models/               # Mongoose schemas for MongoDB
│   ├── listing.js        # Property listing model
│   ├── review.js         # User review and rating model
│   └── user.js           # Passport-local integrated user model
├── public/               # Static styles, client-side scripts, and icon assets
├── routes/               # Modular Express routing definitions
│   ├── listing.js        # Routes for listings operations
│   ├── review.js         # Routes for reviews operations
│   └── user.js           # Routes for auth operations
├── utils/                # Custom operational utilities
│   ├── ExpressError.js   # Custom express error handling class
│   └── wrapAsync.js      # Global async route wrapper to capture uncaught rejections
├── views/                # EJS rendering layouts and templates
│   ├── includes/         # Shared sub-views (Header, Footer, Flash alerts)
│   ├── layouts/          # EJS-mate boilerplate wrappers
│   ├── listings/         # EJS views for CRUD (Index, Show, Edit, New)
│   └── users/            # EJS views for auth forms (Login, Signup)
├── app.js                # Core Express application and pipeline setup
├── cloudConfig.js        # Multer storage integration for Cloudinary SDK
├── middleware.js         # Custom route guards and validations
├── schema.js             # Joi schema definitions for server-side validation
└── vercel.json           # Vercel deployment and rewrite configuration
```

---

## ⚙️ Environment Setup

To run Wanderlust locally, you will need to set up a MongoDB cluster and a Cloudinary account.

1. Create a `.env` file in the root directory:
   ```bash
   touch .env
   ```

2. Add your environment variables:
   ```env
   ATLASDB_URL="YOUR_MONGODB_ATLAS_CONNECTION_STRING"
   SECRET="YOUR_EXPRESS_SESSION_ENCRYPTION_SECRET"
   CLOUD_NAME="YOUR_CLOUDINARY_CLOUD_NAME"
   CLOUD_API_KEY="YOUR_CLOUDINARY_API_KEY"
   CLOUD_API_SECRET="YOUR_CLOUDINARY_API_SECRET"
   ```

---

## 🚀 Getting Started

Follow these steps to launch the application locally:

### 1. Clone the Repository
```bash
git clone https://github.com/Shresth-11/Airbnb.git
cd Airbnb
```

### 2. Install Dependencies
Ensure Node.js (v18+) is installed.
```bash
npm install
```

### 3. Seed the Database
Initialize your MongoDB database with sample vacation rental data:
```bash
node init/index.js
```

### 4. Start the Application Server
Run the local Express server:
```bash
node app.js
```
Open your browser and navigate to `http://localhost:8080` to explore Wanderlust!

---

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

*Built with passion and dedication by [Shresth-11](https://github.com/Shresth-11)* 🚀


