# Expense Approval Management System

A backend platform built with Java and Spring Boot to manage employee expenses, automate approval workflows, and identify potentially fraudulent expense claims using AI.

## Overview

The Expense Approval Management System allows employees to submit expenses, managers to review and approve or reject claims, and administrators to manage users and system access. AI-assisted analysis helps categorize expenses and flag suspicious claims for further review.

## Core Features

- **Expense Management** — Create, view, and track expense claims.
- **Approval Workflow** — Approve or reject pending expenses with a recorded rejection reason.
- **Role-Based Access Control** — Support EMPLOYEE, MANAGER, and ADMIN roles.
- **AI Expense Categorization** — Categorize expenses as TRAVEL, FOOD, SOFTWARE, EQUIPMENT, or OTHER.
- **AI Fraud-Risk Analysis** — Flag potential duplicate claims, unusual amounts, policy violations, and suspicious descriptions.
- **Auditability** — Track submitters, reviewers, and timestamps.
- **Input Validation and Exception Handling** — Return consistent API errors.
- **Reporting and Pagination** — Support efficient expense listing and review.

## Domain Model

### AppUser
- id
- email
- password hash
- fullName
- role

### Expense
- id
- title
- description
- amount
- expenseDate
- status
- category
- submittedBy
- reviewedBy
- rejectionReason
- aiFraudFlags
- aiProcessedAt
- createdAt

## Technology Stack

- Java
- Spring Boot
- Spring Data JPA / Hibernate
- Spring Security
- PostgreSQL
- Maven
- REST APIs
- Bean Validation
- Git and GitHub

Planned extensions:
- AI integration for expense classification and risk analysis
- Docker and containerized deployment
- Automated testing and API documentation
- Microservices architecture, if justified by the project requirements

## Initial Approval Workflow

1. An employee submits an expense.
2. The system validates the request and records it as `PENDING`.
3. AI analyzes the expense and returns a suggested category and potential risk flags.
4. A manager reviews the claim and supporting information.
5. The manager approves or rejects the expense.
6. The system records the reviewer, decision, timestamps, and rejection reason when applicable.

AI risk flags are advisory signals; they do not automatically establish fraud.

## Development Status

🚧 Under development.

## Goals

Build a production-oriented backend that demonstrates secure API design, relational data modeling, approval workflows, AI integration, automated testing, and maintainable software architecture.
