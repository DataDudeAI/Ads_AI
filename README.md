# AI Tools Platform - Refactored v2.0.0

A comprehensive, modular AI tools platform with enhanced security, scalability, and maintainability.

## 🚀 Features

### Core Functionality
- **Multi-Provider AI Integration**: Support for OpenAI, Hugging Face, DeepSeek, OpenRouter, and more
- **Credit System**: Flexible credit management with ad-based rewards
- **Tool Marketplace**: 15+ AI tools including text generation, image creation, code generation, and more
- **User Management**: Secure authentication with session management
- **Admin Dashboard**: Comprehensive admin controls and analytics

### Enhanced Architecture
- **Modular Design**: Separated concerns into dedicated modules
- **Security First**: API key encryption, rate limiting, input sanitization
- **Scalable**: Database-driven with proper indexing and caching
- **Maintainable**: Clean code structure with comprehensive documentation

## 📁 Project Structure

```
GenAiToolbox/
├── app_refactored.py          # Main FastAPI application
├── requirements_enhanced.txt  # Enhanced dependencies
├── 
├── credit/                    # Credit system module
│   ├── __init__.py
│   ├── manager.py            # Credit operations and packages
│   └── history.py            # Transaction tracking
│
├── ads/                      # Advertisement system
│   ├── __init__.py
│   ├── manager.py            # Ad management and rewards
│   └── tracking.py           # Impression and click tracking
│
├── models/                   # Database models
│   ├── __init__.py
│   ├── base.py              # Database configuration
│   ├── user.py              # User model
│   └── selector/            # Model selection logic
│       ├── __init__.py
│       └── selector.py      # Intelligent model selection
│
├── auth/                    # Authentication system
│   ├── __init__.py
│   ├── session.py           # Session management
│   └── user.py              # User authentication
│
├── tools/                   # AI tools definitions
│   ├── __init__.py
│   ├── definitions.py       # Tool configurations
│   └── handlers.py          # Tool processing logic
│
├── utils/                   # Shared utilities
│   ├── __init__.py
│   ├── security.py          # Security utilities
│   ├── validation.py        # Input validation
│   └── logging.py           # Logging utilities
│
├── middleware/              # Request/response middleware
│   ├── __init__.py
│   ├── rate_limiter.py      # Rate limiting
│   ├── auth_middleware.py   # Authentication middleware
│   └── logging_middleware.py # Request logging
│
├── providers/               # AI provider integrations
├── prompts/                 # Prompt marketplace
├── static/                  # Static assets
├── templates/               # HTML templates
└── agents/                  # AI agent logic
```

## 🛠️ Installation

### Prerequisites
- Python 3.8+
- SQLite (or PostgreSQL for production)
- Redis (optional, for caching)

### Setup

1. **Clone the repository**
```bash
git clone <repository-url>
cd GenAiToolbox
```

2. **Install dependencies**
```bash
pip install -r requirements_enhanced.txt
```

3. **Environment configuration**
```bash
cp .env.example .env
# Edit .env with your API keys and settings
```

4. **Initialize database**
```bash
python -c "from models.base import init_database; init_database()"
```

5. **Run the application**
```bash
python app_refactored.py
```

## 🔧 Configuration

### Environment Variables

```env
# Security
SECRET_KEY=your-secret-key-here
SECURE_COOKIES=false  # Set to true in production

# Database
DATABASE_URL=sqlite:///./magicAi.db

# AI Provider API Keys
OPENAI_API_KEY=sk-your-openai-key
HUGGINGFACE_API_KEY=hf-your-huggingface-key
DEEPSEEK_API_KEY=sk-your-deepseek-key
OPENROUTER_API_KEY=sk-or-your-openrouter-key

# Google OAuth (optional)
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret

# Redis (optional)
REDIS_URL=redis://localhost:6379
```

## 🎯 Available Tools

### Text Generation
- **Text Generation**: High-quality content creation
- **AI Copywriter**: Marketing copy and content
- **Email Generator**: Professional email drafting
- **Blog Writer**: SEO-optimized blog posts
- **AI Poetry Generator**: Creative poetry creation

### Career & Professional
- **Resume Builder**: Professional resume creation
- **Cover Letter Creator**: Customized cover letters

### Creative & Media
- **Script Generator**: Video and movie scripts
- **AI Storytelling**: Creative story development
- **Image Generation**: AI-powered image creation

### Technical
- **Code Generation**: Multi-language code creation
- **Chatbot Assistant**: Support and conversation

### Wellness
- **AI Meditation Coach**: Guided relaxation exercises

## 🔐 Security Features

### Authentication & Authorization
- Secure password hashing with bcrypt
- Session-based authentication
- Role-based access control
- CSRF protection

### API Security
- Rate limiting per user/IP
- Input sanitization
- API key encryption
- Secure headers

### Data Protection
- Encrypted API key storage
- Secure session management
- Input validation and sanitization

## 📊 Monitoring & Analytics

### Built-in Analytics
- User activity tracking
- Tool usage statistics
- Credit transaction history
- Ad performance metrics

### Admin Dashboard
- User management
- Credit system overview
- Session statistics
- Rate limit monitoring

## 🚀 Performance Optimizations

### Caching
- Session caching
- Model selection caching
- Rate limit caching

### Database Optimization
- Proper indexing
- Connection pooling
- Query optimization

### Rate Limiting
- Multi-tier rate limiting
- Burst protection
- User-type specific limits

## 🧪 Testing

### Running Tests
```bash
# Install test dependencies
pip install pytest pytest-asyncio httpx

# Run tests
pytest tests/

# Run with coverage
pytest --cov=app tests/
```

### Test Structure
```
tests/
├── test_auth.py          # Authentication tests
├── test_credit.py        # Credit system tests
├── test_tools.py         # Tool functionality tests
├── test_api.py           # API endpoint tests
└── test_security.py      # Security tests
```

## 🔄 Migration from v1.0

### Key Changes
1. **Modular Architecture**: Separated concerns into dedicated modules
2. **Enhanced Security**: Added encryption, rate limiting, and input validation
3. **Improved Database**: Better models with proper relationships
4. **Advanced Tool System**: More tools with better configuration
5. **Better Error Handling**: Comprehensive error management

### Migration Steps
1. Backup your existing database
2. Install new dependencies
3. Run database migrations
4. Update environment variables
5. Test functionality

## 📈 Scalability

### Horizontal Scaling
- Stateless application design
- Database connection pooling
- Redis for session storage
- Load balancer ready

### Vertical Scaling
- Optimized database queries
- Efficient memory usage
- Async request handling
- Background task processing

## 🤝 Contributing

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Install development dependencies
4. Make your changes
5. Add tests
6. Submit a pull request

### Code Standards
- Follow PEP 8 style guide
- Add type hints
- Write comprehensive docstrings
- Include tests for new features

## 📄 License



## 🆘 Support

### Documentation
- API documentation available at `/docs`
- Interactive API explorer at `/redoc`

### Issues
- Report bugs via GitHub Issues
- Feature requests welcome
- Security issues: please email directly

### Community
- Join our Discord server
- Follow us on Twitter
- Check our blog for updates

## 🔮 Roadmap

### v2.1.0 (Q1 2024)
- [ ] Advanced analytics dashboard
- [ ] Multi-language support
- [ ] Mobile app development
- [ ] Advanced prompt templates

### v2.2.0 (Q2 2024)
- [ ] Real-time collaboration
- [ ] Advanced AI models integration
- [ ] Custom tool creation
- [ ] Enterprise features

### v3.0.0 (Q3 2024)
- [ ] AI agent marketplace
- [ ] Advanced workflow automation
- [ ] Multi-tenant architecture
- [ ] Advanced security features

---

**Built with ❤️ using FastAPI, SQLAlchemy, and modern Python practices**
