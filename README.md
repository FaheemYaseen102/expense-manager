# 💸 Expense Manager App

A full-stack expense manager application built with **React** and **Node.js**. The app helps users efficiently track their expenses, set budgets, and receive email notifications when their budget exceeds, or when they’re nearing their budget limit. The app also logs user activity and sends emails using **Nodemailer**, with **JWT** authentication to secure user data.

## 🛠 Technologies

- **Frontend**: React.js, Ant Design, React Icons
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Token)
- **Email Service**: Nodemailer
- **External API**: For finance and self-help news
- **Logging**: Activity logs stored in MongoDB

## 📌 Features

### User Management
- **CRUD Operations for Users**: Create, Read, Update, and Delete user profiles.
- **JWT Authentication**: Secure login and registration.
- **Email Notifications**: 
  - Emails sent when:
    - A new user is created.
    - A user is deleted.
    - Budget exceeds expenses.
    - Expenses near 90% of the budget.
- **User Activity Logging**: Logs user-related actions, including email events.

### Expense Management
- **CRUD Operations for Expenses**: Add, Edit, and Delete expenses with descriptions, amounts, and categories.
- **Categories Collection**: Predefined categories for expenses (e.g., Food, Transport, Utilities).

### Budget Management
- **CRUD Operations for Budgets**: Set and modify budgets for various categories.
- **Budget Exceed Alerts**: Email notifications if the total expenses exceed the set budget.
- **Budget Monitoring**: Email notifications when expenses approach 90% of the set budget.

### Finance and Self-Help News
- Fetch finance and self-help related news from an external API to keep users informed.

## 📬 Email Notifications

- **New User Registration**: Upon successful registration, the user receives a welcome email.
- **User Deletion**: Notifies admins when a user is deleted.
- **Budget Exceeded**: Sends an alert if the user's expenses exceed their set budget.
- **Near Budget Alert**: Sends a warning email when expenses near 90% of the user’s set budget.

## 🔧 Installation

1. Clone the repository:


2. Install backend dependencies:

   ```bash
   cd backend
   npm install
   ```

3. Install frontend dependencies:

   ```bash
   cd frontend
   npm install
   ```

4. Configure environment variables:

   * In the **backend** directory, create a `.env` file and add the following variables:

     * `MONGODB_URI` – Your MongoDB connection string
     * `JWT_SECRET` – Your JWT secret for encoding tokens
     * `JWT_EXPIRATION` – 30d
     * `EMAIL_USER` – Your email username for Nodemailer
     * `EMAIL_PASS` – Your email App password for Nodemailer
     * `PORT` – 8000
  

5. Run the application:

   * Start the backend server:

     ```bash
     npm run dev
     ```

   * Start the frontend:

     ```bash
     npm run dev
     ```

6. Open your browser and go to `http://localhost:3000`.

## 📝 API Endpoints

### Expense Endpoints

* **GET /expenses**: 
* **POST /expenses**: Add a new expense.
* **PUT /expenses/\:expenseId**: Update an existing expense.
* **DELETE /expenses/\:expenseId**: Delete an expense.

### Budget Endpoints

* **GET /budget**: Retrieve the current budget for the logged-in user.
* **POST /budget**: Set a new budget for a category.
* **DELETE /budget/\:budgetId**: Delete a budget.

### User Endpoints


* **GET /users/status**: Get auth status of user
* **POST /login**: Login the user. 
* **POST /**: Create User or Signup
* **PUT /**: Update User 
* **DELETE /users/\:id**: Delete a user 

