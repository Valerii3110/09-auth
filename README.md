🔐 Authentication Module — Express + JWT

A clean, modular, and production-ready authentication system built with Node.js, Express, JWT, and validation schemas.
Designed following the clarity and structural aesthetics of TailwindUI and Next.js documentation.

🚀 Overview

This project implements a complete authentication workflow, including:

User registration

Login & logout

Token refresh

Password reset via email

Request validation

Modular routing and controllers

The structure is clean, scalable, and suitable as a base for any full-stack application.

🛠 Tech Stack
Technology	Purpose
Node.js / Express	Server & routing
JWT (jsonwebtoken)	Access & refresh tokens
bcrypt	Secure password hashing
Celebrate / Joi	Request validation
Nodemailer	Password reset email delivery
dotenv	Environment variables
MongoDB / Mongoose (if used)	User storage
📂 Project Structure
09-auth/
├─ controllers/
│  └─ authController.js        # Business logic
├─ routes/
│  └─ authRoutes.js            # Auth endpoints
├─ validations/
│  └─ authValidation.js        # Joi schemas
├─ middlewares/
│  └─ authMiddleware.js        # Token verification
├─ utils/
│  └─ sendEmail.js             # Email service
├─ models/
│  └─ userModel.js             # User schema (if using MongoDB)
├─ app.js                      # App initialization
├─ server.js                   # Server entry point
└─ README.md

📦 Installation

Clone the repository:

git clone https://github.com/Valerii3110/09-auth.git


Install dependencies:

npm install


Create .env file:

PORT=3000
JWT_SECRET=your_secret_key
JWT_REFRESH_SECRET=your_refresh_secret
MONGODB_URI=mongodb_connection
EMAIL_USER=your_email
EMAIL_PASS=your_email_password
CLIENT_URL=http://localhost:3000


Run in development mode:

npm run dev


Start production build:

npm start

🔑 API Endpoints
Auth Routes
Method	Endpoint	Description
POST	/api/auth/register	Register new user
POST	/api/auth/login	Login and get tokens
POST	/api/auth/logout	Logout user
POST	/api/auth/refresh	Refresh access token
POST	/api/auth/request-reset	Send password reset email
POST	/api/auth/reset-password	Reset user password

All routes include validation schemas and clean controller separation.

✔ Features

JWT-based access & refresh tokens

Strong password hashing

Validation using Celebrate/Joi

Secure email-based password reset

Modular architecture

Clean, extendable controllers

Production-ready code structure

🎨 Design Philosophy (TailwindUI / Next.js)

The project follows:

clean and minimal block structure

consistent naming and folder hierarchy

separation of concerns (controllers, routes, services)

lightweight dependencies

scalable architecture

🚧 Roadmap

Add rate limiting

Add user roles (admin/user)

Add magic-link authentication

Add 2FA

Add login history & device tracking

Integrate with frontend (Next.js / React)

👤 Author

Valerii3110
GitHub: https://github.com/Valerii3110

📄 License

Distributed under the MIT License.

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
