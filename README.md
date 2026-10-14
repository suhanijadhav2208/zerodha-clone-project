# Zerodha Clone Project

A full-stack stock-trading dashboard inspired by Zerodha. This
educational project combines a landing/login frontend, an Express
backend, and a trading dashboard.

> **Disclaimer:** This is an educational/demo project, not an official
> Zerodha product. It is not connected to real brokerage services and
> must not be used for real trading or financial transactions. Parts of
> the project are based on the Apna College Zerodha clone project and
> have been customized.

## Project Structure

``` text
zerodha-clone-project/
├── backend/     # Node.js and Express API
├── dashboard/   # Trading dashboard
├── frontend/    # Landing pages, login and signup
└── README.md
```

## Features

-   User signup and login with password hashing
-   JWT-based authentication using HTTP-only cookies
-   Stock watchlist and trading dashboard
-   Buy and sell order flows
-   Orders, holdings and positions views
-   Funds view with add/withdraw flows
-   Backend API built with Express
-   MongoDB data storage through Mongoose

Some features depend on the backend and database being configured
correctly.

## Technology Stack

-   **Frontend:** React, JavaScript, HTML and CSS
-   **Dashboard:** React
-   **Backend:** Node.js and Express.js
-   **Database:** MongoDB and Mongoose
-   **Authentication:** bcrypt and JSON Web Tokens (JWT)

Check each folder's `package.json` for the exact dependencies and
scripts.

## Prerequisites

-   Node.js and npm
-   A MongoDB database/connection, such as MongoDB Atlas
-   Git

## Configuration

Create a `.env` file inside `backend/` locally. **Do not commit this
file.** Configure the variables expected by the backend:

``` env
PORT=3002
MONGO_URL=your_mongodb_connection_string
JWT_SECRET=replace_with_a_long_random_secret
```

Use your own database connection string and a strong, unique JWT secret.
Never put real credentials in source code, commits, screenshots, or
public repositories.

The local development ports used in this setup are:

-   Frontend: `3000`
-   Dashboard: `3001`
-   Backend: `3002`

The frontend and dashboard may also need API URL environment variables.
Check their source code and `package.json` scripts for the expected
names and values.

## Installation and Running Locally

Open three separate terminals from the project root.

### 1. Backend

``` bash
cd backend
npm install
npm start
```

If `npm start` is not defined in `backend/package.json`, use the script
provided there (for example, `npm run dev` or `node index.js`).

### 2. Frontend

``` bash
cd frontend
npm install
npm start
```

Use the script defined in `frontend/package.json` if it differs.

### 3. Dashboard

``` bash
cd dashboard
npm install
npm start
```

Use the script defined in `dashboard/package.json` if it differs.

Open the local frontend and dashboard addresses in your browser. Make
sure the backend is running and its CORS configuration allows the local
frontend/dashboard origins.

## Security Notes

-   Keep `.env` files out of Git and ensure `.gitignore` excludes
    environment files and `node_modules`.
-   Never publish MongoDB credentials, JWT secrets, access tokens, or
    real user data.
-   If a secret was ever committed, removing it from the latest version
    is not enough: rotate/revoke it and review Git history.
-   Use HTTPS and secure cookie settings for production.
    Local-development cookie settings may need changes before
    deployment.
-   This project is not represented as a production-ready trading
    platform. Security, authorization, validation, testing, and
    deployment hardening would be required.

## Attribution

This project is inspired by the Zerodha trading interface and builds on
the Apna College Zerodha clone project. Retain applicable attribution
and comply with the original project's license and terms.

## License

No license is specified in this README. Unless a license is added,
standard copyright rules apply to original contributions. Review the
original source project's license before redistributing its code.
