# 🎯 Opportunity Hunter
### Discover Opportunities. Match Your Potential. Take Action.

**Opportunity Hunter** is an AI-powered opportunity discovery platform designed to help students and job seekers find relevant scholarships, hackathons, internships, grants, and other career-building opportunities.

Instead of manually searching across multiple websites, users can create a personalized profile using their resume or GitHub information, discover opportunities suited to their background, evaluate match scores, and prepare applications with AI assistance.

---

## ✨ Features

### 👤 1. Personalized Profile Creation
- Create a profile by uploading a resume or providing supported profile information.
- Extract relevant skills, education, and experience.
- Use profile information to personalize opportunity discovery.

### 🔎 2. AI-Powered Opportunity Discovery
- Discover scholarships, internships, hackathons, grants, and similar opportunities.
- Use web search to find potentially relevant opportunities.
- Generate results based on a user's profile and interests.

### 📊 3. Opportunity Matching
- Evaluate opportunities against a user's profile.
- Present match scores and relevant explanations.
- Help users identify opportunities that better fit their skills and eligibility.

### 🤖 4. AI Application Co-Pilot
- Generate tailored cover letter drafts.
- Summarize application requirements.
- Create application checklists.
- Help users organize their next steps.

### 🎯 5. Profile-Specific Results
- Associate discovered opportunities with the corresponding user profile.
- Retrieve opportunities for the selected profile.
- Reduce confusion between results belonging to different profiles.

---

## 🏗️ Architecture

Opportunity Hunter uses a frontend, backend, and database architecture.

| Component | Technology |
|---|---|
| Frontend | Next.js, React, TypeScript |
| Styling | Tailwind CSS, Shadcn UI |
| Backend | Python, FastAPI |
| Database | Supabase, PostgreSQL |
| AI integration | OpenRouter |
| Web search | Tavily API |
| Frontend deployment | Vercel-compatible |
| Backend deployment | Railway-compatible |

The application separates the user interface, API endpoints, AI processing, and persistent data storage.

### How It Works

```text
       User
        |
        v
  Next.js Frontend
        |
        v
   FastAPI Backend
        |
        +------------------+
        |                  |
        v                  v
   AI Processing       Web Search
   OpenRouter          Tavily API
        |                  |
        +---------+--------+
                  |
                  v
       Opportunity Matching
                  |
                  v
        Supabase Database
                  |
                  v
      Personalized Dashboard
```

---

## 🛠️ Technology Stack

**Frontend**
- Next.js
- React
- TypeScript
- Tailwind CSS

**Backend**
- Python
- FastAPI
- Pydantic

**Database**
- Supabase
- PostgreSQL

**External Services**
- OpenRouter for AI model access
- Tavily for web search

---

## 🚀 Getting Started

Follow these instructions to run the project locally.

### Prerequisites

Install the following:

- Python 3.11 or a compatible version
- Node.js and npm
- A Supabase project
- An OpenRouter API key
- A Tavily API key

### 1. Clone the Repository

```bash
git clone https://github.com/Mathesh213/oppurtunity-hunter.git
cd oppurtunity-hunter
```

### 2. Configure the Backend

Navigate to the backend directory:

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Create a `backend/.env` file and configure the environment variables required by your backend implementation.

Typical configuration categories include:

```env
OPENROUTER_API_KEY=your_openrouter_api_key
TAVILY_API_KEY=your_tavily_api_key
SUPABASE_URL=your_supabase_project_url
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key
```

Use the exact variable names expected by your backend configuration. Additional model or provider settings may be required.

**Security:** Never commit API keys, service-role keys, passwords, or other secrets to GitHub.

Start the backend:

```bash
uvicorn main:app --reload --port 8000
```

The API will be available at:

`http://localhost:8000`

### 3. Configure the Frontend

Open another terminal and navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Create a `frontend/.env.local` file with the appropriate backend and public Supabase configuration:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
```

Configure only the variables required by your frontend.

Start the development server:

```bash
npm run dev
```

Open:

`http://localhost:3000`

---

## 🗄️ Database Setup

Opportunity Hunter uses Supabase for persistent storage.

The application uses profile and opportunity data, including the association between an opportunity and its corresponding user profile.

If your database does not yet contain the required schema, configure the necessary tables, relationships, and indexes before running the application.

For profile-specific opportunity storage, the `opportunities` table should contain a `profile_id` column that references the corresponding profile record.

Ensure database access policies and backend credentials are configured securely for your deployment.

---

## 🎬 Application Workflow

1. **Create a profile** using the available onboarding options.
2. **Provide your background** through resume or profile information.
3. **Run the Hunter Agent** to discover relevant opportunities.
4. **Review matches** and evaluate their relevance to your profile.
5. **Open the Application Co-Pilot** for application guidance.
6. **Prepare your application** using the generated checklist and cover letter draft.

AI-generated results should be verified against the original opportunity listing before applying.

---

## 🔐 Environment Variables

Keep environment files local and out of version control.

| Variable | Purpose |
|---|---|
| `OPENROUTER_API_KEY` | Access AI models through OpenRouter |
| `TAVILY_API_KEY` | Access web search |
| `SUPABASE_URL` | Connect the backend to Supabase |
| `SUPABASE_SERVICE_ROLE_KEY` | Server-side database access |
| `NEXT_PUBLIC_API_URL` | Frontend API endpoint |
| `NEXT_PUBLIC_SUPABASE_URL` | Public Supabase project URL |
| `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Public Supabase client key |

The exact variables required depend on the configuration implemented in the project.

Never expose a Supabase service-role key in frontend code or publish it in a public repository.

---

## 🔮 Potential Future Improvements

- Deadline reminders and notifications
- Saved opportunities and application tracking
- Advanced filtering by location, eligibility, and category
- Improved duplicate detection
- Personalized recommendations based on user feedback
- Opportunity status tracking
- Automated deployment and testing
- Expanded support for additional opportunity sources

---

## 👨‍💻 Development

Opportunity Hunter is an evolving project focused on personalized opportunity discovery, AI-assisted recommendations, and application preparation.

Contributions, feedback, and suggestions for improving the platform are welcome.

---

## 📄 License

No license has been specified yet. If you plan to distribute or accept contributions to this project, consider adding an appropriate open-source license.

---

**Built to help students and job seekers spend less time searching and more time pursuing opportunities.**