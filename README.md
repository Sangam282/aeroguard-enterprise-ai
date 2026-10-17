# aeroguard-ai-enterprise-2.8
  AI Builder Cup 2026 (Google)


### Phase 1 — Backend Setup, Database UUID Migration & Automated Test Suite
```bash
cd aeroguard-ai-enterprise/backend

# Run the standalone end-to-end verification suite (zero external dependencies required)
python3 core/test_suite.py
# Create a virtual environment named 'venv'
python3 -m venv venv

# Activate the virtual environment
source venv/bin/activate
# Optional: Full Django REST Framework server startup
pip install -r requirements.txt
python3 manage.py makemigrations core
python3 manage.py migrate
python3 manage.py runserver 0.0.0.0:8000

### Phase 2 — Angular Frontend Setup & Local Development Server
```bash
cd ../frontend
npm install
npm start
# Opens http://localhost:4200 connected to http://localhost:8000/api/v1
