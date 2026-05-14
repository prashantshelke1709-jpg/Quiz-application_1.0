# 📝 Online Quiz System

A full-featured web-based quiz platform that allows administrators to create and manage quizzes, and users to take quizzes and track their performance.

---

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Configuration](#configuration)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

---

## ✨ Features

### For Students / Users
- Register and log in securely
- Browse available quizzes by category or difficulty
- Take timed quizzes with multiple question types (MCQ, True/False, Short Answer)
- View instant results and detailed score breakdown
- Track quiz history and performance over time

### For Admins / Instructors
- Create, edit, and delete quizzes
- Add questions with multiple answer options and set correct answers
- Set quiz duration, passing score, and availability window
- View all student submissions and analytics
- Export results as CSV/PDF

---

## 🛠️ Tech Stack

| Layer        | Technology                          |
|--------------|-------------------------------------|
| Frontend     | React.js / HTML5 / CSS3 / Bootstrap |
| Backend      | Node.js / Express.js                |
| Database     | MongoDB / PostgreSQL                |
| Auth         | JWT (JSON Web Tokens)               |
| Testing      | Jest / Mocha                        |
| Deployment   | Docker / AWS / Heroku               |

> **Note:** Adjust this table to match your actual stack.

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v16 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB](https://www.mongodb.com/) or your preferred database
- [Git](https://git-scm.com/)

---

## ⚙️ Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/online-quiz-system.git

# 2. Navigate into the project directory
cd online-quiz-system

# 3. Install backend dependencies
cd server
npm install

# 4. Install frontend dependencies
cd ../client
npm install
```

---

## 🔧 Configuration

Create a `.env` file in the `server/` directory and add the following environment variables:

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/quizdb
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRES_IN=7d
NODE_ENV=development
```

> ⚠️ Never commit your `.env` file. It is already listed in `.gitignore`.

---

## 📁 Project Structure

```
online-quiz-system/
├── client/                  # Frontend (React.js)
│   ├── public/
│   └── src/
│       ├── components/      # Reusable UI components
│       ├── pages/           # Page-level components
│       ├── services/        # API call handlers
│       └── App.js
│
├── server/                  # Backend (Node.js / Express)
│   ├── controllers/         # Route logic
│   ├── models/              # Database models/schemas
│   ├── routes/              # API route definitions
│   ├── middleware/          # Auth & error handling middleware
│   └── server.js
│
├── .env.example             # Sample environment variables
├── .gitignore
├── README.md
└── docker-compose.yml       # (optional) Docker setup
```

---

## 📡 API Endpoints

### Auth
| Method | Endpoint             | Description          |
|--------|----------------------|----------------------|
| POST   | `/api/auth/register` | Register a new user  |
| POST   | `/api/auth/login`    | Login and get token  |

### Quizzes
| Method | Endpoint              | Description                  |
|--------|-----------------------|------------------------------|
| GET    | `/api/quizzes`        | Get all available quizzes    |
| GET    | `/api/quizzes/:id`    | Get a specific quiz          |
| POST   | `/api/quizzes`        | Create a new quiz (Admin)    |
| PUT    | `/api/quizzes/:id`    | Update a quiz (Admin)        |
| DELETE | `/api/quizzes/:id`    | Delete a quiz (Admin)        |

### Submissions
| Method | Endpoint                   | Description                      |
|--------|----------------------------|----------------------------------|
| POST   | `/api/submissions`         | Submit quiz answers              |
| GET    | `/api/submissions/user`    | Get current user's history       |
| GET    | `/api/submissions/:quizId` | Get all submissions for a quiz (Admin) |

---

## 💻 Usage

### Run in Development Mode

```bash
# Start backend server
cd server
npm run dev

# Start frontend (in a new terminal)
cd client
npm start
```

The app will be available at `http://localhost:3000`  
The API runs at `http://localhost:5000`

### Run with Docker

```bash
docker-compose up --build
```

---

## 🧪 Running Tests

```bash
# Backend tests
cd server
npm test

# Frontend tests
cd client
npm test
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

Please ensure your code follows the project's coding standards and includes relevant tests.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📬 Contact

Have questions or suggestions? Feel free to open an issue or reach out:

- **Email:** your-email@example.com
- **GitHub:** [your-username](https://github.com/your-username)

---

> Made with ❤️ for better learning experiences.
