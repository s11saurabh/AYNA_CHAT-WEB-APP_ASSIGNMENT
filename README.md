# AYNA_CHAT-WEB-APP

## Overview
AYNA_CHAT-WEB-APP is a modern real-time chat application built using the MERN (MongoDB, Express.js, React, Node.js) stack. The application provides a seamless chat experience with real-time message delivery between user and server, user authentication, and a responsive design that works across all devices. This project was developed as part of an assignment to demonstrate WebSocket communication for instant messaging between client and server.

## Live Demo
NOTE:(Deployed link takes 30-40 sec to open.pls wait after clicking on it)
- **Deployed Site**: [https://realtalk-opov.onrender.com/login](https://realtalk-opov.onrender.com/login)

TESTING: feel free to signup with two different account by clicking on "Don`t have account" and use the implemented functionality

<img width="1467" alt="image" src="https://github.com/user-attachments/assets/302ebe40-89ef-4a76-ae2b-205dbe40e44e" />
<img width="1377" alt="image" src="https://github.com/user-attachments/assets/172bd983-56fe-4693-a2e9-5c30aa689dcf" />
<img width="1385" alt="image" src="https://github.com/user-attachments/assets/3153ca8c-a8ae-4c42-9411-4529ac4b8393" />
<img width="1467" alt="image" src="https://github.com/user-attachments/assets/a80d31b9-9e10-492f-857a-3e1d1f8b5486" />
<img width="1296" alt="image" src="https://github.com/user-attachments/assets/cb0b2792-2695-4eae-a16f-2d79cb4cd15d" />


## Technology Stack
- **Frontend**: React.js with Vite
- **Backend**: Node.js with Express.js
- **Database**: MongoDB
- **Real-time Communication**: Socket.IO
- **Authentication**: JSON Web Tokens (JWT)
- **Styling**: Tailwind CSS, DaisyUI
- **Deployment**: Render

## Project Structure

### Frontend Structure (Client)
```
client/
├── public/
├── src/
│   ├── assets/
│   │   ├── sounds/
│   │   └── react.svg
│   ├── components/
│   ├── context/
│   ├── hooks/
│   ├── pages/
│   ├── utils/
│   ├── zustand/
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .env
├── .eslintrc.js
├── .gitignore
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
└── vite.config.js
```

### Backend Structure (Server)
```
server/
├── controllers/
├── db/
│   └── connectToMongoDB.js
├── middleware/
│   └── protectRoute.js
├── models/
│   ├── conversation.model.js
│   ├── message.model.js
│   └── user.model.js
├── routes/
│   ├── auth.routes.js
│   ├── message.routes.js
│   └── user.routes.js
├── socket/
│   └── socket.js
├── utils/
│   └── generateToken.js
├── .env
├── .gitignore
├── package.json
└── server.js
```

## Key Features

### User Authentication
- Secure signup and login functionality
- JWT-based authentication
- Protected routes for authenticated users
- Password hashing for security
- Session management

### Real-time Communication
- WebSocket implementation using Socket.IO
- Instant message delivery between client and server
- Echo functionality: server sends back the same message to the client
- Connection state management
- Automatic reconnection handling

### Chat Functionality
- Server-client messaging
- Message history persistence
- Message timestamps
- Session management
- Message delivery status

### Data Storage
- MongoDB integration for persistent storage
- Local storage for client-side caching
- Message history management
- User data management
- Session storage

### User Interface
- Clean and intuitive chat interface
- Responsive design for all screen sizes
- Message threading
- Loading states and animations
- Error handling and notifications

## Installation and Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- npm or yarn package manager

### Frontend Setup
```bash
# Navigate to client directory
cd client

# Install dependencies
npm install

# Create .env file and add necessary environment variables
VITE_APP_API_URL=your_api_url
VITE_APP_SOCKET_URL=your_socket_url

# Start development server
npm run dev
```

### Backend Setup
```bash
# Navigate to server directory
cd server

# Install dependencies
npm install

# Create .env file and add necessary environment variables
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
NODE_ENV=development

# Start server
npm start
```

## API Documentation

### Authentication Endpoints
- `POST /api/auth/signup`: Register new user
- `POST /api/auth/login`: User login
- `POST /api/auth/logout`: User logout

### Message Endpoints
- `GET /api/messages/:conversationId`: Get conversation messages
- `POST /api/messages`: Send new message
- `PUT /api/messages/:messageId`: Update message
- `DELETE /api/messages/:messageId`: Delete message

### User Endpoints
- `GET /api/users`: Get all users
- `GET /api/users/:userId`: Get user profile
- `PUT /api/users/:userId`: Update user profile

## WebSocket Events
- `connection`: Client connects to server
- `disconnect`: Client disconnects from server
- `message`: New message event
- `echo`: Server echo response
- `online`: Connection status

## Deployment
The application is deployed on Render and can be accessed at:
- Live Demo: https://realtalk-opov.onrender.com/

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Socket.IO documentation
- MongoDB documentation
- React.js documentation
- Tailwind CSS community
- DaisyUI component library

## Repository
GitHub Repository: https://github.com/s11saurabh/AYNA_CHAT-WEB-APP_ASSIGNMENT

## Project Status
This project was developed as part of an assignment to demonstrate real-time chat functionality between client and server using WebSocket communication. The core features have been implemented according to the assignment requirements.
