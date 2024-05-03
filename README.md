Inkspired is a Blog Application built using MERN stack.

Backend Architecture:
![Untitled-2024-03-10-0151](https://github.com/sunnykumar26/inkspired_blog_app/assets/113859373/32f745d0-ced6-4841-acf4-ee9cb5ec0691)


![Screenshot_20240504_023520](https://github.com/sunnykumar26/inkspired_blog_app/assets/113859373/6daa5818-6413-4f49-b532-2b4740559020)

# Inkspired - a blog application 

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This is the backend component of [Your Application Name], a web application built using the MERN (MongoDB, Express, React, Node.js) stack. This repository contains the server-side code responsible for handling requests, managing data, and implementing business logic.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication (register, login, logout)
- User management (CRUD operations on user data)
- Post management (CRUD operations on posts)
- Comment management (CRUD operations on comments)
- JWT-based authentication for protected routes
- Middleware for handling file uploads
- Integration with MongoDB for data storage

## Prerequisites

Before running the backend server, ensure you have the following prerequisites installed on your machine:

- Node.js and npm (Node Package Manager)
- MongoDB (Make sure MongoDB server is running)

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd backend
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Create a `.env` file in the root directory and add the following environment variables:

   ```plaintext
   PORT=5000
   MONGO_URL=your-mongodb-connection-string
   SECRET=your-jwt-secret
   ```

   Replace `your-mongodb-connection-string` with your MongoDB connection string and `your-jwt-secret` with a secret key for JWT token generation.

## Usage

To start the backend server, run the following command:

```bash
npm start
```

The server will start listening on the port specified in the `.env` file (default is 5000).

## API Endpoints

The backend server exposes the following API endpoints:

- **Auth Routes**
  - POST /api/auth/register - Register a new user
  - POST /api/auth/login - Login user
  - GET /api/auth/logout - Logout user
  - GET /api/auth/refetch - Re-fetch user data (protected route)

- **User Routes**
  - GET /api/users - Get all users
  - GET /api/users/:userId - Get user by ID
  - PUT /api/users/:userId - Update user
  - DELETE /api/users/:userId - Delete user

- **Post Routes**
  - GET /api/posts - Get all posts
  - GET /api/posts/:postId - Get post by ID
  - POST /api/posts - Create new post (protected route)
  - PUT /api/posts/:postId - Update post (protected route)
  - DELETE /api/posts/:postId - Delete post (protected route)

- **Comment Routes**
  - GET /api/comments - Get all comments
  - GET /api/comments/:commentId - Get comment by ID
  - POST /api/comments - Create new comment (protected route)
  - PUT /api/comments/:commentId - Update comment (protected route)
  - DELETE /api/comments/:commentId - Delete comment (protected route)

For detailed documentation on each endpoint and how to use them, refer to the source code and comments in the respective route files.

## Contributing

Contributions are welcome! If you find any bugs or have suggestions for improvement, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
