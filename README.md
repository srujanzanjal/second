# AI Pharmacist 💊 - Smart Healthcare Management System

A full-stack AI-powered pharmacy assistant application built with Next.js, FastAPI, and modern ML technologies.

## 🎯 Features

### Frontend Application
- **9 Complete Pages**: Landing, Login, Signup, Dashboard, Chat, Medicines, Alerts, OCR, Settings
- **AI Chat Assistant**: Real-time conversation with Groq LLM integration
- **Prescription OCR**: Upload and analyze prescription images
- **Medicine Inventory**: Browse and manage medicines with search/filter
- **Refill Predictions**: ML-powered medication refill alerts
- **Multi-language Support**: English, Hindi, Marathi translations
- **Dark Mode**: Complete light/dark theme support
- **Responsive Design**: Mobile, tablet, and desktop optimized
- **Authentication**: Secure login with Supabase

### Backend API
- **RESTful API**: FastAPI with async support
- **Chat Endpoint**: AI conversation with intent recognition
- **OCR Processing**: Prescription image analysis
- **Predictions**: ML-based refill forecasting
- **Product Management**: Medicine inventory endpoints
- **User Profiles**: Account and preference management
- **Health Integration**: Allergy and condition tracking

### Technology Stack
- **Frontend**: Next.js 16, React 19, TypeScript, TailwindCSS
- **Backend**: FastAPI, Python 3.14, async/await
- **Database**: Supabase (PostgreSQL)
- **AI/ML**: Groq, OpenAI, scikit-learn, pandas
- **Auth**: Supabase Auth
- **OCR**: Computer vision integration

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/srujanzanjal/second.git
cd second

# Backend Setup
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Configure .env
cp .env.example .env
# Edit .env with your API keys

# Frontend Setup
cd ../frontend
npm install

# Configure .env
cp .env.example .env.local
# Edit .env.local with your Supabase credentials
```

### Running the Application

```bash
# Terminal 1: Frontend
cd frontend
npm run dev
# Runs on http://localhost:3000

# Terminal 2: Backend
cd backend
source venv/bin/activate
python run.py
# Runs on http://localhost:8000
```

## 📋 Environment Variables

### Backend `.env`
```env
# Supabase Configuration
SUPABASE_URL=https://your-supabase-url.supabase.co
SUPABASE_KEY=your_supabase_key

# AI/LLM Configuration
GROQ_API_KEY=your_groq_api_key
OPENAI_API_KEY=your_openai_api_key

# Database
DATABASE_URL=postgresql://user:password@host/database

# Server Configuration
DEBUG=false
ENVIRONMENT=production
```

### Frontend `.env.local`
```env
# Supabase
NEXT_PUBLIC_SUPABASE_URL=https://your-supabase-url.supabase.co
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_DEFAULT_KEY=your_supabase_key

# Backend API
NEXT_PUBLIC_API_URL=http://localhost:8000
```

## 🏗️ Project Structure

```
├── frontend/                 # Next.js React application
│   ├── app/                 # Next.js pages and routes
│   ├── components/          # Reusable UI components
│   ├── contexts/            # React contexts (Auth, Language)
│   ├── hooks/               # Custom React hooks
│   ├── lib/                 # Utilities, API client, types
│   └── public/              # Static assets
│
├── backend/                 # FastAPI Python server
│   ├── core/                # Configuration, database, middleware
│   ├── models/              # Data models and schemas
│   ├── repositories/        # Database access layer
│   ├── routers/             # API endpoints
│   ├── services/            # Business logic
│   └── tests/               # Test files
│
└── docs/                    # Documentation
```

## 📖 Pages Overview

### Public Pages
- **Landing Page** (`/`): Feature showcase and call-to-action
- **Login** (`/auth/login`): User authentication
- **Signup** (`/auth/signup`): New user registration

### Protected Pages (Dashboard)
- **Home** (`/dashboard`): Stats, recent orders, insights
- **Chat** (`/dashboard/chat`): AI pharmacist conversation
- **Medicines** (`/dashboard/medicines`): Product catalog
- **Alerts** (`/dashboard/alerts`): Refill predictions
- **OCR** (`/dashboard/ocr`): Prescription analysis
- **Settings** (`/dashboard/settings`): User preferences

## 🔌 API Endpoints

### Chat
- `POST /api/v1/chat` - Send message to AI assistant

### Products
- `GET /api/v1/products` - List medicines
- `GET /api/v1/products/{id}` - Get product details

### Predictions
- `GET /api/v1/predictions/refill` - Get refill predictions

### Prescriptions
- `POST /api/v1/prescriptions/demo/analyze` - OCR analysis

### Dashboard
- `GET /api/v1/dashboard/stats` - Dashboard statistics
- `GET /api/v1/dashboard/insights` - AI insights

### Health
- `GET /health` - Health check endpoint
- `GET /docs` - Swagger API documentation

## 🧪 Testing

```bash
# Backend tests
cd backend
pytest

# Frontend tests
cd frontend
npm test

# Component testing
npm run test:components
```

## 🎨 UI Components

Built with shadcn/ui and customized Radix UI components:
- Button, Input, Card, Badge, Avatar
- Dropdown Menu, Sheet, Separator
- Switch, Label, Scroll Area, Form

## 🌐 Internationalization

Supported languages:
- 🇬🇧 English (en)
- 🇮🇳 हिंदी (hi)
- 🇮🇳 मराठी (mr)

## 📊 Key Features

### AI Chat Integration
- Real-time chat with Groq LLM
- Intent recognition
- Multi-language support
- Voice input and text-to-speech

### ML Predictions
- Medication refill forecasting
- Stock level analysis
- Patient consumption patterns
- Confidence scoring

### Security
- Supabase authentication
- Protected routes
- Secure API endpoints
- Environment variable isolation

## ✅ Status

- ✓ All 9 pages implemented and tested
- ✓ Backend API functional
- ✓ Frontend-Backend integration working
- ✓ UI/UX complete
- ✓ Multi-language support active
- ✓ Dark mode enabled
- ✓ Responsive design
- ✓ Error handling implemented
- ✓ Loading states
- ✓ Mock data with API fallbacks

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Srujan Zanjal**
- GitHub: [@srujanzanjal](https://github.com/srujanzanjal)

## 📞 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Check existing documentation in `/docs`
- Review API documentation at `http://localhost:8000/docs`

## 🎉 Acknowledgments

- Supabase for backend infrastructure
- Groq for LLM API
- Next.js team for the amazing framework
- FastAPI team for the backend framework
- shadcn/ui for component library

---

**Last Updated**: February 25, 2026 | **Status**: Production Ready ✅
