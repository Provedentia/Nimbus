# CoFund - Personal Finance Management Platform

A comprehensive full-stack personal finance application built with React Native and Node.js, featuring bank account integration, AI-powered financial insights, and real-time transaction management.

## Overview

CoFund is a modern financial management platform that helps users track expenses, manage budgets, and gain insights into their spending patterns. The application integrates with banking institutions through Teller API and provides intelligent financial guidance through AI-powered chat functionality.

## Key Features

- **Bank Account Integration**: Secure connection to bank accounts via Teller API for automatic transaction syncing
- **Real-time Financial Dashboard**: Live view of account balances, recent transactions, and spending analytics
- **AI Financial Assistant**: Intelligent chatbot powered by Groq LLM for personalized financial advice
- **Budget Management**: Create and track budgets with visual progress indicators
- **Transaction Categorization**: Automatic and manual categorization of expenses and income
- **Secure Authentication**: JWT-based authentication with encrypted password storage
- **Cross-Platform Mobile App**: React Native application with iOS and Android support

## Technology Stack

### Backend
- **Runtime**: Node.js with Express.js framework
- **Database**: PostgreSQL with Supabase integration
- **Authentication**: JWT tokens with bcrypt password hashing
- **External APIs**: Teller API for banking, Groq API for AI processing
- **Testing**: Jest with comprehensive test suites
- **Architecture**: RESTful API with modular controller structure

### Frontend
- **Framework**: React Native with TypeScript
- **State Management**: Context API with custom hooks
- **Navigation**: React Navigation for screen routing
- **UI Components**: Custom component library with glassmorphic design
- **Development**: Expo for cross-platform development
- **Testing**: Jest with React Native Testing Library

## Project Structure

```
cofund/
├── backend/                    # Node.js Express API server
│   ├── src/
│   │   ├── controllers/       # API request handlers
│   │   ├── routes/           # Express route definitions
│   │   ├── middleware/       # Authentication and validation
│   │   ├── services/         # External API integrations
│   │   ├── models/           # Data models and schemas
│   │   ├── migrations/       # Database schema migrations
│   │   └── utils/            # Helper functions and utilities
│   ├── tests/                # Backend test suites
│   └── documentation/        # API documentation and contracts
├── frontend/                  # React Native mobile application
│   ├── src/
│   │   ├── screens/          # Application screens
│   │   ├── components/       # Reusable UI components
│   │   ├── navigation/       # Navigation configuration
│   │   ├── contexts/         # React contexts for state management
│   │   ├── hooks/            # Custom React hooks
│   │   ├── api/              # API service layer
│   │   ├── types/            # TypeScript type definitions
│   │   └── utils/            # Utility functions
│   ├── assets/               # Images, icons, and static assets
│   └── docs/                 # Frontend documentation
└── package.json              # Root project configuration
```

## Setup and Installation

### Prerequisites
- Node.js (v16 or higher)
- PostgreSQL database
- Expo CLI for React Native development
- Teller API credentials
- Groq API key

### Backend Setup
```bash
cd backend
npm install
cp config/env-template.js config/env.js
# Configure environment variables in config/env.js
npm run setup-database
npm run dev
```

### Frontend Setup
```bash
cd frontend
npm install
cp env.example .env
# Configure environment variables in .env
npm start
```

### Environment Configuration

The application requires several environment variables for proper functionality:

- **Database**: PostgreSQL connection strings for Supabase
- **Authentication**: JWT secret keys and token expiration settings
- **External APIs**: Teller API credentials and Groq API keys
- **Security**: Encryption keys and certificate paths

## Architecture Highlights

### Security Implementation
- End-to-end encryption for sensitive financial data
- Secure API communication with HTTPS enforcement
- Token-based authentication with automatic refresh
- Input validation and sanitization at all endpoints

### Database Design
- Normalized schema with proper foreign key relationships
- Database triggers for automatic balance calculations
- Migration system for schema version control
- Optimized indexes for query performance

### API Design
- RESTful endpoints with consistent response formats
- Comprehensive error handling and logging
- Rate limiting and request validation middleware
- Webhook support for real-time bank data updates

### Mobile Application
- Responsive design optimized for mobile devices
- Offline capability with data synchronization
- Biometric authentication support
- Push notifications for important account updates

## Testing and Quality Assurance

The project includes comprehensive testing coverage:

- **Unit Tests**: Individual function and component testing
- **Integration Tests**: API endpoint and database interaction testing
- **Authentication Tests**: Security and authorization flow validation
- **Component Tests**: React Native component rendering and interaction testing

## Documentation

Extensive documentation is provided for developers and stakeholders:

- **API Documentation**: Complete endpoint reference with examples
- **Architecture Decision Records (ADRs)**: Technical decision documentation
- **Database Schema**: Entity relationship diagrams and migration guides
- **Style Guide**: UI/UX design principles and component standards
- **Deployment Guide**: Production deployment and configuration instructions

## Development Features

- **Hot Reload**: Instant code updates during development
- **TypeScript Support**: Full type safety and IDE integration
- **Linting and Formatting**: ESLint and Prettier configuration
- **Pre-commit Hooks**: Automated code quality checks
- **Continuous Integration**: Automated testing and deployment pipelines

## Production Considerations

The application is designed with production deployment in mind:

- **Scalability**: Modular architecture supports horizontal scaling
- **Monitoring**: Comprehensive logging and error tracking
- **Performance**: Optimized database queries and efficient data loading
- **Compliance**: Financial data handling following industry best practices

## Contributing

This project demonstrates modern full-stack development practices with attention to security, scalability, and maintainability. The codebase showcases proficiency in:

- Full-stack JavaScript/TypeScript development
- RESTful API design and implementation
- React Native mobile application development
- Database design and optimization
- Security best practices for financial applications
- Test-driven development methodologies
- DevOps and deployment automation

---

This project represents a production-ready financial management platform with enterprise-level architecture and comprehensive feature set suitable for real-world deployment.