# ERP Client Management System

A comprehensive full-stack Enterprise Resource Planning (ERP) system for managing clients, orders, invoices, payments, and support tickets with real-time analytics dashboard.

## Features

### 📊 Dashboard
- **Real-time Analytics** - Key metrics for revenue, clients, orders, and invoices
- **Revenue Trends** - 12-month revenue visualization with charts
- **Payment Distribution** - Breakdown by payment methods (Cash, Card, Transfer, Check)
- **Top Clients** - Ranking of best customers by revenue
- **Alert System** - Notifications for overdue invoices, pending tasks, and open tickets
- **Monthly Comparison** - Current vs previous month performance tracking

### 👥 Client Management
- Complete CRUD operations for client profiles
- Client status tracking (Active, Inactive, Suspended)
- Account balance management
- Modification history with audit trail
- Advanced search and filtering

### 📦 Order Management
- Order creation and tracking
- Multiple order statuses: Pending, Validated, In Progress, Delivered, Cancelled
- Product line items with quantities and pricing
- Order validation workflow
- Cancellation with reason tracking

### 📄 Invoice Management
- Automatic invoice generation from orders
- Payment status tracking (Unpaid, Partially Paid, Paid)
- Multiple payment methods support
- Outstanding balance calculation
- Invoice history and reporting

### 💳 Payment Management
- Payment recording with multiple methods
- Payment reference tracking
- Invoice payment allocation
- Payment history and receipts
- Account balance payments

### 🎫 Support Ticket System
- Ticket creation and management
- Status workflow: Open, In Progress, Resolved, Closed, Archived
- Client association and agent assignment
- Comment system (Internal/External)
- Ticket history and activity log
- File attachments support

### 📅 Deadline Management (Échéances)
- Automated email reminders
- Account suspension scheduling
- Pending task tracking
- Execution status monitoring

## 🛠 Tech Stack

### Backend
- **Runtime:** Node.js 16.x+
- **Framework:** Express.js
- **Database:** MongoDB 6.x with Mongoose ODM
- **Authentication:** JWT (ready for implementation)
- **Validation:** Express Validator
- **Scheduler:** Node-cron for automated tasks

### Frontend
- **Framework:** Angular 17.x (Standalone Components)
- **UI Components:** Custom components with TypeScript
- **Charts:** Chart.js / ng2-charts
- **HTTP Client:** Angular HttpClient with RxJS
- **Routing:** Angular Router
- **Styling:** SCSS with responsive design

### Development Tools
- **Version Control:** Git
- **Package Manager:** npm
- **Code Editor:** VS Code (recommended)
- **API Testing:** Postman / Thunder Client

## 🏗 System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     Angular Frontend                        │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐     │
│  │Dashboard │  │ Clients  │  │  Orders  │  │ Invoices │     │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘     │
│  ┌──────────┐  ┌──────────┐                                 │
│  │ Payments │  │ Tickets  │                                 │
│  └──────────┘  └──────────┘                                 │
└─────────────────────────────────────────────────────────────┘
                           │
                           ▼ HTTP/REST API
┌─────────────────────────────────────────────────────────────┐
│                    Express.js Backend                       │
│  ┌──────────────────────────────────────────────────────┐   │
│  │              RESTful API Routes                      │   │
│  │  /api/dashboard  /api/clients  /api/commandes        │   │
│  │  /api/factures   /api/paiements  /api/tickets        │   │
│  └──────────────────────────────────────────────────────┘   │
│  ┌──────────────────────────────────────────────────────┐   │
│  │           Business Logic Layer                       │   │
│  │  Models | Validation | Aggregation | Scheduling      │   │
│  └──────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                           │
                           ▼ Mongoose ODM
┌─────────────────────────────────────────────────────────────┐
│                    MongoDB Database                         │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐            │
│  │ clients │ │commandes│ │ factures│ │paiements│            │
│  └─────────┘ └─────────┘ └─────────┘ └─────────┘            │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐                        │
│  │ tickets │ │écheances│ │ counter │                        │
│  └─────────┘ └─────────┘ └─────────┘                        │
└─────────────────────────────────────────────────────────────┘
```

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js:** v16.x or higher ([Download](https://nodejs.org/))
- **npm:** v8.x or higher (comes with Node.js)
- **MongoDB:** v6.x or higher ([Download](https://www.mongodb.com/try/download/community))
  - Or use MongoDB Atlas (cloud database)
- **Git:** Latest version ([Download](https://git-scm.com/))
- **Angular CLI:** v17.x or higher

