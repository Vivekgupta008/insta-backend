# Backend Setup Instructions

## Installation

1. Navigate to the server directory:
```bash
cd server
```

2. Install dependencies:
```bash
npm install
```

## Running the Server

Start the backend server:
```bash
npm start
```

Or for development with auto-reload:
```bash
npm run dev
```

The server will run on `http://localhost:5000`

## API Endpoints

- **POST** `/api/verify` - Submit username and password (stores in MongoDB)
- **GET** `/api/health` - Health check endpoint
- **GET** `/api/users` - Get all users (for testing, excludes passwords)

## MongoDB

The server connects to MongoDB Atlas using the provided connection string.
Data is stored in the `users` collection with the following schema:
- username (String)
- password (String)
- timestamp (Date)

## Testing

Test the API using curl:
```bash
curl -X POST http://localhost:5000/api/verify \
  -H "Content-Type: application/json" \
  -d '{"username":"testuser","password":"testpass"}'
```

