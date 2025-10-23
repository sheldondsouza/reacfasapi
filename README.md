# Reacfasapi

A starter full‑stack template combining a React frontend with a FastAPI backend. This repository provides a simple, opinionated structure to build modern web applications with a TypeScript/React frontend and a Python/FastAPI backend.

## Features

- React frontend (JavaScript or TypeScript)
- FastAPI backend with automatic OpenAPI (Swagger) docs
- Example CORS setup and environment-based configuration
- Development and production run instructions
- Optional Docker configuration (if Dockerfiles / compose are added)

## Tech stack

- Frontend: React (Create React App or Vite), npm/yarn, optionally TypeScript
- Backend: Python 3.10+, FastAPI, Uvicorn
- Optional: Docker & Docker Compose for containerized development

## Prerequisites

- Python 3.10 or newer
- Node.js 16+ and npm or yarn
- (Optional) Docker and Docker Compose

## Quick start

### Backend (FastAPI)

1. Create and activate a virtual environment

   macOS / Linux
   ```
   python -m venv .venv
   source .venv/bin/activate
   ```

   Windows (PowerShell)
   ```
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

2. Install dependencies
   ```
   pip install -r backend/requirements.txt
   ```

3. Set environment variables (example)
   ```
   export DATABASE_URL="sqlite:///./dev.db"
   export SECRET_KEY="your-secret-key"
   export DEBUG=True
   ```

4. Run the development server
   ```
   uvicorn backend.main:app --reload --host 0.0.0.0 --port 8000
   ```

5. Open the interactive API docs at:
   - Swagger UI: http://localhost:8000/docs
   - ReDoc: http://localhost:8000/redoc

### Frontend (React)

1. Change into the frontend directory
   ```
   cd frontend
   ```

2. Install dependencies
   ```
   npm install
   # or
   yarn
   ```

3. Start the development server
   ```
   npm start
   # or
   yarn start
   ```

4. Open the app at http://localhost:3000 (default)

## Environment variables

Create a `.env` file in backend and/or frontend directories with values similar to:

```
# backend/.env
DATABASE_URL=sqlite:///./dev.db
SECRET_KEY=super-secret
DEBUG=True

# frontend/.env
REACT_APP_API_URL=http://localhost:8000
```

Adjust secrets and DB URLs for production.

## Running with Docker (optional)

If Dockerfile(s) and docker-compose.yml are present:

```
docker-compose up --build
```

This builds and runs frontend and backend services in containers.

## Tests

- Backend: from the backend directory run `pytest`
- Frontend: from the frontend directory run `npm test` or `yarn test`

Add/extend tests as features are implemented.

## Suggested project structure

- backend/ — FastAPI application (Python)
- frontend/ — React application (JS/TS)
- .github/ — CI workflows
- README.md — this file
- docker-compose.yml, Dockerfile(s) — optional container configs

## Contributing

Contributions are welcome. Please open an issue to discuss major changes, and submit pull requests for bug fixes and features. Follow these guidelines:

- Open an issue describing your planned change if it’s nontrivial
- Create a branch per feature/fix
- Add or update tests where appropriate
- Keep commits small and focused

## License

Add a LICENSE file (for example MIT) and update this section accordingly.

## Maintainer / Contact

Maintainer: sheldondsouza
