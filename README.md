# Conversational AI Project

A voice-based conversational AI system that combines LLMs with voice capabilities.

## Features

- Voice-only interaction
- Real-time speech-to-text and text-to-speech
- Configurable LLM integration
- Conversation history
- Context awareness
- Custom knowledge base integration
- Male/Female voice selection

## Tech Stack

### Backend

- Go 1.21+
- Gin web framework
- WebSocket for real-time communication
- Google Cloud Speech-to-Text
- Google Cloud Text-to-Speech
- PostgreSQL
- Redis
- Vector database for knowledge base

### Frontend

- React 18
- TypeScript
- TailwindCSS
- WebSocket client
- Web Audio API

## Project Structure

```
.
├── backend/
│   ├── cmd/
│   │   └── server/        # Main application entry point
│   ├── internal/
│   │   ├── api/          # API handlers and middleware
│   │   ├── config/       # Configuration management
│   │   ├── models/       # Data models
│   │   ├── services/     # Business logic
│   │   └── utils/        # Utility functions
│   └── pkg/
│       ├── llm/          # LLM integration
│       ├── voice/        # Voice processing
│       └── knowledge/    # Knowledge base management
├── frontend/             # React frontend application
└── docs/                # Project documentation
```

## Getting Started

### Prerequisites

- Go 1.21 or higher
- Node.js 18 or higher
- Docker and Docker Compose
- Google Cloud account with Speech-to-Text and Text-to-Speech APIs enabled

### Backend Setup

1. Navigate to the backend directory
2. Install dependencies:
   ```bash
   go mod download
   ```
3. Set up environment variables:
   ```bash
   cp .env.example .env
   ```
4. Run the server:
   ```bash
   go run cmd/server/main.go
   ```

### Frontend Setup

1. Navigate to the frontend directory
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables:
   ```bash
   cp .env.example .env
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

## Environment Variables

### Backend

- `PORT`: Server port (default: 8080)
- `GOOGLE_APPLICATION_CREDENTIALS`: Path to Google Cloud credentials
- `DATABASE_URL`: PostgreSQL connection string
- `REDIS_URL`: Redis connection string
- `VECTOR_DB_URL`: Vector database connection string

### Frontend

- `VITE_API_URL`: Backend API URL
- `VITE_WS_URL`: WebSocket URL

## Development Timeline

- Week 1: Foundation

  - Project setup
  - Core backend services
  - Basic frontend structure
  - Voice processing integration

- Week 2: Core Features

  - LLM integration
  - Conversation management
  - Knowledge base integration
  - Real-time communication

- Week 3: Polish & Launch
  - UI/UX refinement
  - Performance optimization
  - Testing and bug fixes
  - Deployment and monitoring

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request
