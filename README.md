# InzuTrust

InzuTrust is a property-rental platform with a React web application and an
Express API. It includes property listings, tenant and landlord workflows,
agent and admin dashboards, lease agreements, payments, maintenance requests,
disputes, messaging, notifications, and trust scores.

## Project layout

- `frontend/` - React 19 and Vite application
- `backend/` - Express API using Sequelize and MySQL

## Requirements

- Node.js and npm
- A MySQL database
- Credentials for the external services used by the backend (as applicable)

## Setup

1. Install backend dependencies:

   ```powershell
   cd backend
   npm install
   ```

2. Copy `backend/.env.example` to `backend/.env` and set the database
   credentials, a strong `JWT_SECRET`, and any service credentials you use.
   The backend also supports Cloudinary, email, and Daily API credentials.
   Do not commit `.env` files or real credentials.

3. Start the API from `backend/`:

   ```powershell
   npm run dev
   ```

   The API defaults to port `3306`; set `PORT` in `backend/.env` to choose
   another port.

4. In a second terminal, install frontend dependencies and start Vite:

   ```powershell
   cd frontend
   npm install
   npm run dev
   ```

   The frontend uses the deployed API by default. To use a local API, copy
   `frontend/.env.example` to `frontend/.env` and set `VITE_API_URL` to the
   API URL, for example `http://localhost:5000/api` when the backend uses
   `PORT=5000`.

## Useful scripts

Run these from the relevant `backend/` or `frontend/` directory:

- Backend: `npm run dev` or `npm start`
- Frontend: `npm run dev`, `npm run build`, `npm run lint`, or `npm run preview`
