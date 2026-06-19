# CommBank Server

A modern ASP.NET Core API server for managing banking operations, built with C# and MongoDB.

## Overview

CommBank Server is a RESTful API backend that provides comprehensive banking functionality including user authentication, account management, transaction tracking, and financial goals management. The application leverages MongoDB for data persistence and follows clean architecture principles with service-based patterns.

##  Features

- **User Authentication**: Secure login with BCrypt password hashing
- **Account Management**: Create, read, update, and delete bank accounts
- **Transaction Tracking**: Monitor and manage financial transactions
- **Goals Management**: Set and track financial goals with user-specific queries
- **Tag System**: Categorize and organize financial data
- **MongoDB Integration**: Scalable NoSQL database backend



### Core Components

#### Models

- **User**: Represents a bank customer with login credentials, linked goals and accounts
- **Account**: Bank account with account number, balance, type, and linked transactions
- **Transaction**: Financial transaction with user and account references
- **Goal**: Financial goals associated with users for tracking savings targets
- **Tag**: Categorization system for organizing financial data

#### Services

All services follow a consistent CRUD pattern and interact with MongoDB collections:

- **AuthService**: Handles user authentication with secure password verification
- **UsersService**: Full CRUD operations for user management
- **AccountsService**: Account lifecycle management
- **TransactionsService**: Transaction handling including user-specific queries
- **GoalsService**: Goal management with user filtering

#### Controllers

RESTful API endpoints structured as:

- `/api/user` - User management endpoints
- `/api/account` - Account management endpoints
- `/api/goal` - Goal management endpoints
- `/api/transaction` - Transaction management endpoints

##  Key Technologies

- **Framework**: ASP.NET Core
- **Language**: C# (.NET)
- **Database**: MongoDB
- **Security**: BCrypt for password hashing
- **ORM**: MongoDB C# Driver
- **Architecture**: Service Layer Pattern, Dependency Injection

##  Database Schema

### Collections

All models use MongoDB BSON ObjectId for unique identification:

- **Users**: User accounts with encrypted passwords and linked goals
- **Accounts**: Bank accounts with transaction tracking
- **Transactions**: Financial records linked to users and accounts
- **Goals**: Financial targets linked to users
- **Tags**: Categorization tags for financial data

##  Security Features

- **Password Hashing**: BCrypt.Net for secure password storage
- **Input Validation**: BSON ObjectId validation for MongoDB queries
- **SQL Injection Prevention**: Parameterized MongoDB queries throughout
- **Async Operations**: All database operations are asynchronous

##  Development Setup

### Prerequisites

- .NET SDK
- MongoDB instance
- Visual Studio or VS Code


