=======
# Fleet Management System

A comprehensive web application for managing vehicle fleets, drivers, trips, maintenance, and fuel logs. Built with Node.js, Express, MySQL, and EJS.

## 🚀 Workflow Overview

### 1. Authentication & Security
- **Signup**: Users register with Name, Email, Password, and Role (Manager, Dispatcher, Safety Officer, Analyst).
- **Email Verification**: A 6-digit OTP is sent via Gmail (SMTP) for account activation.
- **Login**: Secured session-based authentication with `bcryptjs` password hashing.
- **Rate Limiting**: Protection against brute-force attacks on password resets.
- **Audit Logging**: All critical actions (Login, Logout, Data mutations) are tracked in the database.

### 2. Fleet & Personnel Management
- **Vehicles**: Track license plates, model year, fuel types, and status (Active, Maintenance, Out of Service).
- **Drivers**: Manage driver profiles, contact info, and licensing.

### 3. Operations
- **Trips**: Create and track trips, assigning specific vehicles and drivers. Includes cargo weight and route details.
- **Fuel Logs**: Monitor fuel consumption and costs per vehicle.
- **Maintenance**: Track service records, costs, and incident reports to ensure fleet health.

### 4. Insights
- **Dashboard**: Real-time overview of active trips, vehicle status, and recent activity.
- **Analytics**: Detailed reports on driver performance, fuel expenses, and maintenance trends.

---

## 🛠️ Tech Stack
- **Backend**: Node.js, Express.js
- **Frontend**: EJS (Embedded JavaScript Templates), CSS
- **Database**: MySQL (using `mysql2` with connection pooling)
- **Utilities**: `nodemailer` (Email), `multer` (File Uploads), `express-session` (Auth), `dotenv` (Config)

---

## ⚙️ Setup & Installation

### Prerequisites
- Node.js (v16+)
- MySQL Server

### 1. Clone & Install Dependencies
```bash
npm install
```

### 2. Database Configuration
1. Create a MySQL database (e.g., `fleet_db`).
2. Import the schema found in `database/schema.sql`.
3. Configure your credentials in the `.env` file.

### 3. Environment Variables (.env)
Create a `.env` file in the root directory:
```env
PORT=3000
APP_URL=http://localhost:3000

DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=fleet_db

SESSION_SECRET=your_secret_key

EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
EMAIL_FROM="Fleet System <your_email@gmail.com>"
```

### 4. Running the App
- **Development**: `npm run dev` (starts with nodemon)
- **Production**: `npm start`

---

## 📂 Project Structure
- `app.js`: Main application entry point.
- `/routes`: Definition of all API endpoints and page routes.
- `/controllers`: Business logic handling for each module.
- `/models`: Database query abstractions.
- `/views`: UI templates.
- `/config`: Configuration for DB, Mailer, and File Uploads.
- `/public`: Static assets (CSS, Images, JS).
- `/database`: SQL schema and migrations.
>>>>>>> d602823dcee3bbac4d8d5e7682af2ae7e30ec5c1
