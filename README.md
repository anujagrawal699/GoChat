# GoChat

A real-time chat application built with Go WebSocket backend and React frontend. This application demonstrates high-performance WebSocket communication with a modern React frontend interface.

## Features

- **Real-time Communication**: Instant message delivery using WebSocket protocol
- **Scalable Architecture**: Efficiently handles multiple concurrent connections
- **Modern UI**: Clean and responsive design built with React
- **Connection Pool**: Smart connection management for optimal performance
- **Component-Based Frontend**: Modular React components for maintainability

## Project Structure

```
└── anujagrawal699-GoChat/
    ├── backend/                 # Go WebSocket server
    │   ├── main.go             # Entry point
    │   ├── pkg/
    │   │   └── websocket/      # WebSocket implementation
    │   │       ├── pool.go     # Connection pool management
    │   │       ├── websocket.go # WebSocket utilities
    │   │       └── client.go   # Client connection handling
    │   └── go.mod              # Go dependencies
    └── frontend/               # React application
        ├── public/             # Static assets
        └── src/
            ├── api/            # API integration
            └── components/     # React components
                ├── ChatInput/  # Message input component
                ├── Header/     # App header
                ├── ChatHistory/# Message history
                └── Message/    # Individual message
```

## Technical Stack

### Backend
- **Go**: High-performance server-side language
- **Gorilla WebSocket**: Robust WebSocket implementation
- **Connection Pool**: Custom implementation for managing WebSocket connections
- **Client Handler**: Dedicated client connection management

### Frontend
- **React**: UI component library
- **SCSS**: Advanced styling with nested rules
- **WebSocket API**: Browser WebSocket for real-time communication
- **Component Architecture**: Modular design for maintainability

## Prerequisites

- Go >= 1.18
- Node.js >= 16
- npm >= 8
- Modern web browser with WebSocket support

## Installation

### Backend Setup
```bash
# Navigate to backend directory
cd backend

# Install dependencies
go mod tidy

# Start the server
go run main.go
```

### Frontend Setup
```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

## Component Details

### Backend Components

- **websocket.go**: 
  - Handles WebSocket connection upgrades
  - Manages message routing
  - Implements connection lifecycle

- **pool.go**:
  - Maintains active connection pool
  - Handles broadcasting messages
  - Manages client registration/deregistration

- **client.go**:
  - Manages individual client connections
  - Handles message reading/writing
  - Implements connection cleanup

### Frontend Components

- **ChatInput**:
  - Message composition interface
  - Emoji support
  - Input validation

- **ChatHistory**:
  - Message thread display
  - Auto-scrolling
  - Message grouping

- **Message**:
  - Individual message rendering
  - Timestamp display
  - Message status indicators

- **Header**:
  - Application branding
  - User status
  - Connection status display

## Environment Configuration

### Backend
```bash
# Default port configuration
export PORT=8080

# Optional configurations
export MAX_CONNECTIONS=100
export PING_INTERVAL=30s
```

### Frontend
```bash
# Update WebSocket connection in src/api/index.js
const socket = new WebSocket('ws://localhost:8080/ws')

# Environment variables
REACT_APP_WS_URL=ws://localhost:8080/ws
REACT_APP_API_TIMEOUT=5000
```

## Development Workflow

1. Start the backend server
2. Launch the frontend development server
3. Open http://localhost:3000 in your browser
4. Backend WebSocket endpoint available at ws://localhost:8080/ws

## Contribution Guidelines

1. Fork the repository
2. Create a feature branch
3. Commit changes with descriptive messages
4. Submit pull request with detailed description
