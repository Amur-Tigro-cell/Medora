# Medora

Medora is a full-stack healthcare platform built with the MERN stack. It
connects patients with medicines, doctors, appointments, blood donors, and
emergency blood requests in one application.

## Features

### Patients

- Create an account, sign in, reset a forgotten password, and manage a profile
- Browse medicines, search products, add items to a cart, and place orders
- Select a shipping address and pay with PayPal or AamarPay
- Browse doctors and book appointments
- Search and filter blood donors
- Register as a donor or submit an emergency blood request
- Review medicines and chat with an administrator

### Administrators

- Manage users, medicines, doctors, donors, orders, appointments, and blood
  requests
- Create, update, and remove catalog and healthcare records
- Review and approve orders, appointments, and blood requests

## Technology

- **Frontend:** React, React Router, Redux Toolkit, Material UI, Bootstrap
- **Backend:** Node.js, Express, MongoDB, Mongoose
- **Authentication:** JWT with HTTP-only cookies
- **Payments:** PayPal and AamarPay
- **Email:** Nodemailer

## Project structure

```text
.
├── backend/
│   ├── config/          # Database configuration
│   ├── controller/      # Request handlers
│   ├── middleware/      # Authentication and error handling
│   ├── models/          # Mongoose models
│   ├── routes/          # API routes
│   └── server.js        # Express entry point
├── frontend/
│   └── src/
│       ├── Screens/     # Page-level React components
│       ├── components/  # Shared UI components
│       └── slices/      # Redux state and API slices
└── uploads/             # Uploaded images for local development
```

## Requirements

- Node.js 18 or newer
- npm
- MongoDB database

## Getting started

1. Clone the repository and enter the project directory:

   ```bash
   git clone https://github.com/Amur-Tigro-cell/Medora.git
   cd Medora
   ```

2. Install backend dependencies:

   ```bash
   npm install
   ```

3. Install frontend dependencies:

   ```bash
   npm install --prefix frontend
   ```

4. Create a `.env` file in the project root:

   ```env
   NODE_ENV=development
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_long_random_secret
   PAYPAL_CLIENT_ID=your_paypal_client_id
   ```

   Keep `.env` private. It is intentionally excluded from version control.

5. Start the development servers:

   ```bash
   npm run dev
   ```

   The API runs on `http://localhost:5000` and the React application runs on
   `http://localhost:3000`.

## Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Run the backend and frontend together |
| `npm run server` | Run the backend with Nodemon |
| `npm run client` | Run the React frontend |
| `npm start` | Start the backend |
| `npm run build` | Install dependencies and build the frontend |
| `npm run data:import` | Import seed data |
| `npm run data:destroy` | Remove seed data |

## API areas

The backend exposes REST endpoints under:

```text
/api/users
/api/meds
/api/doctors
/api/bloods
/api/appointments
/api/orders
/api/requests
/api/upload
```

PayPal configuration is available at `/api/config/paypal`.

## Production

Build the application with:

```bash
npm run build
```

When `NODE_ENV=production`, the Express server serves the compiled React
application and exposes uploaded files from the configured upload directory.
Set all production environment variables through the hosting provider rather
than committing them to the repository.

## Screenshots

Product screenshots are available in [`ss/`](./ss/).

## License

This project is released under the MIT License.
