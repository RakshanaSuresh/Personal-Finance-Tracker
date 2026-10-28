# Personal Finance Tracker

A full-stack web application for managing personal finances, tracking income and expenses, organizing categories, setting monthly budgets, and understanding spending habits through reports and visualizations.

## Overview

The Personal Finance Tracker helps users record and manage their financial activities in one place. It provides a dashboard for monitoring financial performance, transaction management tools, category-based budgets, and reports for analyzing income and expenses.

This project was developed as a practical full-stack application using React, TypeScript, Node.js, Express, and PostgreSQL.

## Features

### 1. Dashboard
- View financial summary cards.
- Monitor income, expenses, and net savings.
- Visualize income and expense trends.
- View expense category breakdowns.
- Monitor budget alerts.
- View the five most recent transactions.

### 2. Transaction Management
- Create, view, update, and delete transactions.
- Record income and expenses.
- Assign categories, dates, descriptions, and payment methods.
- Search and filter transactions.
- Sort transactions by date and amount.
- Export transaction records to CSV.

### 3. Budget Management
- Set monthly budgets for expense categories.
- View budget amounts and spending progress.
- Track remaining budget amounts.
- Identify budget warnings and exceeded budgets.
- Create, update, and delete budgets.

### 4. Financial Reports
- View monthly financial summaries.
- Analyze income and expense trends.
- Review expense breakdowns by category.
- Monitor daily income and spending.
- Compare financial activity across reporting periods.

### 5. Category Management
- Create income and expense categories.
- Edit category names, colors, and icons.
- Delete categories when permitted.
- View category transaction counts.

## Technology Stack

| Technology | Purpose |
|---|---|
| React | User interface |
| TypeScript | Type-safe application development |
| Vite | Frontend development server and build tool |
| Tailwind CSS | Styling and responsive layouts |
| Node.js | Backend runtime |
| Express.js | REST API development |
| PostgreSQL | Relational database |
| `pg` | PostgreSQL connectivity from Node.js |
| Git and GitHub | Version control and source code management |

## Project Structure

```text
personal-finance-tracker/
├── client/
│   └── src/
│       ├── api/
│       ├── pages/
│       │   ├── TransactionsPage.tsx
│       │   ├── BudgetsPage.tsx
│       │   ├── ReportsPage.tsx
│       │   └── CategoriesPage.tsx
│       ├── types/
│       └── App.tsx
├── server/
│   └── src/
│       └── ...
├── README.md
└── .gitignore
```

*Note: Adjust the backend folder structure to match your actual repository.*

## Getting Started

### Prerequisites

Install the following software before running the application:

- [Node.js](https://nodejs.org/)
- npm (included with Node.js)
- [PostgreSQL](https://www.postgresql.org/download/)
- [Git](https://git-scm.com/downloads)
- A code editor such as Visual Studio Code

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd personal-finance-tracker
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### 2. Set up the database

1. Start PostgreSQL.
2. Create a database named `finance_tracker`, if it does not already exist.
3. Configure the backend connection using your local PostgreSQL credentials.
4. Apply the project's existing database schema and migrations or setup scripts.

**Important:** Do not recreate an existing database containing your saved transactions, categories, or budgets. Follow the database setup instructions in your project.

### 3. Configure environment variables

Create the required environment file using the variable names expected by your backend configuration.

For example, if your server uses these names, the configuration could look like:

```env
PORT=5000
DATABASE_URL=postgresql://USERNAME:PASSWORD@localhost:5432/finance_tracker
```

Replace the example credentials with your local configuration. Do not commit passwords, API keys, or other secrets to GitHub.

If your backend uses separate PostgreSQL variables such as `DB_HOST`, `DB_USER`, and `DB_PASSWORD`, use those names instead.

### 4. Install backend dependencies

Open a terminal in VS Code:

```bash
cd server
npm install
```

Start the backend using the development script defined in `server/package.json`. For example, if the project defines a `dev` script:

```bash
npm run dev
```

Keep the backend terminal running.

### 5. Install frontend dependencies

Open a second terminal:

```bash
cd client
npm install
```

Start the Vite development server:

```bash
npm run dev
```

Open the local URL displayed in the terminal, commonly:

```text
http://localhost:5173
```

Ensure the frontend API configuration points to the correct backend URL.

## API Overview

The backend provides REST API endpoints for the following operations.

| Resource | Example endpoints | Purpose |
|---|---|---|
| Transactions | `/api/transactions` | Manage transaction records |
| Categories | `/api/categories` | Manage income and expense categories |
| Budgets | `/api/budgets` | Manage monthly category budgets |
| Reports | `/api/reports/summary` | Retrieve financial summaries |
| Reports | `/api/reports/trends` | Retrieve monthly trends |
| Reports | `/api/reports/category-breakdown` | Retrieve category spending data |
| Reports | `/api/reports/daily-spending` | Retrieve daily financial activity |

*Verify the actual route prefixes and HTTP methods in your backend before publishing this section.*

## Testing

Recommended manual tests include:

- Create, update, and delete a test transaction.
- Verify transaction search, filtering, sorting, and CSV export.
- Create and update category budgets.
- Check monthly reports against transaction records.
- Add and edit categories.
- Refresh the application and verify saved data persists.
- Check browser developer tools and backend logs for unexpected errors.

Use test records where possible and preserve real financial data.

## Security and Data Handling

- Store database credentials in environment variables.
- Keep `.env` files out of version control.
- Validate user input on the backend.
- Use parameterized SQL queries.
- Restrict access to data according to the application's authentication and authorization design.
- Back up important database records before making schema changes.

## Future Improvements

Potential enhancements include:

- User authentication and secure account management.
- Multi-user financial data isolation.
- Deployment to a production hosting environment.
- Automated backend and frontend tests.
- Improved accessibility and mobile responsiveness.
- Additional financial insights and spending analytics.

## Learning Outcomes

This project provides practical experience with:

- Building a full-stack TypeScript application.
- Developing REST APIs with Express.
- Connecting an application to PostgreSQL.
- Implementing CRUD operations.
- Managing frontend state and API integration.
- Creating financial reports and visualizations.
- Using Git and GitHub for version control.

## Author

**Your Name**

IT Undergraduate — University of Moratuwa

GitHub: [Your GitHub Profile](https://github.com/YOUR_GITHUB_USERNAME)

---

*This project is developed for learning and portfolio purposes.*
