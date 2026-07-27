# AI Powered Interview Assistant

An AI-powered interview application that conducts mock technical interviews through voice interaction. The application asks interview questions, records candidate responses, converts speech to text, evaluates answers using an LLM, and provides detailed feedback at the end of the interview.

## Live Demo

**Application:** https://ai-powered-interview-assistant-sigma.vercel.app

**GitHub Repository:** https://github.com/chinna0425/AI-Powered-Interview-Assistant

---

## Features

- AI-driven interview experience
- Voice-based question and answer interaction
- Speech-to-text conversion for candidate responses
- Dynamic interview flow with conversation memory
- AI-generated feedback after interview completion
- Candidate score and performance summary
- Simple and responsive web interface

---

## Tech Stack

### Frontend

- HTML
- CSS
- JavaScript

### Backend

- Python
- FastAPI

### AI & LLM

- LangChain
- LangGraph
- Groq (Llama 3.3 70B)
- AssemblyAI (Speech-to-Text)

### Other Technologies

- REST APIs
- Python Dotenv

---

## Project Structure

```
AI-Powered-Interview-Assistant/
│
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── ...
│
├── frontend/
│   ├── index.html
│   ├── script.js
│   ├── style.css
│   └── ...
│
├── .env
├── README.md
└── requirements.txt
```

---

## Workflow

1. Select the interview subject.
2. The AI generates the first interview question.
3. The candidate answers using their microphone.
4. Speech is converted into text.
5. The response is evaluated and stored in conversation memory.
6. The AI generates the next question based on the interview flow.
7. After all questions are completed, the AI generates:
   - Overall score
   - Performance summary
   - Strengths
   - Areas for improvement
   - Suggestions for further learning

---

## System Architecture

```
                Candidate
                     │
                     ▼
             Frontend (HTML/CSS/JS)
                     │
                     ▼
               FastAPI Backend
                     │
          ┌──────────┴──────────┐
          │                     │
          ▼                     ▼
   AssemblyAI STT         LangGraph Memory
          │                     │
          └──────────┬──────────┘
                     ▼
          Groq Llama 3.3 (LLM)
                     │
                     ▼
            Interview Feedback
```

---

## Installation

### Clone the repository

```bash
git clone https://github.com/chinna0425/AI-Powered-Interview-Assistant.git

cd AI-Powered-Interview-Assistant
```

---

### Create a virtual environment

```bash
python -m venv venv
```

---

### Activate the environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

---

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
ASSEMBLYAI_API_KEY=your_assemblyai_api_key
```

---

## Run the Backend

```bash
uvicorn app:app --reload
```

---

## Run the Frontend

Open `index.html` in your browser or serve the frontend using any local server.

---

## Example Interview Flow

```
AI:
Tell me about yourself.

Candidate:
Introduces themselves.

↓

AI:
What is React?

↓

Candidate:
Explains React.

↓

AI:
Can you explain the Virtual DOM?

↓

Candidate:
Answers.

↓

AI:
Interview completed.

Overall Score: 8.6 / 10

Feedback:
• Good understanding of React fundamentals.
• Improve explanation of state management.
• Practice advanced JavaScript concepts.
```

---

## Future Improvements

- Multiple interview domains
- Resume-based interview generation
- Difficulty level selection
- Conversation history
- Authentication
- Dashboard for interview reports
- Video interview support
- Database integration


## License

This project is created for learning and educational purposes.
