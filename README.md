# Authentication_Google_OAuth_with_.env
Added Google OAuth and introduced .env file for secure environment variable management


# 🔐 Passport Authentication with Express, PostgreSQL & Google OAuth

A Node.js authentication app using Express.js, PostgreSQL, and Passport.js that supports both **Local Authentication (email & password)** and **Google OAuth 2.0**. Environment variables are securely managed using a `.env` file.

---

## 📦 Features

- ✅ Local authentication using email and hashed password
- ✅ Google OAuth 2.0 authentication
- ✅ PostgreSQL database integration for storing users
- ✅ Session management with `express-session`
- ✅ Password encryption with `bcrypt`
- ✅ Environment variables stored securely in `.env`
- ✅ Protected routes (e.g. `/secrets`) accessible only when logged in

---

## 🗃️ Environment Configuration (`.env`)

The `.env` file is used to store sensitive configuration data and environment variables. This helps keep credentials and secret keys out of your source code.

Example `.env` file:


<img width="473" alt="4 2_ env" src="https://github.com/user-attachments/assets/cb40cffd-a527-4532-9eb9-00794780f52a" />


## 🔑 Google OAuth 2.0 Authentication
Users can log in using their Google account via Passport's google-oauth2 strategy.

Flow:
User navigates to `/auth/google`

Google asks for permission to access profile and email

On success, user is redirected to `/auth/google/secrets`

If user doesn't exist in the database, they are added

User is logged in and redirected to the protected `/secrets` page
