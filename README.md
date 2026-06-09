# KAS-F: Pay Management System

A comprehensive pay management system for processing employee payroll, calculating taxes, and managing payments.

## Features
- Employee Management
- Attendance Tracking
- Payroll Processing
- Tax Calculation
- Payment Distribution
- Compliance Reporting
- Real-time Dashboard

## Technology Stack
- Backend: Django + Django REST Framework
- Database: PostgreSQL
- Frontend: React + Material-UI
- Authentication: JWT
- Containerization: Docker & Docker Compose

## Quick Start

### Option 1: Docker (Recommended)
```bash
docker-compose up
```

Access:
- Frontend: http://localhost:3000
- Backend API: http://localhost:8000/api
- Admin Panel: http://localhost:8000/admin

### Option 2: Local Setup

**Backend:**
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

**Frontend:**
```bash
cd frontend
npm install
npm start
```

## Project Structure
```
KAS-F/
├── backend/              # Django REST API
│   ├── config/          # Django settings
│   ├── payroll/         # Main app
│   ├── manage.py
│   └── requirements.txt
├── frontend/            # React dashboard
│   ├── src/
│   ├── package.json
│   └── public/
├── docker-compose.yml
└── README.md
```

## API Documentation

See `backend/README.md` for complete API endpoints.

## Database Schema

Key tables:
- **employees**: Employee information
- **attendance**: Daily attendance records
- **payroll**: Monthly payroll records
- **payments**: Payment transactions
- **tax_rules**: Tax configuration
- **payslip_audit**: Audit trail

## Default Credentials (For Development)

After migrations, create a superuser:
```bash
python manage.py createsuperuser
```

## License

MIT License - See LICENSE file

## Support

For issues and questions, please create a GitHub issue.
