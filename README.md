# Foodyman Web Suite

A comprehensive, state-of-the-art restaurant management and food delivery ecosystem. This repository contains the complete web codebase including the backend API services, administrator dashboard, customer-facing web application, and QR-code menu web app.

---

## 📂 Project Structure

The project is organized into modular applications under the web suite directory:

```text
foodyman_web/
├── admin_backend/     # Laravel API Backend (Core business logic & DB management)
├── admin_frontend/    # React-based Admin & Seller Dashboard (Management panel)
├── web_frontend/      # Next.js Customer Web Application (Ordering & browsing website)
└── qrcode_menu/       # Vite-based QR-code Interactive Menu (In-restaurant digital ordering)
```

---

## 🛠️ Technology Stack

Each module leverages a modern and high-performance stack:

*   **Core Backend**: Laravel (PHP 8.x), MySQL, Redis.
*   **Customer Web Application**: Next.js (React 18), Redux Toolkit, MUI (Material UI), Swiper, Sass.
*   **Admin Dashboard**: React (v17), Ant Design, Redux Toolkit, ApexCharts, Sass.
*   **QR Menu**: React (v18), Vite, Emotion, MUI, Framer Motion.

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed on your system:
*   [Node.js](https://nodejs.org/) (v18 or higher recommended)
*   [PHP](https://www.php.net/) (v8.1 or higher)
*   [Composer](https://getcomposer.org/)
*   [MySQL Server](https://www.mysql.com/)

---

### 1. ⚙️ Backend API Setup (`admin_backend`)

The backend is built with Laravel and acts as the central API service for all frontends.

1.  Navigate to the backend directory:
    ```bash
    cd admin_backend
    ```
2.  Install composer dependencies:
    ```bash
    composer install
    ```
3.  Create your local environment file:
    ```bash
    copy .env.example .env
    ```
4.  Configure your database credentials in the newly created `.env` file:
    ```env
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=your_database_user
    DB_PASSWORD=your_database_password
    ```
5.  Generate the application key:
    ```bash
    php artisan key:generate
    ```
6.  Run the database migrations and seeders:
    ```bash
    php artisan migrate --seed
    ```
7.  Start the local development server:
    ```bash
    php artisan serve
    ```

---

### 2. 🖥️ Customer Web Application Setup (`web_frontend`)

A Next.js SSR (Server-Side Rendered) web app for the consumer storefront.

1.  Navigate to the web frontend directory:
    ```bash
    cd ../web_frontend
    ```
2.  Install NPM dependencies:
    ```bash
    npm install
    ```
3.  Configure API endpoint and credentials in `.env`:
    ```env
    NEXT_PUBLIC_BASE_URL=http://localhost:8000
    ```
4.  Start the Next.js development server:
    ```bash
    npm run dev
    ```
    *The app will run locally at `http://localhost:8000`.*

---

### 3. 📊 Admin & Seller Dashboard Setup (`admin_frontend`)

A React dashboard for administrators, store managers, and sellers.

1.  Navigate to the admin frontend directory:
    ```bash
    cd ../admin_frontend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Configure the global application configuration file at `src/configs/app-global.js` or configure the `.env` file to point to your backend API.
4.  Start the development server:
    ```bash
    npm start
    ```
    *The dashboard will start locally on `http://localhost:3000` (or another available port).*

---

### 4. 📱 QR-Code Menu Web App (`qrcode_menu`)

An interactive digital menu for in-shop customer tables.

1.  Navigate to the QR Menu directory:
    ```bash
    cd ../qrcode_menu
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the development server using Vite:
    ```bash
    npm run dev
    ```
    *The app will run locally at `http://localhost:5173`.*

---

## 🌟 Features Summary

*   **Multi-tenant Dashboard**: Complete management panels for Super Admins, Sellers/Store Managers, and Delivery Staff.
*   **Customer Storefront**: Highly responsive, SEO-optimized ordering system with geolocation, multi-language support, and real-time tracking.
*   **Smart QR Menus**: Allows restaurant visitors to scan table QR codes, browse live menus, and place orders directly.
*   **Comprehensive API**: Secure RESTful endpoints built with Laravel, featuring robust authentication, reporting, and payment gateway integrations.

---

## 📄 License

This project is proprietary software. All rights reserved.
