# HireMate AI - Resume Analyzer & Mock Interviewer

![HireMate AI Logo](HireMate%20Logo.svg)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Project Structure](#project-structure)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

HireMate AI is a comprehensive AI-powered career enhancement platform that combines resume analysis, interview practice, and career coaching into a single, intelligent application. The platform leverages advanced natural language processing and machine learning techniques to provide personalized career guidance and interview preparation.

### Key Capabilities

- **Resume Analysis**: Advanced ATS (Applicant Tracking System) compatibility scoring with detailed feedback
- **Mock Interviews**: AI-powered interview practice with speech recognition and real-time evaluation
- **Career Coaching**: Personalized career guidance and skill development recommendations
- **Report Generation**: Comprehensive performance reports with actionable insights
- **Speech Recognition**: Voice-to-text functionality for natural interview interactions

## ✨ Features

### 🔍 Resume Analysis & ATS Scoring
- **PDF Processing**: Advanced OCR-based text extraction from PDF resumes
- **ATS Optimization**: Real-time compatibility scoring against job descriptions
- **Keyword Analysis**: Intelligent keyword extraction and matching
- **Improvement Suggestions**: Actionable recommendations for resume enhancement
- **Similarity Scoring**: Semantic similarity analysis using advanced NLP techniques

### 🎤 AI-Powered Mock Interviews
- **Personalized Questions**: CV-based interview questions generated using AI
- **Real-time Evaluation**: Instant feedback on interview responses
- **Speech Recognition**: Voice-to-text conversion for natural interactions
- **Progressive Difficulty**: Adaptive questioning based on performance
- **Conversational Flow**: Natural dialogue simulation with context awareness

### 🎯 Career Coaching
- **Personalized Guidance**: AI-driven career advice based on resume and goals
- **Skill Development**: Targeted learning recommendations
- **Job Search Strategy**: Strategic career planning and job search guidance
- **Interactive Chat**: Natural conversation interface with the AI coach

### 📊 Comprehensive Reporting
- **Performance Analytics**: Detailed scoring and performance metrics
- **Strengths Analysis**: Identification of key strengths and competencies
- **Improvement Areas**: Specific recommendations for enhancement
- **PDF Export**: Professional report generation in PDF format
- **Progress Tracking**: Historical performance monitoring

### 🎨 Modern User Interface
- **Responsive Design**: Mobile-first approach with cross-device compatibility
- **Intuitive Navigation**: User-friendly interface with clear navigation
- **Real-time Updates**: Live feedback and progress indicators
- **Accessibility**: WCAG compliant design principles
- **Dark Mode Support**: Optional dark theme for enhanced user experience

## 🛠 Technology Stack

### Frontend
- **React 18**: Modern React with hooks and functional components
- **TypeScript**: Type-safe JavaScript development
- **Vite**: Fast build tool and development server
- **React Router**: Client-side routing and navigation
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Modern icon library
- **Axios**: HTTP client for API communication
- **jsPDF**: PDF generation for reports

### Backend
- **FastAPI**: Modern Python web framework
- **Uvicorn**: ASGI server for FastAPI
- **Groq**: AI language model integration
- **Spacy**: Natural language processing
- **OpenCV**: Computer vision for OCR
- **PyTesseract**: OCR text extraction
- **Sentence Transformers**: Semantic similarity analysis
- **KeyBERT**: Keyword extraction
- **SpeechRecognition**: Speech-to-text conversion
- **PyPDF2**: PDF processing and manipulation

### Development Tools
- **ESLint**: Code linting and quality assurance
- **PostCSS**: CSS processing and optimization
- **Autoprefixer**: CSS vendor prefixing
- **TypeScript**: Type checking and compilation

## 🏗 Architecture

### System Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   External      │
│   (React/Vite)  │◄──►│   (FastAPI)     │◄──►│   Services      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         │                       │                       │
    ┌─────────┐            ┌─────────┐              ┌─────────┐
    │ Session │            │ AI/ML   │              │ Groq    │
    │Storage  │            │Models   │              │ API     │
    └─────────┘            └─────────┘              └─────────┘
```

### Component Architecture

- **Frontend**: Single Page Application (SPA) with component-based architecture
- **Backend**: RESTful API with modular service architecture
- **Data Flow**: State management through React hooks and session storage
- **Communication**: HTTP/HTTPS API communication with JSON data format

## 📋 Prerequisites

### System Requirements
- **Node.js**: Version 18 or higher
- **Python**: Version 3.8 or higher
- **npm**: Version 8 or higher
- **pip**: Python package manager

### Development Environment
- **Git**: Version control system
- **Code Editor**: VS Code (recommended) or any modern code editor
- **Browser**: Modern web browser with JavaScript enabled

### External Services
- **Groq API**: AI language model service (requires API key)
- **Google Speech Recognition**: Speech-to-text service (optional)

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone <repository-url>
cd resume-analyser-mock-interviewer
```

### 2. Frontend Setup

```bash
# Install Node.js dependencies
npm install

# Start development server
npm run dev
```

### 3. Backend Setup

```bash
# Navigate to backend directory
cd backend-python

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install Python dependencies
pip install -r requirements.txt

# Download Spacy model
python -m spacy download en_core_web_sm

# Start backend server
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

### 4. Environment Configuration

Create a `.env` file in the `backend-python` directory:

```env
GROQ_API_KEY=your_groq_api_key_here
```

## ⚙️ Configuration

### Frontend Configuration

The frontend configuration is managed through `src/config.js`:

- **Development Environment**: Local development with `http://localhost:8000`
- **Production Environment**: Deployed backend URL
- **Mobile Environment**: Mobile-optimized backend URL

### Backend Configuration

Key configuration files:

- **main.py**: FastAPI application configuration and middleware
- **requirements.txt**: Python dependencies and versions
- **.env**: Environment variables and API keys

### CORS Configuration

The backend is configured to accept requests from:
- `https://hire-mate-ai-green.vercel.app` (Production)
- `http://localhost:5173` (Development)

## 📖 Usage

### 1. Resume Upload and Analysis

1. Navigate to the "Resume Upload" page
2. Upload a PDF resume file
3. Enter a job description for ATS scoring
4. Receive instant analysis with ATS compatibility score
5. View detailed feedback and improvement suggestions

### 2. Mock Interview Practice

1. Access the "Interview" page (requires uploaded resume)
2. Introduce yourself to start the interview
3. Answer AI-generated questions based on your resume
4. Use voice input or text input for responses
5. Receive real-time evaluation and feedback
6. Continue through multiple rounds of questions

### 3. Career Coaching

1. Visit the "Career Coach" page
2. Chat with the AI career coach about your goals
3. Receive personalized career advice and guidance
4. Get skill development recommendations
5. Discuss job search strategies

### 4. Report Generation

1. Complete interview sessions to generate reports
2. Access the "Report" page for comprehensive analysis
3. View performance metrics and scores
4. Download PDF reports for offline use
5. Track progress over time

## 🔌 API Endpoints

### Resume Analysis
- `POST /api/analyze-resume`: Upload and analyze resume with ATS scoring
- `POST /api/extract-name`: Extract candidate name from resume

### Interview Management
- `POST /api/interview/start`: Initialize interview session
- `POST /api/interview/evaluate`: Evaluate interview answers
- `POST /api/interview/next-question`: Get next interview question
- `POST /api/interview/report`: Generate interview report

### Career Coaching
- `POST /api/career-coach`: Chat with AI career coach

### Speech Recognition
- `POST /api/speech-to-text`: Convert audio to text

### Utility Endpoints
- `GET /api/test`: Health check endpoint

## 📁 Project Structure

```
resume-analyser-mock-interviewer/
├── backend-python/                 # Python backend
│   ├── main.py                     # FastAPI application entry point
│   ├── requirements.txt            # Python dependencies
│   ├── interview.py                # Interview logic and AI integration
│   ├── career.py                   # Career coaching functionality
│   ├── report.py                   # Report generation
│   ├── utils.py                    # Utility functions and NLP
│   ├── speech_to_text.py           # Speech recognition
│   ├── ats.py                      # ATS scoring logic
│   └── test.py                     # Testing utilities
├── src/                           # React frontend
│   ├── components/                # Reusable React components
│   │   └── Navigation.jsx         # Navigation component
│   ├── pages/                     # Page components
│   │   ├── Home.jsx              # Landing page
│   │   ├── Upload.jsx            # Resume upload page
│   │   ├── Interview.jsx         # Interview practice page
│   │   ├── Report.jsx            # Report generation page
│   │   └── CareerCoach.jsx       # Career coaching page
│   ├── App.tsx                   # Main React application
│   ├── main.tsx                  # React entry point
│   ├── config.js                 # Configuration settings
│   └── index.css                 # Global styles
├── public/                       # Static assets
├── package.json                  # Node.js dependencies
├── vite.config.ts               # Vite configuration
├── tailwind.config.js           # Tailwind CSS configuration
├── tsconfig.json                # TypeScript configuration
├── render.yaml                  # Deployment configuration
└── README.md                    # Project documentation
```

## 🚀 Deployment

### Frontend Deployment (Vercel)

1. Connect your GitHub repository to Vercel
2. Configure build settings:
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Install Command: `npm install`

### Backend Deployment (Render)

1. Connect your GitHub repository to Render
2. Configure service settings:
   - Environment: Python
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `uvicorn main:app --host 0.0.0.0 --port $PORT`

### Environment Variables

Set the following environment variables in your deployment platform:

- `GROQ_API_KEY`: Your Groq API key for AI functionality

## 🤝 Contributing

### Development Workflow

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Submit a pull request

### Code Standards

- Follow ESLint configuration for JavaScript/TypeScript
- Use TypeScript for type safety
- Follow PEP 8 for Python code
- Write meaningful commit messages
- Add tests for new features

### Testing

- Run frontend tests: `npm run test`
- Run backend tests: `python -m pytest`
- Test API endpoints using Postman or similar tools

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:

1. Check the [Issues](https://github.com/your-repo/issues) page
2. Create a new issue with detailed information
3. Contact the development team

## 🔄 Version History

- **v1.0.0**: Initial release with core features
- **v1.1.0**: Added speech recognition and enhanced UI
- **v1.2.0**: Improved ATS scoring and report generation
- **v1.3.0**: Added career coaching and mobile optimization

## 🙏 Acknowledgments

- Groq for providing AI language model services
- Open source community for various libraries and tools
- Contributors and beta testers for feedback and improvements

---

**Note**: This project is actively maintained and regularly updated with new features and improvements. Please check the repository for the latest version and updates.