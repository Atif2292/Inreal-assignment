# AI-Powered Job Match Platform

## Project Overview
This project is a mini job matching platform where users can sign up, create their profile, view job listings, and get AI-powered job recommendations based on their profile.

---

## Tech Stack

- **Frontend:** React.js with Tailwind CSS  
- **Backend:** Flask (Python)  
- **Database:** SQLite  
- **Authentication:** JWT (JSON Web Tokens)  
- **AI Integration:** SentenceTransformers for job matching

---

## Setup Instructions

### Backend

1. Clone the repo and go to backend folder  
2. Create a virtual environment and activate it  
3. Install dependencies:  
pip install -r requirements.txt
4. Create `.env` file and add your API keys (if any)  
5. Run the backend server:  
python app.py

### Frontend

1. Go to frontend folder  
2. Install npm packages:  
npm install
3. Start the React app:  
npm start

---

## AI Usage & Prompt Design

- Instead of external AI APIs (like OpenAI or HuggingFace), we used the **SentenceTransformers** library for semantic similarity.  
- The backend calculates embedding vectors for user skills and job skills, then matches jobs with highest similarity scores.  
- This approach avoids API quota limits and is faster for local matching.  

---

## API Documentation

- **POST /api/signup**: Register new user  
- **POST /api/login**: User login (returns JWT token)  
- **POST /api/profile**: Update user profile (skills, location, experience)  
- **GET /api/jobs**: Get all job listings  
- **GET /api/recommendations**: Get AI-powered recommended jobs based on user profile

---

## Code Architecture Overview

- **Frontend:** React components styled with Tailwind CSS, state managed via useState hook.  
- **Backend:** Flask REST API with JWT authentication, SQLAlchemy for ORM, bcrypt for password hashing.  
- **AI Matching:** SentenceTransformers for embedding and cosine similarity for job match score calculation.

---

## Trade-offs & Assumptions

- External AI APIs (OpenAI, HuggingFace) were attempted but faced quota and permission issues, so the project uses SentenceTransformers locally for job recommendations.  
- SQLite is used for simplicity; for production, switch to PostgreSQL or MongoDB.  
- User skills and job skills are stored as comma-separated strings for ease but can be improved with normalized tables.

---

## Live Links

- **Frontend:** [inreal-assign.netlify.app]  
- **Backend API:** [https://dummy-2-7njc.onrender.com/]  
- **GitHub Repo:** [(https://github.com/Atif2292/Inreal-assignment/)]

---

