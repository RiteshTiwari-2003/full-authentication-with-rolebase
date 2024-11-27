# Role-Based Authentication System

A full-stack authentication system with role-based access control (RBAC) built using Node.js, React, and MongoDB.

## Features

### Authentication
- User registration with role selection (Admin/User)
- Secure login with JWT token authentication
- Protected routes based on user roles
- Automatic token management
- Session persistence using localStorage

### User Management
- **Admin Features:**
  - View all users
  - Delete users
  - Modify user roles (promote to admin or demote to user)
  - Full access to user management dashboard

- **Regular User Features:**
  - View all users (read-only)
  - Access to personal dashboard
  - View personal profile information

### Security Features
- Password hashing using bcrypt
- JWT token-based authentication
- Protected API endpoints
- Role-based access control
- Input validation and sanitization
- Secure HTTP-only cookies
- CORS protection

## Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB (with Mongoose)
- JWT for authentication
- bcrypt for password hashing

### Frontend
- React.js
- Material-UI for styling
- Axios for API calls
- React Router for navigation
- Context API for state management

## Prerequisites

Before running this project, make sure you have:
1. Node.js (v14 or higher)
2. MongoDB installed or MongoDB Atlas account
3. npm or yarn package manager

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Authentication and authorization
```

2. Install backend dependencies:
```bash
cd app
npm install
```

3. Install frontend dependencies:
```bash
cd ../client
npm install
```

4. Create a .env file in the backend directory (app folder) with the following variables:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=3000
```

## Running the Application

1. Start the backend server:
```bash
cd app
npm start
```
The server will run on http://localhost:3000

2. Start the frontend development server:
```bash
cd client
npm start
```
The client will run on http://localhost:3001

## API Endpoints

### Authentication Routes
- POST `/api/auth/register` - Register a new user
- POST `/api/auth/login` - Login user
- GET `/api/auth/me` - Get current user profile
- GET `/api/auth/users` - Get all users (requires authentication)

### Admin Routes
- DELETE `/api/auth/users/:userId` - Delete a user (admin only)
- PUT `/api/auth/users/:userId/role` - Update user role (admin only)



## Security Best Practices Implemented

1. Password Hashing
   - Passwords are hashed using bcrypt before storing
   - Salt rounds configured for optimal security

2. JWT Implementation
   - Tokens expire after 24 hours
   - Secure token storage in HTTP-only cookies
   - Token verification on protected routes

3. Input Validation
   - Server-side validation for all inputs
   - Sanitization of user inputs
   - Strong password requirements

4. CORS Configuration
   - Configured to accept requests only from frontend origin
   - Credentials enabled for cross-origin requests

## Error Handling

The application implements comprehensive error handling:
- Custom error messages for various scenarios
- Proper HTTP status codes
- Validation error messages
- Database error handling
- Token verification errors

## Future Improvements

1. Implement refresh tokens
2. Add email verification
3. Add password reset functionality
4. Implement OAuth authentication
5. Add user activity logging
6. Enhance security with rate limiting
7. Add two-factor authentication
8. Implement more granular permissions

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


