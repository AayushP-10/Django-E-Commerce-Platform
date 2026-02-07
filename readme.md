# Django E-Commerce Platform

## Overview

This project is a fully functional E-Commerce website built with Django, with a primary focus on understanding backend development using the Django framework. A free frontend template from MDBootstrap was used as the base UI, while all core e-commerce features were implemented on top of it.

The backend uses a mix of generic class-based views and function-based views to demonstrate different Django design approaches. The application relies on Django’s default SQLite database and integrates Stripe for handling online payments.

This README outlines the major features of the application and provides step-by-step instructions to run the project locally.

---

## Key Features

- User authentication and account management using django-allauth
- Product browsing with category-based filtering and search
- Shopping cart functionality with add and remove actions
- Like functionality for products
- Coupon support to apply discounts at checkout
- Dynamic and user-friendly checkout process
- Secure payment processing using Stripe API
- Order history tracking
- Refund request functionality
- Customized Django admin dashboard for management

---

## Project Structure

The directory structure of the Django application is organized as follows:

    E-commerce-Website-Django/
        |-- core/
        |-- djangoecommerce/
        |-- static/
        |-- static_in_env/
        |-- templates/
        |-- .env
        |-- manage.py
        |-- .gitignore
        |-- requirements.txt
        |-- readme.md

---

## Prerequisites

- Python version 3.6 or higher  
- Recommended version used during development: Python 3.8  

It is strongly recommended to use a virtual environment to isolate dependencies.

---

## Setup and Usage

### Virtual Environment Setup

Install virtualenv if it is not already installed:

    pip install virtualenv

Verify the project directory contents:

    ls

You should see directories such as:

    core/  djangoecommerce/  static/  static_in_env/  templates/
    manage.py  requirements.txt  readme.md

Create a virtual environment:

    virtualenv venv_name

Activate the virtual environment:

On Windows (Git Bash):

    source venv_name/Scripts/activate

On Linux or macOS:

    source venv_name/bin/activate

Install project dependencies:

    pip install -r requirements.txt

---

## Getting Started

Apply database migrations and create a superuser account:

    python manage.py migrate
    python manage.py createsuperuser --username <username> --email <email>

Start the development server:

    python manage.py runserver

---

## Static Files

Static files are preconfigured in the Django settings. If styles do not load correctly, run:

    python manage.py collectstatic

Access the application in the browser:

    http://localhost:8000/

Initially, no products will be visible. Products must be added through the Django admin panel.

Admin dashboard:

    http://localhost:8000/admin/

---

## Models Used

The application uses the following models:

- UserProfile
- Item
- Category
- OrderItem
- Cart
- Address
- Payment
- Coupon
- Refund
- Comment

Add items to the Item model through the admin panel to begin using the storefront. The homepage supports pagination and displays 8 products per page, so adding more than 8 items will demonstrate pagination behavior.

---

## Stripe Payment Integration

Stripe is used to process payments securely. For testing purposes, Stripe provides test card credentials.

Use the following test card details during checkout:

- Card Number: 4242 4242 4242 4242
- Expiry Date: Any future date (e.g., 12/30)
- CVV: Any valid value

---