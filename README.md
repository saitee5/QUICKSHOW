# 🎬 QUICKSHOW — Movie Ticket Booking Platform

A full-stack, modern movie ticket booking web application built with **React 19**, **Vite**, **Tailwind CSS**, **Node.js**, **Express**, **MongoDB**, **Clerk Authentication**, and **Inngest**.

---

##  Features

### 👤 User Experience
- ** Movie Discovery & Showtimes:** Browse trending, featured, and upcoming movies with high-resolution posters and details.
- ** Trailer Previews:** Watch official movie trailers seamlessly with integrated video playback.
- ** Interactive Booking System:** Select preferred dates, showtimes, and pick seats via an interactive cinema seat layout.
- ** Secure Authentication:** Seamless user sign-in and sign-up powered by Clerk.
- **\ My Bookings:** Track active and past ticket reservations.
- ** Favorites & Watchlist:** Save favorite movies for quick access.
- ** Toast Notifications:** Real-time feedback and booking status updates.

### 🛠️ Admin Portal
- ** Analytics Dashboard:** Overview of total bookings, active shows, and revenue metrics.
- ** Show Management:** Add new movies, assign show timings, seat capacities, and pricing.
- ** Manage Shows & Bookings:** View and manage scheduled shows and customer reservations.

### ⚡ Backend & Event Workflows
- **⚡ Inngest Event-Driven System:** Background sync for Clerk webhooks (e.g., automatic user creation & updates in MongoDB).
- **🗄️ MongoDB with Mongoose:** Scalable database schemas for users, movies, shows, and bookings.
- **🔒 Secure API Endpoints:** Protected routes using Clerk Express middleware and CORS configuration.

---

## 🛠️ Tech Stack

### Frontend (`/client`)
- **Framework:** [React 19](https://react.dev/) + [Vite](https://vite.dev/)
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/)
- **Routing:** [React Router DOM v7](https://reactrouter.com/)
- **Authentication:** [@clerk/react](https://clerk.com/)
- **Icons:** [Lucide React](https://lucide.dev/)
- **Media Player:** [React Player](https://github.com/cookpete/react-player)
- **Notifications:** [React Hot Toast](https://react-hot-toast.com/)

### Backend (`/server`)
- **Runtime:** [Node.js](https://nodejs.org/)
- **Framework:** [Express 5](https://expressjs.com/)
- **Database:** [MongoDB](https://www.mongodb.com/) via [Mongoose](https://mongoosejs.com/)
- **Authentication & Middleware:** [@clerk/express](https://clerk.com/)
- **Background Jobs & Webhooks:** [Inngest](https://www.inngest.com/)
- **Media Management:** [Cloudinary](https://cloudinary.com/)
- **Development Tooling:** [Nodemon](https://nodemon.io/)

---

## 📁 Project Structure

```text
QUICKSHOW/
├── client/                     # Frontend application (React + Vite)
│   ├── public/                 # Static assets
│   ├── src/
│   │   ├── assets/             # Images, icons, and static data
│   │   ├── components/         # Reusable UI components (Navbar, Hero, MovieCard, etc.)
│   │   ├── pages/              # App pages (Home, Movies, MovieDetails, SeatLayout, etc.)
│   │   │   └── admin/          # Admin dashboard & management pages
│   │   ├── App.jsx             # Route definitions and layout wrapper
│   │   ├── main.jsx            # React root & ClerkProvider setup
│   │   └── index.css           # Global Tailwind CSS styles
│   ├── package.json
│   └── vite.config.js
│
├── server/                     # Backend API (Express + MongoDB)
│   ├── configs/                # DB connection & external service configurations
│   ├── inngest/                # Inngest client, event triggers, and functions
│   ├── models/                 # Mongoose schemas (User, Show, Booking, etc.)
│   ├── server.js               # Express application entry point
│   └── package.json
│
└── README.md                   # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
Make sure you have the following installed on your machine:
- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- A [MongoDB Atlas](https://www.mongodb.com/atlas) database or local MongoDB instance
- A [Clerk](https://clerk.com/) account for authentication keys
- An [Inngest](https://www.inngest.com/) account for event workflows

---

### 1. Clone the Repository
```bash
git clone https://github.com/saishreesaxena/QUICKSHOW.git
cd QUICKSHOW
```

---

### 2. Backend Setup (`server`)

1. **Navigate to the server directory:**
   ```bash
   cd server
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the `server` directory:
   ```env
   PORT=3000
   MONGODB_URI=your_mongodb_connection_string
   CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   CLERK_SECRET_KEY=your_clerk_secret_key
   INNGEST_EVENT_KEY=your_inngest_event_key
   INNGEST_SIGNING_KEY=your_inngest_signing_key
   ```

4. **Start the backend server:**
   ```bash
   npm run server
   ```
   *The server will run at `http://localhost:3000`.*

---

### 3. Frontend Setup (`client`)

1. **Navigate to the client directory (in a new terminal):**
   ```bash
   cd client
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure Environment Variables:**
   Create a `.env` file in the `client` directory:
   ```env
   VITE_CURRENCY=$
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   ```

4. **Start the development server:**
   ```bash
   npm run dev
   ```
   *The client app will run at `http://localhost:5173`.*

---

## 🛠️ Available Scripts

### In `/client`:
- `npm run dev` — Starts the Vite development server with HMR.
- `npm run build` — Compiles the client app for production.
- `npm run preview` — Previews the production build locally.
- `npm run lint` — Runs Oxlint to check code quality.

### In `/server`:
- `npm run server` — Runs the Express server in development mode with `nodemon`.
- `npm start` — Runs the Express server in production mode.

---

