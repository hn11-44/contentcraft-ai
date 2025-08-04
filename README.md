# ContentCraft AI - Multi-Agent Content Generation System

> **🚧 Work in Progress** - This project showcases an advanced multi-agent AI system for content creation. The frontend is minimal as the focus is on demonstrating the sophisticated backend architecture and AI orchestration capabilities.

## 🎯 Project Overview

ContentCraft AI is an enterprise-grade content generation platform that leverages a **multi-agent system architecture** to produce high-quality, SEO-optimized articles. The system demonstrates advanced AI orchestration, where specialized agents collaborate to research, write, optimize, and score content across multiple languages.

**Primary Focus**: Showcasing multi-agent system design, AI orchestration, and backend architecture capabilities.

## 🏗️ Architecture Highlights

### Multi-Agent System (CrewAI Framework)

The core innovation lies in the **sequential multi-agent workflow** where each agent has specialized responsibilities:

#### 🔍 **Research Agent** (`crew.py:48-54`)
- **Model**: Groq Llama 3.3 70B
- **Specialty**: Multilingual SEO research and competitive analysis
- **Tools**: DuckDuckGo Search integration
- **Output**: Comprehensive content briefs with search intent analysis

#### ✍️ **Writer Agent** (`crew.py:56-62`)
- **Model**: Groq DeepSeek R1 Distill 70B
- **Specialty**: Brand-aligned content creation in multiple languages
- **Capability**: Native-level writing quality across languages
- **Output**: Complete articles following structured briefs

#### ⚡ **SEO Optimizer Agent** (`crew.py:64-72`)
- **Model**: Google Gemini 2.5 Pro
- **Specialty**: Technical SEO optimization and internal linking
- **Tools**: Internal link discovery and strategic placement
- **Output**: Fully optimized content with metadata

#### 📊 **SEO Scorer Agent** (`crew.py:73-81`)
- **Model**: Google Gemini 2.5 Flash
- **Specialty**: Content analysis and scoring
- **Tools**: On-page SEO analysis, keyword density checker
- **Output**: Performance scores and improvement recommendations

### Advanced Features Demonstrated

#### 🧠 **Multi-LLM Strategy**
- **Strategic Model Selection**: Different agents use optimized models for their tasks
- **Cost Optimization**: Balancing performance and cost across the pipeline
- **Rate Limiting**: Proper API management for production scenarios

#### 🛠️ **Custom Tool Development** (`tools/custom_tool.py`)
- Built custom CrewAI tools for specific business logic
- Demonstrates extensibility and integration capabilities
- Production-ready database integration patterns

#### 🌐 **Production-Ready API** (`api/`)
- **FastAPI backend** with async/await patterns
- **JWT authentication** and user management
- **PostgreSQL integration** with SQLAlchemy ORM
- **RESTful design** with proper error handling
- **CORS configuration** for frontend integration

#### 🏛️ **Database Architecture**
- **Hierarchical content organization**: Users → Pillars → Clusters → Articles
- **Brand configuration management** for personalized content
- **Article lifecycle tracking** and metadata storage
- **Async database operations** for scalability

## 🔧 Technical Stack

### Backend (Primary Focus)
- **Multi-Agent Framework**: CrewAI
- **API Framework**: FastAPI
- **Database**: PostgreSQL with async SQLAlchemy
- **Authentication**: JWT with passlib
- **AI Models**: 
  - Groq (Llama, DeepSeek, Mistral)
  - Google Gemini (Pro 2.5, Flash)
- **Tools**: Custom CrewAI tools, DuckDuckGo integration

### Frontend (Minimal Implementation)
- **Framework**: Next.js 14
- **Styling**: Tailwind CSS
- **UI Components**: Shadcn/ui
- **State Management**: React Context

## 📁 Project Structure

```
ContentCraftApp/
├── contentcraft_ai/                 # Core AI System
│   ├── src/contentcraft_ai/
│   │   ├── config/
│   │   │   ├── agents.yaml          # Agent definitions
│   │   │   └── tasks.yaml           # Task configurations
│   │   ├── crew.py                  # Multi-agent orchestration
│   │   ├── tools/                   # Custom CrewAI tools
│   │   └── api/                     # FastAPI backend
│   │       ├── main_api.py          # API entry point
│   │       ├── models.py            # Database models
│   │       ├── schemas.py           # Pydantic schemas
│   │       ├── auth.py              # JWT authentication
│   │       └── v1/endpoints.py      # API endpoints
├── contentcraft-frontend/           # Next.js frontend (minimal)
└── README.md                        # This file
```

## 🚀 Key Capabilities Demonstrated

### 1. **Agent Orchestration**
- Sequential task processing with context passing
- Dynamic input handling across agents
- Error handling and fallback mechanisms

### 2. **Production Scalability**
- Async database operations
- Rate limiting and API quotas
- Multi-model load balancing

### 3. **Enterprise Features**
- Multi-tenant architecture
- Brand customization per user
- Comprehensive content lifecycle management

### 4. **AI Integration Expertise**
- Multiple LLM provider integration (Groq, Google)
- Custom tool development for business logic
- Prompt engineering and output parsing

## 🎯 What This Project Showcases

### For Potential Employers:

#### **AI/ML Engineering Skills**
- Multi-agent system design and implementation
- LLM integration and optimization
- Custom tool development for AI frameworks
- Production-ready AI pipeline architecture

#### **Backend Development Expertise**
- FastAPI and async Python development
- Database design and ORM implementation
- Authentication and security best practices
- RESTful API design and documentation

#### **System Architecture**
- Microservices-ready design patterns
- Scalable database architecture
- Multi-provider AI integration
- Production deployment considerations

#### **Problem-Solving Approach**
- Complex workflow orchestration
- Business logic abstraction
- Error handling and resilience
- Performance optimization strategies

## 📋 Current Status

- ✅ Multi-agent system fully implemented
- ✅ API backend with authentication
- ✅ Database integration and models
- ✅ Custom tools and integrations
- 🚧 Frontend implementation (minimal by design)
- 🚧 Deployment configuration
- 🚧 Comprehensive testing suite

## 🔑 Key Differentiators

1. **Advanced AI Orchestration**: Goes beyond simple LLM calls to demonstrate complex multi-agent workflows
2. **Production Architecture**: Built with scalability, maintainability, and enterprise needs in mind
3. **Multi-Provider Integration**: Showcases ability to work with different AI providers and optimize for specific use cases
4. **Custom Tooling**: Demonstrates ability to extend AI frameworks with business-specific functionality

---

**Note**: This project prioritizes showcasing backend architecture and AI system design over frontend polish. The multi-agent system, API design, and database architecture represent the core value proposition and technical expertise demonstrated.