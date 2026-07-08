# WanderLust

WanderLust is a full-stack web application designed for listing and reviewing vacation rentals, similar to Airbnb. It allows users to explore various travel listings, register accounts, post their own properties with images, and write reviews for different accommodations.

The project is built using the MVC (Model-View-Controller) design pattern with Node.js, Express, MongoDB, and EJS.

## Live Demo
Check out the live version of the project here: [WanderLust on Vercel](https://wanderlust-kappa-nine.vercel.app/listings)

## Features
- **User Authentication:** Secure sign-up, login, and logout using Passport.js.
- **CRUD Operations:** Create, edit, and delete property listings. Only the listing owner has permission to edit or delete it.
- **Image Upload:** Upload and store listing photos securely on Cloudinary.
- **Review System:** Add star ratings (1 to 5) and comments on listings. Users can delete their own reviews.
- **Form Validation:** Client-side and server-side validation using Bootstrap and Joi.

## Tech Stack
- **Backend:** Node.js, Express.js
- **Database:** MongoDB, Mongoose ODM
- **Templating:** EJS (Embedded JavaScript) with `ejs-mate` for layouts
- **Authentication:** Passport.js (passport-local)
- **Image Hosting:** Cloudinary (via `multer` and `multer-storage-cloudinary`)
- **Validation:** Joi

---

## Setup and Installation

To run this project locally, follow these steps:

### Prerequisites
- Node.js installed
- MongoDB installed locally or a MongoDB Atlas account
- A Cloudinary account for hosting listing images

### 1. Clone the repository
```bash
git clone https://github.com/Shresth-11/WanderLust.git
cd WanderLust
```

### 2. Install dependencies
```bash
npm install
```

### 3. Configure Environment Variables
Create a `.env` file in the root directory and add the following keys with your own credentials:
```env
ATLASDB_URL="your-mongodb-connection-string"
SECRET="your-session-secret"
CLOUD_NAME="your-cloudinary-cloud-name"
CLOUD_API_KEY="your-cloudinary-api-key"
CLOUD_API_SECRET="your-cloudinary-api-secret"
```

### 4. Seed the Database
To populate the database with some sample listing data, run the initialization script:
```bash
node init/index.js
```

### 5. Run the Application
Start the Express server:
```bash
node app.js
```
The server will start listening on port `8080`. Open `http://localhost:8080` in your web browser.

---

## Directory Structure
- `/controllers` - Contains the business logic for listings, reviews, and users.
- `/models` - Mongoose schemas for Listing, Review, and User.
- `/routes` - Express routers defining app endpoints.
- `/views` - EJS templates for rendering pages.
- `/public` - Static assets including stylesheets and scripts.
- `/init` - Sample data and seeding script.

## License
This project is open-source and available under the [MIT License](LICENSE).
