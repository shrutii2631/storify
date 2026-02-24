# Inventory & Billing Management System (Django)

Backend-focused Django project for managing products, customers, billing, and stock.

## Features
- Product CRUD (add, update, delete)
- Customer management
- Billing system with GST & discount
- Automatic stock deduction during billing
- Invoice PDF generation
- Low stock alerts
- Sales analytics dashboard
- CSV export of sales

## Tech Stack
- Python
- Django
- SQLite
- ReportLab
- HTML/CSS

## Database Design
- Product
- Customer
- Bill
- BillItem (stores price_at_sale to preserve billing history)

## Key Logic
- Billing handled in Django views
- Subtotal, GST and total calculated during bill creation
- Stock reduced automatically after successful billing
- Prevents billing when stock is insufficient

## Setup (Local)
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
