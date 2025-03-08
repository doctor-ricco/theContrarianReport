# The Contrarian Report

A web platform built with Django that connects clients and writers, managing contract work with an integrated PayPal subscription payment system.

## 📋 Overview

The Contrarian Report is an innovative platform created to facilitate connections between clients who need written content and professional writers. The system offers complete user management, project requests, contract administration, and payment processing through PayPal subscriptions.

## 🚀 Features

- Role-based authentication system (clients and writers)
- Comprehensive project management
- Contract generation and administration
- PayPal integration for subscription processing
- Responsive design using Bootstrap 5

## 🔧 Technology Stack

- **Framework**: Django
- **Database**: SQLite
- **Frontend**: HTML, CSS, Bootstrap 5
- **Payment Processing**: PayPal API
- **Dependencies**: Listed in `requirements.txt`

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- Git

### Setup Instructions

1. Clone the repository to your local machine

    ```
    git clone https://github.com/doctor-ricco/theContrarianReport
    cd Contra
    ```

2. Create and activate a virtual environment

    For Windows:
    
    ```
    python -m venv .venv
    .venv\Scripts\activate
    ```
    
    For macOS/Linux:
    
    ```
    python -m venv .venv
    source .venv/bin/activate
    ```

3. Install the required dependencies

    ```
    pip install -r requirements.txt
    ```

4. Create a `.env` file in the project root with your PayPal API credentials (for payment functionality)

    ```
    PAYPAL_CLIENT_ID=your_client_id
    PAYPAL_SECRET_ID=your_secret_id
    PAYPAL_AUTH_URL=https://api.sandbox.paypal.com/v1/oauth2/token
    PAYPAL_BILLING_SUBSCRIPTIONS_URL=https://api.sandbox.paypal.com/v1/billing/subscriptions
    ```

## 🏃‍♂️ Running the Application

1. Navigate to the `src` directory

    ```
    cd src
    ```

2. Run database migrations

    ```
    python manage.py migrate
    ```

3. Create a superuser (admin account)

    ```
    python manage.py createsuperuser
    ```

4. Start the development server

    ```
    python manage.py runserver
    ```

5. Open your browser and go to http://127.0.0.1:8000/

## 📱 Project Structure

- `account/`: User authentication and management
- `client/`: Client-specific functionality
- `writer/`: Writer-specific functionality
- `common/`: Shared templates and utilities
- `contrarian/`: Main project settings
- `static/`: Static files (CSS, JS, images)

## 🔑 User Roles

- **Clients**: Can create projects, manage contracts, and make payments
- **Writers**: Can view available projects, submit proposals, and manage their contracts
- **Administrator**: Can manage all aspects of the system through the Django admin interface

## 💡 Development Notes

- The application uses SQLite for data storage
- PayPal integration is configured using sandbox for testing
- The project uses Bootstrap 5 for UI components

## 🛡️ Security Notes

- For production deployment, make sure to:
  - Change the `SECRET_KEY` in settings
  - Set `DEBUG = False`
  - Configure proper database credentials
  - Set up HTTPS with a valid SSL certificate

## 📄 License

See the LICENSE file for details.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request 