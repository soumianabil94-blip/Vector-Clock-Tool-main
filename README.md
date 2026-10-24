# Vector Clock Visualiser

An interactive educational tool for understanding **vector clocks and causal ordering in distributed systems**.

## Overview

In distributed systems, multiple processes execute independently and communicate by exchanging messages. Because there is no single global clock, determining the order of events across processes can be challenging.

This project provides an interactive visualisation of vector clocks, helping users understand how distributed events are ordered and how processes track causal relationships between events.

The application combines a React-based frontend with a Flask backend to provide interactive diagrams, explanations and learning activities.

## Features

- **Interactive visualisation:** Explore events across multiple processes and observe how vector clocks change.
- **Causal ordering:** Understand the relationship between events, including happened-before relationships and concurrent events.
- **Step-by-step explanations:** Follow clock updates as processes execute events and exchange messages.
- **AI-assisted learning:** Access an AI-powered panel for additional explanations and help understanding distributed systems concepts.
- **Quizzes and practice:** Reinforce understanding through interactive learning activities.

## Tech Stack

| Component | Technologies |
|---|---|
| Frontend | React, Vite, JavaScript |
| Visualisation | D3.js |
| Backend | Python, Flask |
| AI integration | Gemini API |
| Testing | Vitest, React Testing Library, pytest |

## Project Structure

```text
Vector-Clock-Tool/
├── backend/
│   ├── app.py
│   ├── routes/
│   ├── services/
│   ├── tests/
│   └── requirements.txt
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.js
└── README.md
```

## Getting Started

### Prerequisites

Install the following before running the application:

- Python 3
- Node.js and npm
- Git

### 1. Clone the repository

```bash
git clone https://github.com/soumianabil94-blip/Vector-Clock-Tool-main.git
cd Vector-Clock-Tool
```


### 2. Set up the backend

Navigate to the backend directory:

```bash
cd backend
```

Create and activate a Python virtual environment.

**Windows (PowerShell):**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS/Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

If AI functionality requires a Gemini API key, configure it using an environment variable as specified by the application. Never commit API keys or other secrets to GitHub.

Start the Flask server:

```bash
python app.py
```

The backend should be available at:

[http://127.0.0.1:5000](http://127.0.0.1:5000)

Keep this terminal running.

### 3. Set up the frontend

Open a second terminal and navigate to the frontend directory:

```bash
cd frontend
```

Install the dependencies:

```bash
npm install
```

Start the Vite development server:

```bash
npm run dev
```

Open the local URL displayed in the terminal, usually:

[http://localhost:5173](http://localhost:5173)

Both the frontend and backend must be running for features that require the Flask API.

## Testing

The project uses separate testing tools for the frontend and backend.

**Frontend:**

From the `frontend` directory, run the test command configured in `package.json`, for example:

```bash
npm run test
```

**Backend:**

From the `backend` directory, with the virtual environment activated, run:

```bash
pytest
```

Refer to the project configuration for the available test scripts and dependencies.

## Learning Objectives

This project explores key distributed systems concepts, including:

- Logical clocks and vector clock updates.
- Event ordering and causal relationships.
- Message passing between distributed processes.
- The distinction between causally ordered and concurrent events.

## Future Improvements

Potential areas for further development include additional distributed systems scenarios, expanded learning exercises and more detailed explanations of event ordering.

## Author

Developed as a Computer Science individual project exploring interactive tools for learning distributed systems concepts.
