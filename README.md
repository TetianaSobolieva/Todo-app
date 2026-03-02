# React Todo App with API
A full-stack Todo application with user authentication, built with React + TypeScript on the frontend and a custom Node.js REST API backed by PostgreSQL.

## 🔗 Demo
[Live Demo](https://tetianasobolieva.github.io/Todo-app/)
## 🛠 Tech Stack
**Frontend**
* **React** — component-based UI
* **TypeScript** — static typing
* **SCSS** — component styles
* **Vite** — build tool and dev server
**Backend**
* **Node.js** — custom REST API
* **PostgreSQL** — relational database
* **bcrypt** — password hashing
* **JWT** — token-based authentication
**Tooling**
* **Cypress** — end-to-end testing
* **ESLint** + Prettier + Stylelint — code quality and formatting

## 📁 Project Structure
```text
TODO-APP/
├── dist/
├── node_modules/
├── public/
├── src/
│   ├── api/
│   ├── components/
│   ├── styles/
│   ├── types/
│   └── utils/

```
## 🚀 Getting Started
### Prerequisites
- **Node.js v18+**
- **PostgreSQL running locally**
### Installation
```bash
# Clone the repository
git clone https://github.com/MaksOther/react_todo-app-with-api.git

# Navigate to the project
cd react_todo-app-with-api

# Install dependencies
npm install
```
### Environment Variables
Create a .env file in the root (or update the existing one)
### Running the App
```bash
# Start the frontend
npm start

# Start the backend (if separate)
npm run server
```
The app will be available at http://localhost:5173
### Running E2E Tests
```bash
npm run cypress:open
```
## 🔐 Authentication Flow
1. User registers with email and password
2. Password is hashed with bcrypt before storing in PostgreSQL
3. On login, server validates credentials and returns a JWT token
4. Token is stored on the client and sent with each API request
5. Protected routes require a valid token
