# TradeMate Architecture

## Project Overview

TradeMate is a full-stack mobile application designed for traders to record trades, manage risk, analyze performance, and improve trading discipline.

The application combines trading knowledge with modern software engineering practices using React Native, Go, and PostgreSQL.

---

# Architecture Type

TradeMate follows a:

**Full-Stack Modular Monolith Architecture**

The system consists of:

- One Mobile Application
- One Backend API
- One PostgreSQL Database

The backend follows a layered architecture:

```text
Handler → Service → Repository → Database
```

---

# Technology Stack

## Frontend

- React Native
- Expo
- TypeScript

## Backend

- Go
- Gin Framework
- JWT Authentication
- bcrypt Password Hashing

## Database

- PostgreSQL

## DevOps

- Git
- GitHub
- Docker

---

# High Level Architecture

```text
React Native Mobile App
        ↓
REST API / HTTPS
        ↓
Go Backend API
        ↓
PostgreSQL Database
```

---

# Repository Structure

```text
TradeMate/
│
├── mobile/
│
├── backend/
│
├── docs/
│
├── README.md
│
└── .gitignore
```

---

# Frontend Architecture

```text
mobile/
│
├── src/
│   ├── screens/
│   ├── components/
│   ├── services/
│   ├── navigation/
│   ├── storage/
│   ├── hooks/
│   ├── types/
│   └── utils/
```

## Responsibilities

- User Authentication Screens
- Trade Journal Screens
- Risk Calculator Screens
- Dashboard Screens
- Analytics Screens
- API Communication
- Local Token Storage

---

# Backend Architecture

```text
backend/
│
├── cmd/
├── config/
├── internal/
│   ├── auth/
│   ├── trades/
│   ├── risk/
│   ├── dashboard/
│   ├── analytics/
│   ├── marketdata/
│   └── middleware/
│
├── routes/
├── pkg/
└── migrations/
```

---

# Backend Layers

## Handler Layer

Responsibilities:

- Receive HTTP Requests
- Validate Request Format
- Return HTTP Responses

Example:

```text
POST /api/trades
```

---

## Service Layer

Responsibilities:

- Business Logic
- Risk Calculations
- Trade Analysis
- Validation Rules

---

## Repository Layer

Responsibilities:

- Database Queries
- Insert Records
- Read Records
- Update Records
- Delete Records

---

## Database Layer

Responsibilities:

- Data Storage
- Data Relationships
- Query Execution

Database:

```text
PostgreSQL
```

---

# Core Modules

## Authentication Module

Features:

- Signup
- Login
- JWT Authentication
- Profile Management

---

## Trade Journal Module

Features:

- Create Trade
- View Trades
- Update Trade
- Delete Trade
- Trade History

---

## Risk Management Module

Features:

- Risk Amount Calculation
- Position Size Calculation
- Risk Reward Ratio
- Profit/Loss Estimation

---

## Dashboard Module

Features:

- Total Trades
- Win Rate
- Total Profit/Loss
- Average Win
- Average Loss
- Best Trading Pair

---

## Analytics Module

Features:

- Emotion Tracking
- Mistake Analysis
- Performance Reports
- Setup Analysis

---

## Market Data Module

Future Features:

- Live Market Prices
- Candle Data
- TradingView Integration
- Price Alerts

---

# Request Flow

Example:

```text
Mobile App
      ↓
API Request
      ↓
Auth Middleware
      ↓
Handler
      ↓
Service
      ↓
Repository
      ↓
PostgreSQL
      ↓
Response
      ↓
Mobile App
```

---

# Security

TradeMate will implement:

- bcrypt Password Hashing
- JWT Authentication
- Protected Routes
- Environment Variables
- Input Validation

Sensitive data will never be stored inside the repository.

---

# Future Enhancements

- TradingView Webhooks
- Push Notifications
- Backtesting Engine
- Market Data Integration
- AI Trade Insights
- Web Dashboard

---

# Architecture Summary

TradeMate is a full-stack trading journal and risk management platform built using:

- React Native + Expo
- Go + Gin
- PostgreSQL
- JWT Authentication

The project follows a Modular Monolith Architecture with a Layered Backend Design to maintain scalability, maintainability, and clean code organization.