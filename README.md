# Backend Server

This is a lightweight backend server built with **Express** and **WebSocket** that enables real-time data broadcasting to multiple connected clients. It also provides an HTTP endpoint for broadcasting data to all WebSocket clients.

## Features

* **Express.js** server with a `/broadcast` endpoint
* **WebSocket** server for real-time communication
* **CORS** enabled
* Uses `body-parser` for JSON request handling
* Supports both production and development modes

## Installation

1. **Clone the repository:**

   ```bash
   git clone <your-repo-url>
   cd backend-server
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

## Scripts

| Script | Command       | Description                     |
| ------ | ------------- | ------------------------------- |
| start  | `npm start`   | Starts the server using Node.js |
| dev    | `npm run dev` | Starts the server with Nodemon  |

## Usage

### Start the server

```bash
npm start
```

Server will run on port `1234` by default (or the value of `PORT` in your environment variables).

### WebSocket Endpoint

Clients can connect to:

```
ws://localhost:1234
```

### HTTP Broadcast Endpoint

Send a POST request to:

```
http://localhost:1234/broadcast
```

**Request body (JSON):**

```json
{
  "message": "Hello clients!"
}
```

**Response:**

```json
{
  "message": "Data broadcasted successfully",
  "data": {
    "message": "Hello clients!"
  }
}
```

## Project Structure

```
backend-server/
├── package.json      # Project metadata and dependencies
└── server.js         # Main server code
```

## Dependencies

* [express](https://www.npmjs.com/package/express)
* [ws](https://www.npmjs.com/package/ws)
* [body-parser](https://www.npmjs.com/package/body-parser)
* [nodemon](https://www.npmjs.com/package/nodemon) (for development)

## License

This project is licensed under the ISC License.

---

Let me know if you want this customized further (e.g., Docker instructions, testing info, etc.).
