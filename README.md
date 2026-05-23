# Employee Knowledge System

An AI-powered Employee Knowledge Management System built using Flask, SQLite, and Groq LLM API. This system helps organizations store employee problem-solving experiences and allows users to ask questions and receive intelligent answers based on saved organizational knowledge.

---

## 📌 Project Overview

The Employee Knowledge System is designed to capture employee knowledge, workplace problems, solutions, and lessons learned in a centralized system.

Instead of losing valuable experience when employees leave or change roles, this platform stores knowledge and uses AI to answer questions based on previously recorded information.

The application also includes a dashboard for tracking knowledge entries, employees, and AI queries.

---

## 🚀 Features

- Employee knowledge submission
- AI-based question answering system
- Knowledge database storage
- Dashboard with analytics
- View employee knowledge records
- Delete knowledge entries
- Question history tracking
- User-friendly web interface

---

## 🛠 Technologies Used

### Frontend
- HTML
- CSS
- JavaScript

### Backend
- Python
- Flask

### Database
- SQLite

### AI / API
- Groq API
- Llama 3.1 8B Instant Model

### Libraries Used
- Flask
- OpenAI SDK
- SQLite3
- Python Dotenv

---

## 📂 Project Structure

```plaintext
employee-knowledge-system/
│── app.py
│── .env
│
├── database/
│   └── knowledge.db
│
├── static/
│   ├── style.css
│   └── script.js
│
├── templates/
│   ├── welcome.html
│   ├── index.html
│   ├── ask.html
│   └── view.html
│
├── uploads/
│
└── vector_store/
```

---

## ⚙️ How the System Works

### 1. Knowledge Submission
Employees submit:

- Employee Name
- Department
- Problem faced
- Solution implemented
- Lesson learned

This information is stored in an SQLite database.

### 2. AI Knowledge Retrieval
When a user asks a question:

1. The question is stored in the database.
2. Previously stored employee knowledge is retrieved.
3. A prompt is generated dynamically.
4. The prompt is sent to the Groq API using the Llama model.
5. AI generates a practical answer based on employee experiences.

### 3. Dashboard Analytics
The dashboard displays:

- Total knowledge entries
- Total employees
- Total AI queries
- Recent knowledge entries
- Recently asked questions

---

## 🏗️ System Workflow

```plaintext
Employee Input
       ↓
Store in SQLite Database
       ↓
User Asks Question
       ↓
Retrieve Stored Knowledge
       ↓
Generate Prompt
       ↓
Groq LLM API (Llama 3.1)
       ↓
AI Response Generated
       ↓
Display Answer to User
```

---

## 🔧 Installation Steps

### Step 1: Clone Repository

```bash
git clone <repository-url>
```

### Step 2: Move into Project Folder

```bash
cd employee-knowledge-system
```

### Step 3: Install Dependencies

```bash
pip install flask openai python-dotenv
```

### Step 4: Create `.env` File

Add your Groq API key:

```env
GROQ_API_KEY=your_api_key_here
```

### Step 5: Run Application

```bash
python app.py
```

### Step 6: Open Browser

Open:

```plaintext
http://127.0.0.1:5000/
```

---

## 🗄 Database Design

### Table: knowledge

| Column | Description |
|--------|-------------|
| id | Unique ID |
| employee_name | Employee name |
| department | Department name |
| problem | Problem faced |
| solution | Solution applied |
| lesson | Lesson learned |

### Table: question_history

| Column | Description |
|--------|-------------|
| id | Unique ID |
| question | User asked question |

---

## 📸 Pages in the System

### Welcome Page
Landing page of the application.

### Dashboard
Displays analytics and employee knowledge statistics.

### Ask AI Page
Allows users to ask questions and receive AI-generated responses.

### View Knowledge Page
Displays all stored knowledge records.

---

## 🔥 Advantages

- Prevents knowledge loss in organizations
- Reuses employee expertise
- Fast knowledge retrieval
- AI-assisted practical responses
- Easy to use and lightweight system

---

## 🚧 Challenges Faced

Developing the Employee Knowledge System involved several challenges. One major challenge was connecting the Flask backend with the SQLite database and managing employee knowledge efficiently. Another challenge was generating meaningful AI responses using stored knowledge through prompt engineering. Proper handling of API keys using environment variables and integrating the Groq API with Flask also required careful implementation. Designing a clean and responsive interface while maintaining smooth communication between frontend and backend was another challenge faced during development.

---

## 🔮 Future Enhancements

- Authentication and login system
- Role-based access control
- Knowledge search functionality
- File/document upload support
- Better dashboard analytics
- Vector database integration for advanced retrieval
- Semantic search using embeddings

---

## 👨‍💻 Author

Developed as an AI-powered knowledge management project using Flask and Groq LLM.
