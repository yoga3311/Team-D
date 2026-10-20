# ClearDQ v3 - Data Quality Management (SQL Server / SSMS)
## 1. Database (SQL Server)
Install SQL Server (Express is fine) + "ODBC Driver 17 (or 18) for SQL Server" + SSMS.
cd backend && copy .env.example .env  -> edit DB_SERVER (see the server name shown in SSMS login), DB_DRIVER, and DB_USER/DB_PASSWORD if not using Windows auth.
The database "ClearDQ", all tables, the admin user and 6 benchmark domains are created automatically on first start. Browse them in SSMS.
## 2. Backend
python -m venv venv && venv\Scripts\activate && pip install -r requirements.txt && uvicorn app.main:app --reload --port 8000
## 3. Frontend
cd frontend && npm install && npm run dev -> http://localhost:5173
## Login
One login page: your role (admin/analyst) is detected from your email. Default admin: admin@dqm.com / Admin@123
Samples to test with: samples/pharma_sample.xlsx (domain Pharma), samples/banking_sample.xlsx (Banking & Finance)
