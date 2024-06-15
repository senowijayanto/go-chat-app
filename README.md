# Real-Time Chat Application with Redis Pub/Sub, Golang, and WebSocket

## Description

This is a real-time chat application built using Golang, Redis Pub/Sub, and WebSocket. The application allows multiple users to join a chat room by entering a username, and then send and receive messages in real-time. The backend is powered by Golang with Redis handling the Pub/Sub messaging, and the frontend uses HTML and JavaScript to handle user interactions and WebSocket connections.

## Stack

- **Backend**: Golang
  - WebSocket for real-time communication
  - Redis Pub/Sub for message broadcasting
- **Frontend**: HTML, CSS, and JavaScript
  - WebSocket for real-time updates

## Prerequisites

Before running the application, ensure you have the following installed:

1. **Redis**: Install Redis on your machine. You can download it from [redis.io/download](https://redis.io/download).
2. **Golang**: Install Go from [golang.org/dl](https://golang.org/dl/).

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/chat-app.git
   cd chat-app
   ```

2. Install the necessary Go packages:
   ```bash
   go get github.com/go-redis/redis/v8
   go get github.com/gorilla/mux
   ```

## Running the Application

### Start Redis

Open a terminal window and run the following command to start the Redis server:
```bash
redis-server
```

Keep this terminal window open while you proceed with the next steps.

### Run the Golang Server

Open a new terminal window or tab, navigate to the directory where your Golang files (`main.go`) are located, and run:
```bash
go run main.go
```

This command starts the HTTP server on `localhost:8080`.

### Access the Chat Interface

Open your web browser and navigate to:
```
http://localhost:8080
```

1. **Enter Username**: You will see an input field to enter your username.
2. **Press Enter or Click Submit**: After entering your username, press Enter or click the "Submit" button to join the chat.

### Simulate Chat Interaction

To simulate interactions between multiple users:

1. Open one browser window or tab and navigate to `http://localhost:8080`. Enter a username to join the chat as User 1.
2. Open another browser window or tab (preferably a different browser or an incognito/private window) and navigate to `http://localhost:8080` again. Enter a different username to join the chat as User 2.

### Sending Messages

- Type a message in the input field and press Enter or click the "Send" button.
- The message will appear in the chat interface in real-time.
- Messages from other users will also appear in real-time.

## Code Structure

- **main.go**: The main server file that sets up the HTTP routes and WebSocket connections.
- **web/**: The directory containing frontend files (HTML, CSS, JavaScript).

## Additional Notes

- **Error Handling**: Implement error handling and validation for username input and message sending to improve user experience.
- **Enhancements**: Consider adding features such as message timestamps, user authentication, multiple chat rooms, or message persistence for a more robust application.