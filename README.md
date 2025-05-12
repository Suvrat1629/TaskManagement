# Task Management Application

A full-stack task management application built with the MERN stack (MongoDB, Express.js, React, Node.js). This app allows users to create, read, update, and delete tasks, providing a user-friendly interface for managing daily tasks efficiently. The backend is deployed on [Render](https://taskmanagement-axgs.onrender.com), and the frontend is hosted on [Vercel](https://task-management-nine-beige.vercel.app).

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
  - [Prerequisites](#prerequisites)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Deployment](#deployment)
  - [Deploying Backend on Render](#deploying-backend-on-render)
  - [Deploying Frontend on Vercel](#deploying-frontend-on-vercel)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Task Management**: Create, edit, delete, and view tasks.
- **Responsive Design**: Accessible on both desktop and mobile devices.
- **User-Friendly Interface**: Intuitive UI for seamless task management.
- **CORS Support**: Configured to allow cross-origin requests from the frontend.
- **RESTful API**: Backend provides endpoints for task CRUD operations.

## Technologies Used
- **Frontend**:
  - React.js
  - Axios (for API requests)
  - CSS (or a CSS framework like Tailwind CSS, if used)
- **Backend**:
  - Node.js
  - Express.js
  - MongoDB
  - Mongoose (MongoDB ORM, if used)
- **Deployment**:
  - Render (backend)
  - Vercel (frontend)
- **Other**:
  - CORS middleware

## Setup Instructions

### Prerequisites
- Node.js (v18.x or later)
- npm or Yarn
- MongoDB (local or cloud, e.g., MongoDB Atlas)
- Git
- Accounts on [Render](https://render.com) and [Vercel](https://vercel.com) for deployment

### Backend Setup
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Suvrat1629/TaskManagement.git
   cd TaskManagement/server
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Run the Backend**:
   ```bash
   npm start
   ```
   The server will run at `http://localhost:3000` and is configured to connect to the frontend at `https://task-management-nine-beige.vercel.app`.

### Frontend Setup
1. **Navigate to the Frontend Directory**:
   ```bash
   cd TaskManagement/Frontend
   ```

2. **Install Dependencies**:
   ```bash
   cd Backend
   npm install
   ```

3. **Run the Frontend**:
   ```bash
   cd Frontend
   npm run dev
   ```
   The app will open at `http://localhost:3000` and is configured to communicate with the backend at `https://taskmanagement-axgs.onrender.com`.

## Deployment

### Deploying Backend on Render
1. **Push Code to GitHub**:
   Ensure your repository is pushed to GitHub:
   ```bash
   git push origin main
   ```

2. **Create a Web Service on Render**:
   - Log in to [Render](https://render.com).
   - Click **New** > **Web Service** and connect your GitHub repository.
   - Configure:
     - **Environment**: Node.js
     - **Root Directory**: `Backend`
     - **Build Command**: `npm install`
     - **Start Command**: `npm start`

3. **Deploy**:
   - Click **Create Web Service** to deploy.
   - The backend will be accessible at `https://taskmanagement-axgs.onrender.com`.

### Deploying Frontend on Vercel
1. **Push Code to GitHub**:
   Ensure the `Frontend` folder is part of the repository.

2. **Create a New Project on Vercel**:
   - Log in to [Vercel](https://vercel.com).
   - Click **New Project** and import your GitHub repository.
   - Configure:
     - **Framework Preset**: React
     - **Root Directory**: `Frontend`
     - **Build Command**: `npm run build`
     - **Output Directory**: `build`

3. **Deploy**:
   - Click **Deploy** to launch the frontend.
   - The frontend will be accessible at `https://task-management-nine-beige.vercel.app`.

## API Endpoints
- **GET** `/api/tasks`: Retrieve all tasks.
- **POST** `/api/tasks`: Create a new task.
- **PUT** `/api/tasks/:id`: Update a task by ID.
- **DELETE** `/api/tasks/:id`: Delete a task by ID.

**Example Request** (GET tasks):
```bash
curl https://taskmanagement-axgs.onrender.com/api/tasks
```

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

Please follow the [Contribution Guidelines](CONTRIBUTING.md) (if available).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
