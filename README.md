# Q-Master | Queue Management System

A professional full-stack queue management system built with the MERN stack (MongoDB, Express, React, Node.js) and modern UI principles. This project demonstrates database integration, RESTful API design, and real-time frontend updates.

## Features

- **Customer Registration**: Quick token generation with service selection.
- **Token System**: Unique token numbers generated based on service codes.
- **Live Status Display**: Public dashboard showing tokens "Now Serving" and "Waiting".
- **Admin Management**: Full CRUD operations for queue entries.
- **MVC Architecture**: Clean separation of concerns in the backend.
- **Real-time Sync**: Automatic polling mechanism for high-availability.
- **Responsive Design**: Mobile-first UI styled with Tailwind CSS.

## Tech Stack

- **Frontend**: React.js, Tailwind CSS, Axios, React Router, Lucide Icons, Framer Motion.
- **Backend**: Node.js, Express.js, Mongoose.
- **Database**: MongoDB (via Mongoose ODM).

## Installation

1. **Clone the repository**
2. **Setup environment variables**
   - Create a `.env` file based on `.env.example`.
   - Provide your `DATABASE_URL` (MongoDB string).
3. **Install Dependencies**
   ```bash
   npm install
   ```
4. **Development**
   ```bash
   npm run dev
   ```
5. **Build for Production**
   ```bash
   npm run build
   ```

## Folder Structure

```text
/
├── server.ts            # Production server & Vite middleware
├── src/
│   ├── backend/         # Node.js Backend (MVC)
│   │   ├── config/      # DB connection
│   │   ├── models/      # Mongoose schemas
│   │   ├── controllers/ # Logic handlers
│   │   └── routes/      # API endpoints
│   ├── components/      # UI Components
│   ├── pages/           # Application Views
│   ├── services/        # API Integration
│   └── App.tsx          # Main entry & Routing
```

## Database Schema

### Queue Collection
- `tokenNumber` (String)
- `customerName` (String)
- `phoneNumber` (String)
- `serviceId` (ObjectId)
- `status` (Enum: pending, serving, completed)
- `priority` (Enum: normal, express, vip)
- `counterNumber` (Number)

### Service Collection
- `name` (String)
- `code` (String)
- `active` (Boolean)

---
Built as part of the DecodeLabs Industrial Training Kit.
