# Real-Time Chat Application

This is a real-time chat application built using **Spring Boot** and **WebSockets** with STOMP messaging. It allows users to join a chat room, send messages, and receive updates when other users join or leave.

## Features
- Real-time messaging using **WebSockets**
- Users receive notifications when someone joins or leaves
- Built with **Spring Boot 3 & STOMP protocol**
- Uses **SockJS** for WebSocket fallback support

## Tech Stack
- **Backend:** Spring Boot 3, WebSockets, STOMP, SockJS
- **Frontend:** HTML, JavaScript, CSS
- **Messaging:** STOMP over WebSockets

## Setup & Installation

### Prerequisites
Make sure you have the following installed:
- Java 17+
- Maven 3+
- Web browser

### Clone the Repository
```sh
git clone https://github.com/spring-web-chat.git
cd spring-web-chat
```

### Build the Application
```sh
mvn clean install
```

### Run the Application
The application runs on port **1010** (default changed from 8080).
```sh
mvn spring-boot:run
```

### WebSocket Endpoint
- **STOMP WebSocket URL:** `ws://localhost:1010/ws`
- **STOMP Subscribe Topic:** `/topic/public`
- **STOMP Message Sending:** `/app/chat.sendMessage`
- **STOMP User Join:** `/app/chat.addUser`

## Usage
1. Open the browser and navigate to:
   ```
   http://localhost:1010/
   ```
2. Enter a username and click **Join**.
3. Start chatting in real time!
4. Messages are broadcasted to all users in the chat room.
5. When a user leaves, a message is displayed.



## API Endpoints
| Endpoint                  | Description                     |
|---------------------------|---------------------------------|
| `/ws`                     | WebSocket connection endpoint  |
| `/topic/public`           | Topic for receiving messages   |
| `/app/chat.sendMessage`   | Send chat messages             |
| `/app/chat.addUser`       | Notify when a user joins       |

## Troubleshooting
- **Cannot connect to WebSocket:** Ensure the app is running on port `1010`.
- **Message not sent/received:** Check WebSocket subscription and server logs.
- **Application fails to start:** Ensure dependencies are installed and port `1010` is not in use.

## License
This project is licensed under the MIT License.

## Author
- **Your Name** (Update this with your name)
- GitHub: [your-profile](https://github.com/your-profile)

---
Enjoy chatting! 🚀

