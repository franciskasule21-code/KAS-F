# KAS-F Backend - Django API

REST API for Pay Management System built with Django and Django REST Framework.

## Setup Instructions

### 1. Install Dependencies
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\\Scripts\\activate
pip install -r requirements.txt
```

### 2. Configure Database
Create `.env` file:
```
DEBUG=True
SECRET_KEY=your-secret-key-here
DATABASE_URL=postgresql://postgres:postgres@localhost:5432/kas_f_db
DB_USER=postgres
DB_PASSWORD=postgres
DB_HOST=localhost
DB_PORT=5432
```

### 3. Run Migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

### 4. Create Superuser
```bash
python manage.py createsuperuser
```

### 5. Run Development Server
```bash
python manage.py runserver
```

API will be available at `http://localhost:8000/api/`

## API Endpoints

### Employees
- `GET /api/employees/` - List all employees
- `POST /api/employees/` - Create employee
- `GET /api/employees/{id}/` - Get employee details
- `PUT /api/employees/{id}/` - Update employee
- `DELETE /api/employees/{id}/` - Delete employee
- `GET /api/employees/{id}/payroll_history/` - Get payroll history
- `GET /api/employees/{id}/attendance_summary/` - Get attendance summary

### Attendance
- `GET /api/attendance/` - List attendance records
- `POST /api/attendance/` - Create attendance
- `POST /api/attendance/bulk_create/` - Bulk create attendance

### Payroll
- `GET /api/payroll/` - List payroll records
- `POST /api/payroll/calculate_payroll/` - Calculate payroll
- `POST /api/payroll/{id}/approve/` - Approve payroll
- `GET /api/payroll/{id}/audit_log/` - Get audit log

### Tax Rules
- `GET /api/tax-rules/` - List tax rules
- `GET /api/tax-rules/current_year/` - Get current year rules

### Payments
- `GET /api/payments/` - List payments
- `POST /api/payments/process_payments/` - Process payments
- `POST /api/payments/{id}/mark_completed/` - Mark payment completed

## Docker Setup
```bash
docker-compose up
```
