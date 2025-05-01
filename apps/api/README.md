# LLaMAlert API

FastAPI backend for the LLaMAlert behavioral anomaly detection demo.

## Features
- Anomaly detection inference endpoint
- LLaMA-2-7B integration
- PostgreSQL data storage
- CRUD API for synthetic data management

## Development
```bash
# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run development server
uvicorn main:app --reload
```