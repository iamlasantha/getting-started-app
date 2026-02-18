# Getting Started App

A simple Todo List application built with Node.js, Express, and Docker. This project demonstrates a containerized REST API application with data persistence.

## 🚀 Features

- **Item Management**: Create, Read, Update, and Delete (CRUD) todo items.
- **Persistence**: Supports SQLite and MySQL databases.
- **Dockerized**: Fully containerized for easy deployment.
- **REST API**: Clean JSON API endpoints.

## 🛠️ Tech Stack

- **Runtime**: Node.js (CommonJS)
- **Framework**: Express.js
- **Database**: SQLite (default) / MySQL
- **Containerization**: Docker
- **Utilities**: uuid, wait-port

## 🏁 Getting Started

### Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop) installed and running.
- (Optional) [Node.js](https://nodejs.org/) v18+ for local development.

### 🐳 Running with Docker (Recommended)

1.  **Build the image:**
    ```bash
    docker build -t getting-started .
    ```

2.  **Run the container:**
    ```bash
    docker run -dp 3000:3000 getting-started
    ```

3.  **Access the app:**
    Open [http://localhost:3000](http://localhost:3000) in your browser.

### 💻 Running Locally

1.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```

2.  **Start the server:**
    ```bash
    npm run dev
    # or
    yarn dev
    ```

The server will start on port `3000`.

## 🔌 API Endpoints

| Method | Endpoint | Description | Body Parameters |
| :--- | :--- | :--- | :--- |
| `GET` | `/items` | Get all todo items | None |
| `POST` | `/items` | Create a new item | `{ "name": "Item Name" }` |
| `PUT` | `/items/:id` | Update an item | `{ "name": "New Name", "completed": boolean }` |
| `DELETE` | `/items/:id` | Delete an item | None |

## 📁 Project Structure

```
├── src/
│   ├── persistence/       # Database connection logic (SQLite/MySQL)
│   ├── routes/            # API Route handlers
│   ├── static/            # Frontend static files (HTML/CSS/JS)
│   └── index.js           # App entry point
├── Dockerfile             # Docker configuration
├── package.json           # Dependencies and scripts
└── README.md              # Project documentation
```

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## 📄 License

This project is licensed under the MIT License.