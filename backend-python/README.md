# HireMate AI Backend Service

FastAPI-based backend service for AI-powered resume analysis, interview practice, and career coaching.

## 🎯 Overview

A robust FastAPI application that provides AI-driven career enhancement features including resume analysis, mock interviews, career coaching, and speech recognition capabilities.

## ✨ Features

- **Resume Analysis**: OCR-based PDF processing with ATS compatibility scoring
- **AI Interviews**: Intelligent question generation and answer evaluation using Groq AI
- **Career Coaching**: Personalized career guidance and recommendations
- **Speech Recognition**: Voice-to-text conversion for natural interactions
- **Report Generation**: Comprehensive PDF reports with detailed analytics
- **NLP Processing**: Advanced text analysis, keyword extraction, and semantic similarity

## 🛠 Technology Stack

### Core
- **FastAPI**: Modern Python web framework
- **Uvicorn**: ASGI server
- **Python 3.8+**: Modern Python with async support

### AI & ML
- **Groq**: AI language model integration
- **Spacy**: Natural language processing
- **Sentence Transformers**: Semantic similarity analysis
- **KeyBERT**: Keyword extraction
- **OpenCV + PyTesseract**: OCR processing

### Data & Audio
- **PyPDF2 + pdf2image**: PDF processing
- **SpeechRecognition + pydub**: Audio processing
- **ReportLab**: PDF generation
- **NumPy + SciPy**: Scientific computing

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Groq API key
- Tesseract OCR (for PDF processing)

### Installation

```bash
# Clone and navigate
git clone <repository-url>
cd backend-python

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
python -m spacy download en_core_web_sm

# Set environment variables
echo "GROQ_API_KEY=your_api_key_here" > .env

# Start server
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

## 🔌 API Endpoints

### Core Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/analyze-resume` | Analyze resume with ATS scoring |
| `POST` | `/api/interview/start` | Start interview session |
| `POST` | `/api/interview/evaluate` | Evaluate interview answers |
| `POST` | `/api/interview/next-question` | Get next question |
| `POST` | `/api/interview/report` | Generate interview report |
| `POST` | `/api/career-coach` | Chat with AI career coach |
| `POST` | `/api/speech-to-text` | Convert audio to text |
| `GET` | `/api/test` | Health check |

### Example Usage

```bash
# Test health check
curl http://localhost:8000/api/test

# Analyze resume
curl -X POST "http://localhost:8000/api/analyze-resume" \
  -F "resume=@resume.pdf" \
  -F "job_description=Software Engineer position"
```

## 📁 Project Structure

```
backend-python/
├── main.py                 # FastAPI app entry point
├── interview.py            # Interview logic & AI integration
├── career.py              # Career coaching functionality
├── report.py              # Report generation
├── utils.py               # Utility functions & NLP
├── speech_to_text.py      # Speech recognition
├── ats.py                 # ATS scoring logic
├── test.py                # Testing utilities
├── requirements.txt       # Python dependencies
└── README.md              # This file
```

## ⚙️ Configuration

### Environment Variables
- `GROQ_API_KEY`: Groq API key (required)
- `LOG_LEVEL`: Logging level (default: INFO)

### CORS Configuration
Configured for:
- `https://hire-mate-ai-green.vercel.app` (Production)
- `http://localhost:5173` (Development)

## 🚀 Deployment

### Local Development
```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

### Production (Render)
1. Connect GitHub repository to Render
2. Set environment variables
3. Build Command: `pip install -r requirements.txt && python -m spacy download en_core_web_sm`
4. Start Command: `uvicorn main:app --host 0.0.0.0 --port $PORT`

## 🧪 Testing

```bash
# Run tests
python -m pytest

# Test Groq integration
python test.py

# Test API endpoints
curl http://localhost:8000/api/test
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/your-feature`
3. Follow PEP 8 standards and add tests
4. Submit pull request

## 📄 License

MIT License - see [LICENSE](../LICENSE) for details.

## 🆘 Support

- Check [Issues](https://github.com/your-repo/issues) page
- Create new issue with detailed information
- Contact development team

---

**Note**: This backend service requires a Groq API key for AI functionality. See the [main README](../README.md) for complete project documentation. 