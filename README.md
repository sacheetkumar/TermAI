# TermAI 🚀

[![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white)](https://socket.io/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

**TermAI** is an AI-powered cloud terminal that enables developers to code from anywhere, at any time, using any device. With a browser-based terminal interface, integrated AI automation, and seamless GitHub synchronization, TermAI brings a premium development environment to your fingertips.

---

## ✨ Key Features

-   **🌐 Browser-Based Terminal**: Full-featured interactive terminal powered by `xterm.js` and `node-pty`.
-   **🤖 AI Assistant**: Integrated AI to help with command execution, task automation, and real-time coding answers.
-   **⌨️ Neovim Integration**: Use your favorite modal editor directly in the browser terminal.
-   **📂 GitHub Synchronization**: Clone, save, and manage your projects directly from/to GitHub.
-   **🧠 Context-Aware AI**: Provide file and directory context to the AI for smarter assistance.
-   **📱 Mobile Friendly**: Code on the go from your mobile, tablet, or laptop.
-   **💬 Interactive Chat**: Context-based chat mode for follow-up questions and debugging.
-   **🔍 Knowledge Base**: Real-time answers from Stack Exchange integrated into your terminal workflow.

---

## 🛠️ Tech Stack

### Frontend
-   **Framework**: [Next.js 14](https://nextjs.org/) (App Router)
-   **Styling**: Tailwind CSS, Radix UI, Framer Motion
-   **State Management**: Recoil, TanStack Query
-   **Terminal**: xterm.js
-   **Auth**: Clerk

### Backend
-   **Server**: Node.js, Express
-   **Real-time**: Socket.io
-   **Terminal Proxy**: node-pty
-   **Database**: MongoDB with Prisma ORM

### Infrastructure
-   **Containerization**: Docker
-   **Cloud**: Google Cloud Run

---

## 🚀 Getting Started

### Prerequisites
-   [Node.js](https://nodejs.org/) (v18+)
-   [pnpm](https://pnpm.io/) or [npm](https://www.npmjs.com/)
-   [Docker](https://www.docker.com/) (optional, for containerized setup)
-   [MongoDB](https://www.mongodb.com/) instance

### 1. Setting up the Socket Server
The socket server handles the terminal sessions and AI interactions.

1.  Navigate to the `server` directory:
    ```bash
    cd server
    ```
2.  Install dependencies:
    ```bash
    npm install # or pnpm install
    ```
3.  Configure environment variables (see `.env.example`):
    -   `PORT`: Port for the socket server (default: `3000`)
    -   `APP_URL`: URL of the frontend application
    -   `API_URL`: URL of the backend API
4.  Start the server:
    ```bash
    npm run dev
    ```

### 2. Setting up the Web Application
The frontend provides the dashboard and terminal interface.

1.  Navigate to the `web` directory:
    ```bash
    cd web
    ```
2.  Install dependencies:
    ```bash
    npm install # or pnpm install
    ```
3.  Configure environment variables:
    Create a `.env` file based on the required services (Clerk, Database, etc.).
    ```bash
    # Example (partial list)
    DATABASE_URL="mongodb+srv://..."
    NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="..."
    CLERK_SECRET_KEY="..."
    NEXT_PUBLIC_SOCKET_SERVER_URL="http://localhost:3000"
    ```
4.  Initialize Prisma:
    ```bash
    npx prisma generate
    ```
5.  Start the development server:
    ```bash
    npm run dev
    ```
    The application will be available at [http://localhost:4000](http://localhost:4000).

---

## 🐳 Docker Setup
You can run the server using Docker:
```bash
cd server
docker compose up -d
```

---

## 📄 License
Detailed license information coming soon.

---

Developed with ❤️ for developers who love the terminal.