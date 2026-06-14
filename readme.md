# 🌍 WanderLust

A full-stack Airbnb-inspired travel listing web application where users can explore destinations, create their own property listings, upload images, and share reviews.

🚀 **Live Demo:**  
https://wanderlust-r3lk.onrender.com

---

# 📌 Features

## 🔐 Authentication & Authorization

- User registration and login system
- Secure authentication using Passport.js
- Session management using MongoStore
- Only authenticated users can create listings
- Only listing owners can edit/delete their listings

## 🏠 Listing Management

- Create new travel listings
- View all available listings
- View individual listing details
- Edit existing listings
- Delete listings

## 🖼️ Image Upload

- Upload listing images using Cloudinary
- Image storage and optimization through Cloudinary
- Multer used for handling file uploads

## ⭐ Reviews System

- Users can add reviews
- Users can delete their reviews
- Review author association using MongoDB references

## ⚡ Other Features

- Flash messages for user feedback
- Server-side validation using Joi
- MVC architecture
- Responsive UI using Bootstrap

---

# 🛠️ Tech Stack

## Frontend

- HTML
- CSS
- Bootstrap 5
- EJS Template Engine

## Backend

- Node.js
- Express.js

## Database

- MongoDB Atlas
- Mongoose ODM

## Authentication

- Passport.js
- Passport Local Strategy
- Passport Local Mongoose

## File Upload

- Multer
- Cloudinary

## Deployment

- Render

---

# 📁 Project Structure

```
WanderLust
│
├── controllers
│   ├── listing.js
│   ├── reviews.js
│   └── users.js
│
├── init
│   ├── data.js
│   └── index.js
│
├── models
│   ├── listing.js
│   ├── review.js
│   └── user.js
│
├── public
│   ├── css
│   │   ├── rating.css
│   │   └── style.css
│   │
│   └── js
│       └── script.js
│
├── routes
│   ├── listing.js
│   ├── review.js
│   └── user.js
│
├── utils
│   ├── ExpressError.js
│   └── wrapAsync.js
│
├── views
│   ├── includes
│   │   ├── flash.ejs
│   │   ├── footer.ejs
│   │   └── navbar.ejs
│   │
│   ├── layouts
│   │   └── boilerplate.ejs
│   │
│   ├── listings
│   │   ├── edit.ejs
│   │   ├── index.ejs
│   │   ├── new.ejs
│   │   └── show.ejs
│   │
│   ├── users
│   │   ├── login.ejs
│   │   └── signup.ejs
│   │
│   └── error.ejs
│
├── app.js
├── cloudConfig.js
├── middleware.js
├── package.json
├── package-lock.json
└── schema.js

```

---

# 📌 Important Files

| File              | Description                                 |
| ----------------- | ------------------------------------------- |
| app.js            | Main application entry point                |
| cloudConfig.js    | Cloudinary configuration                    |
| middleware.js     | Authentication and authorization middleware |
| schema.js         | Joi validation schemas                      |
| models/listing.js | Listing database schema                     |
| models/review.js  | Review database schema                      |
| models/user.js    | User authentication model                   |
| controllers/      | Contains business logic                     |
| routes/           | Handles application routes                  |
| views/            | EJS templates                               |

---

# 🔗 Application Routes

## Listings

| Method | Route           | Description          |
| ------ | --------------- | -------------------- |
| GET    | `/listings`     | Display all listings |
| GET    | `/listings/new` | Create listing form  |
| POST   | `/listings`     | Create new listing   |
| GET    | `/listings/:id` | Show listing details |
| PUT    | `/listings/:id` | Update listing       |
| DELETE | `/listings/:id` | Delete listing       |

## Reviews

| Method | Route                             | Description   |
| ------ | --------------------------------- | ------------- |
| POST   | `/listings/:id/reviews`           | Add review    |
| DELETE | `/listings/:id/reviews/:reviewId` | Delete review |

## Authentication

| Method | Route     | Description       |
| ------ | --------- | ----------------- |
| GET    | `/signup` | Signup page       |
| POST   | `/signup` | Register user     |
| GET    | `/login`  | Login page        |
| POST   | `/login`  | Authenticate user |
| GET    | `/logout` | Logout user       |

---

# ⚙️ Installation & Setup

## 1. Clone Repository

```bash
git clone https://github.com/mYuvraj4118/WanderLust.git
```

## 2. Navigate to Project

```bash
cd WanderLust
```

## 3. Install Dependencies

```bash
npm install
```

## 4. Create Environment Variables

Create a `.env` file in the root directory.

Add:

```env
ATLASDB_URL=your_mongodb_atlas_url

CLOUD_NAME=your_cloudinary_name

CLOUD_API_KEY=your_cloudinary_api_key

CLOUD_API_SECRET=your_cloudinary_secret

SECRET=your_session_secret
```

## 5. Start Application

Development mode:

```bash
nodemon app.js
```

Application will run at:

```
http://localhost:8080
```

---

# ☁️ Deployment

The project is deployed using:

- Render for hosting
- MongoDB Atlas for database
- Cloudinary for image storage

Live URL:

https://wanderlust-r3lk.onrender.com

---

# 🧱 Architecture

The project follows MVC architecture:

```
User Request
      |
      ↓
Routes
      |
      ↓
Controllers
      |
      ↓
Models
      |
      ↓
MongoDB Database

```

---

# 🔒 Security Implementations

- Password hashing using Passport Local Mongoose
- Authentication middleware
- Authorization checks
- Joi input validation
- Environment variables for sensitive credentials

---

# 👨‍💻 Author

**Yuvraj**

GitHub:
https://github.com/mYuvraj4118

Linkedin:
http://www.linkedin.com/in/yuvraj-mathe

---

# 📜 License

This project is licensed under the ISC License.
