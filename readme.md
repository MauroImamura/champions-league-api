# Champions League API

![Champions League API Cover](./assets/champions-league-api-cover.png)

## Overview

Champions League API is a **Node.js** and **TypeScript** project built using the **Express** framework. This API provides data on players and clubs participating in the Champions League, allowing users to perform CRUD operations on players and retrieve club information.  

## Features

- **Player Data**: Create, read, update, and delete players.
- **Club Data**: Retrieve club information.
- **Express Router**: Organized route handling for clean and scalable code.
- **CORS Support**: Ensures API accessibility across different origins.

## Technologies Used

- **Node.js**: Backend runtime environment.
- **Express**: Fast and minimalist web framework.
- **TypeScript**: Type safety and improved developer experience.
- **Tsup**: Bundler for compiling TypeScript code.
- **TSX**: Node.js enhanced with TypeScript support.

## API Routes

### **Players**
- `GET /players`: Get all players.
- `GET /players/:id`: Get player by ID.
- `POST /players`: Create a new player.
- `PATCH /players/:id`: Update an existing player.
- `DELETE /players/:id`: Delete a player by ID.

### **Clubs**
- `GET /clubs`: Get all clubs.
- `GET /clubs/:id`: Get club by ID.

## Prerequisites

- **Node.js** (>= 14.x)
- **npm** (>= 6.x)

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/MauroImamura/champions-league-api.git
   cd champions-league-api
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Create `.env` File** and set PORT value:
   ```
   PORT=3300
   ```

## Running the Project

### **Development Mode**:
```bash
npm run start:dev
```

### **Watch Mode**:
This mode restarts the server on code changes:
```bash
npm run start:watch
```

### **Production Build and Run**:
1. Build the project:
   ```bash
   npm run dist
   ```

2. Start the built code:
   ```bash
   npm run start:dist
   ```

## Folder Structure

```
champions-league-api/
│
├── src/
│   ├── server.ts      # API server setup
│   ├── routes/        # Express route handlers
│   ├── controllers/   # Requests and response handling for API operations
│   ├── services/      # Business logic for API operations
│   ├── models/        # TypeScript interfaces for data models
│   ├── repositories/  # TypeScript repositories for data handle
│   └── data/
│       └── players.json   # Sample player data
│       └── clubs.json     # Sample club data
│
├── .env               # Environment variables
├── package.json       # Project dependencies and scripts
├── tsconfig.json      # TypeScript configuration
└── README.md          # Project documentation
```

## Example Player Model

```typescript
export interface playerModel {
  id: number;
  name: string;
  club: string;
  nationality: string;
  position: string;
  statistics: {
    Overall: number;
    Pace: number;
    Shooting: number;
    Passing: number;
    Dribbling: number;
    Defending: number;
    Physical: number;
  };
}
```

## Example Club Model

```typescript
export interface clubModel {
  id: number;
  name: string;
}
```

## Contributing

Contributions are welcome! Please fork the repository and open a pull request with your improvements.

## Acknowledgments

This project was made during dio.me node bootcamp, based on Felipe Aguiar's course.

