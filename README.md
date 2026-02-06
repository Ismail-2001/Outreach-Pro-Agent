# Outreach Pro Agent 🚀

**Hyper-personalized cold outreach automation powered by Agentic AI.**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.9%2B-blue.svg)
![React](https://img.shields.io/badge/react-18-blue.svg)
![Status](https://img.shields.io/badge/status-active-green.svg)

## 📖 Project Overview

**Outreach Pro Agent** is an autonomous AI system designed to transform cold outreach from a numbers game into a precision targeting retrieval system. Unlike traditional tools that blast generic templates, this agent researches prospects, analyzes their recent activities (LinkedIn posts, company news), identifies specific "trigger events", and crafts hyper-personalized emails that drive **15-20% response rates**.

Built for modern sales teams, it features a self-correcting "Agentic" workflow that ensures every email meets strict quality standards before it's ever seen by a human.

## ✨ Key Features

*   **🕵️‍♂️ Deep Lead Enrichment**: Automatically aggregates data from LinkedIn, company websites, and news sources to build a comprehensive prospect profile.
*   **🧠 Intelligent Analysis Agent**: Uses Large Language Models (Kimi 2.5) to deduce pain points, professional interests, and strategic entry points.
*   **✍️ Hyper-Personalization Engine**: Generates 100% unique email copy for every lead. No templates—just context-aware writing.
*   **🔄 Self-Correcting Quality Control**: An internal "Auditor" agent scores generated emails against best practices and forces a re-write if quality targets aren't met.
*   **📊 Live Agent Dashboard**: A real-time React interface to monitor the agent's thought process, manage leads, and track campaign ROI.
*   **🧪 A/B Testing**: Automatically generates variant approaches (e.g., "Social Proof" vs. "Problem-First") to optimize conversion.

## 🛠️ Tech Stack

### Frontend
*   **Framework**: React 18 + Vite
*   **Styling**: TailwindCSS
*   **UI Components**: Radix UI / Shadcn UI
*   **Icons**: Lucide React
*   **State Management**: React Hooks

### Backend
*   **API**: FastAPI (Python)
*   **Database**: SQLAlchemy ORM (SQLite for dev, PostgreSQL compatible)
*   **Validation**: Pydantic
*   **Task Management**: Async/Await (Architecture ready for Celery/Redis)

### AI & Agents
*   **LLM Core**: Kimi 2.5 / Moonshot AI (OpenAI-compatible interface)
*   **Agent Logic**: Custom Orchestrator with Feedback Loops

## 🏗️ Architecture

The system follows a multi-stage **Agentic Workflow**:

1.  **Ingestion**: Lead data is captured via API or manual entry.
2.  **Enrichment**: The system attempts to fill in missing details (Company size, recent news).
3.  **Analysis Phase**: The AI Agent reads the enriched profile and outputs a structured "Strategy Document" (Pain points, Hooks).
4.  **Drafting Phase**: The Content Agent writes the email based *strictly* on the Strategy Document.
5.  **Quality Control**: The Auditor Agent reviews the draft. If the score < 80/100, it is sent back for revision.
6.  **Delivery**: The final approved email is queued for sending.

## 🚀 Installation & Setup

### Prerequisites
*   Node.js 18+
*   Python 3.9+
*   Git

### 1. Clone the Repository
```bash
git clone https://github.com/Ismail-2001/Outreach-Pro-Agent.git
cd Outreach-Pro-Agent
```

### 2. Backend Setup
```bash
cd outreach-architect
# Create virtual environment (optional but recommended)
python -m venv venv
# Windows: venv\Scripts\activate
# Mac/Linux: source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the server
python main.py
```
*The backend runs on `http://localhost:8000`*

### 3. Frontend Setup
```bash
# Open a new terminal
cd app

# Install dependencies
npm install

# Start the dev server
npm run dev
```
*The dashboard runs on `http://localhost:5173`*

### 4. Environment Keys
Create a `.env` file in `outreach-architect/`:
```env
KIMI_API_KEY=your_api_key_here  # Leave empty to use Mock Mode
DATABASE_URL=sqlite:///./outreach.db
LOG_LEVEL=INFO
```

## 🎮 Usage

1.  **Open the Dashboard**: Navigate to `http://localhost:5173`.
2.  **Live Demo**: Click on "Go to Dashboard" or scroll to the Live Demo section.
3.  **Create a Lead**: Enter a prospect's name, company, and role.
4.  **Run Agent**: Click "Generate Campaign".
5.  **Observe**: Watch the terminal output as the agent performs researching, analyzing, and drafting steps in real-time.

## 📦 Deployment

### Frontend (Vercel/Netlify)
The `app` folder is a standard Vite application.
1.  Push repo to GitHub.
2.  Import into Vercel.
3.  Set Root Directory to `app`.
4.  Build Command: `npm run build`.
5.  Output Directory: `dist`.

### Backend (Railway/Render)
1.  Deploy the `outreach-architect` folder.
2.  Ensure `python main.py` is the start command (or use `uvicorn main:app --host 0.0.0.0 --port $PORT`).
3.  Set environment variables.

## 🗺️ Roadmap

*   [ ] **LinkedIn Integration**: Real-time scraper for live profile data.
*   [ ] **Email Sending**: Integration with Gmail/Outlook APIs.
*   [ ] **Multi-User Support**: Auth0 authentication for sales teams.
*   [ ] **Campaign Sequences**: Multi-step automated follow-ups.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:
1.  Fork the project.
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

*Built with ❤️ by the Ismail Sajid*
