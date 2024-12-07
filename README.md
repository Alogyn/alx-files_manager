# 0x04. Files Manager 📂

![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow?style=flat-square&logo=javascript) ![Backend](https://img.shields.io/badge/Backend-NodeJS-green?style=flat-square&logo=node.js) ![NoSQL](https://img.shields.io/badge/Database-MongoDB-red?style=flat-square&logo=mongodb)

## 📖 Project Overview
The **Files Manager** project is a backend application combining concepts from authentication, API design, NoSQL databases, background processing, and file management. The application enables users to:
- Authenticate and manage access tokens.
- Upload and manage files with public/private access.
- View file statistics.
- Generate thumbnails for images.

The project leverages key technologies like **Node.js**, **ExpressJS**, **MongoDB**, **Redis**, and **Kue** for background job processing.

## 🎯 Learning Objectives
- 🔑 **Authentication**: Implement user authentication via tokens.
- 🛠️ **API Design**: Develop RESTful endpoints with ExpressJS.
- 🗄️ **MongoDB**: Store and retrieve data using NoSQL databases.
- ⚡ **Redis**: Manage temporary data efficiently.
- 🖼️ **Background Workers**: Process tasks asynchronously with Kue.
- 🌐 **Pagination**: Implement efficient data pagination.

## 🛠️ Technologies Used
- **Node.js** (v12.x.x)
- **ExpressJS**
- **MongoDB**
- **Redis**
- **Kue** for background jobs
- **Babel** for ES6+ support
- **Mocha** for testing

## 📋 Requirements
- Files must run on **Ubuntu 18.04 LTS** using Node.js (v12.x.x).
- Files should use the `.js` extension and follow **ESLint** standards.
- Include a `README.md` file at the root of the project directory.

## 🚀 Installation and Usage

### Prerequisites
1. Install Node.js v12:
    ```bash
    curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
    sudo apt-get install -y nodejs
    ```

2. Install MongoDB and Redis:
    ```bash
    sudo apt-get install -y mongodb redis
    ```

3. Install required npm packages:
    ```bash
    npm install
    ```

### Running the Server
Start the application:
```bash
npm run start-server
```

### Running Workers
Start background workers:
```bash
npm run start-worker
```

## 📝 Features
### Core Features
1. User Authentication:
      - Login and generate tokens.
      - Logout and invalidate tokens.

2. File Management:
      - Upload files (text, images).
      - Manage public/private access.
      - Retrieve file content with MIME types.

3. File Viewing and Pagination:
      - List files with pagination support.
      - Retrieve individual file metadata.

4. Image Thumbnail Generation:
      - Generate thumbnails (100px, 250px, 500px).
        
5. Statistics:
      - Monitor number of users and files.

### Endpoints Overview

| **Method** | **Endpoint**           | **Description**                              |
|------------|-------------------------|----------------------------------------------|
| GET        | `/status`              | Check Redis and MongoDB connectivity.        |
| GET        | `/stats`               | Retrieve user and file statistics.           |
| POST       | `/users`               | Register a new user.                         |
| GET        | `/connect`             | Authenticate and generate a token.           |
| GET        | `/disconnect`          | Logout and invalidate token.                 |
| GET        | `/users/me`            | Retrieve authenticated user details.         |
| POST       | `/files`               | Upload a file.                               |
| GET        | `/files/:id`           | Retrieve file metadata by ID.                |
| GET        | `/files`               | List files with optional pagination.         |
| PUT        | `/files/:id/publish`   | Make a file public.                          |
| PUT        | `/files/:id/unpublish` | Make a file private.                         |
| GET        | `/files/:id/data`      | Retrieve file content with optional size.    |

## 🧠 Key Concepts
- **Redis**: Efficiently cache temporary data and manage authentication tokens.
- **MongoDB**: Store persistent user and file metadata.
- **Asynchronous Processing**: Use Kue to handle background tasks like image resizing or email notifications.
- **File Management**: Manage file uploads, directory structures, and access control.

## 🌐 Resources
- [Node JS getting started](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs)
- [Process API doc](https://node.readthedocs.io/en/latest/api/process/)
- [Express getting started](https://expressjs.com/en/starter/installing.html)
- [Mocha documentation](https://mochajs.org/)
- [Nodemon documentation](https://github.com/remy/nodemon#nodemon)
- [MongoDB](https://github.com/mongodb/node-mongodb-native)
- [Bull](https://github.com/OptimalBits/bull)
- [Image thumbnail](https://www.npmjs.com/package/image-thumbnail)
- [Mime-Types](https://www.npmjs.com/package/mime-types)
- [Redis](https://github.com/redis/node-redis)

## ⚖️ License
This project is part of the ALX Software Engineering Program.  
© 2024 ALX. All rights reserved.
