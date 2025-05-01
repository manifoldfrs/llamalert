# LLaMAlert: AI-Driven Behavioral Anomaly Detection Prototype

## Project Description

A concise demo showcasing behavioral anomaly detection for fraud prevention, utilizing LLaMA-2-7B from Hugging Face. The demo features a React frontend with interactive, real-time visualizations using confidence bars, and a Python backend integrated with a PostgreSQL database, all deployed via Vercel's free tier.

## Features

### Frontend
- Interactive dashboard with minimalist design
- User input forms for typing biometrics and location simulation
- Real-time anomaly detection visualization with confidence bars
- Professional UI with clear visual indicators for legitimate vs. anomalous behavior

### Backend
- FastAPI REST API for real-time inference
- Integration with LLaMA-2-7B for anomaly detection
- PostgreSQL database for storing behavioral data and inference logs
- Lightweight deployment on Vercel's free tier

### AI Detection
- Prompt-engineering for detecting anomalies in typing patterns and login locations
- Optimized for <2 second inference latency per request
- Comprehensive synthetic data generation for testing

## Getting Started

### Prerequisites
- Node.js >= 18
- PNPM >= 8
- Python >= 3.9
- Docker (for local PostgreSQL)

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/llamalert.git
cd llamalert
```

2. Install JavaScript dependencies
```bash
pnpm install
```

3. Set up the backend environment
```bash
cd apps/api
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
pip install -r requirements-dev.txt  # For development dependencies
```

4. Set up the local database
```bash
cd ../../infra
docker compose up -d
```

5. Run migrations
```bash
cd ../apps/api
alembic upgrade head
```

6. Start the development servers
```bash
cd ../..
pnpm dev
```

## Development

### Linting and Formatting

For TypeScript/JavaScript:
```bash
# Run ESLint
pnpm lint

# Fix ESLint issues
pnpm lint:fix

# Format code with Prettier
pnpm format
```

For Python:
```bash
# Run Ruff linter
pnpm lint:py

# Format code with Black and isort
pnpm format:py
```

## Project Structure
```
llamalert/
├── apps/
│   ├── frontend/  # React TypeScript SPA
│   └── api/       # FastAPI backend
├── packages/
│   └── ui/        # Shared UI components
└── infra/         # Infrastructure configuration
```

## License
MIT
