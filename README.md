# 🎨 AI 3D Forge - Intelligent 3D Asset Generation Platform

[![GitHub stars](https://img.shields.io/github/stars/yourusername/ai-3d-forge-platform)](https://github.com/yourusername/ai-3d-forge-platform/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/yourusername/ai-3d-forge-platform)](https://github.com/yourusername/ai-3d-forge-platform/network)
[![GitHub issues](https://img.shields.io/github/issues/yourusername/ai-3d-forge-platform)](https://github.com/yourusername/ai-3d-forge-platform/issues)
[![GitHub license](https://img.shields.io/github/license/yourusername/ai-3d-forge-platform)](https://github.com/yourusername/ai-3d-forge-platform/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

> **Transform Imagination into 3D Reality - Just Describe, We Create!** 🚀

## 🌟 Overview

AI 3D Forge is a cutting-edge web platform that leverages Google's Gemini AI to generate professional 3D assets from simple text descriptions or hand-drawn sketches. Built for game developers, architects, designers, and 3D enthusiasts, this platform makes 3D content creation accessible to everyone - no 3D modeling experience required!

![AI 3D Forge Banner](https://via.placeholder.com/1200x400/6C63FF/FFFFFF?text=AI+3D+Forge)

## ✨ Features

### 🎯 Core Features
- **📝 Text-to-3D**: Convert natural language descriptions into 3D models
- **✏️ Sketch-to-3D**: Upload hand-drawn sketches and watch them become 3D
- **🎨 Texture Generation**: Create realistic textures from text prompts
- **🎬 Animation Creation**: Generate basic animations for your 3D models
- **📦 Multiple Formats**: Export in GLB, OBJ, STL, FBX, and more
- **🔄 Real-time Preview**: Interactive 3D viewer with rotation and zoom

### 🎮 User Experience
- **💎 Beautiful UI**: Modern glassmorphism design with dark/light themes
- **📱 Responsive**: Works seamlessly on desktop, tablet, and mobile
- **⚡ Fast Generation**: Optimized for CPU-only systems
- **📊 Asset Library**: Smart organization and search of generated assets
- **📈 History Tracking**: Keep track of all your generations

### 🔒 Security & Performance
- **🔐 JWT Authentication**: Secure user authentication
- **🛡️ Rate Limiting**: Prevent API abuse
- **💾 Caching**: Optimized performance with Redis cache
- **📊 Analytics**: Track usage and performance metrics

## 🏗️ Architecture

### System Architecture


### Technology Stack
| Component | Technology | Version | Purpose |
|-----------|-----------|---------|---------|
| **Frontend** | React | 18.2.0 | UI Framework |
| | Vite | 4.0.0 | Build Tool |
| | Tailwind CSS | 3.3.0 | Styling |
| | Three.js | 0.155.0 | 3D Rendering |
| | Framer Motion | 10.0.0 | Animations |
| | React Query | 4.29.0 | State Management |
| **Backend** | FastAPI | 0.100.0 | Web Framework |
| | SQLAlchemy | 2.0.0 | ORM |
| | Alembic | 1.11.0 | Migrations |
| | Celery | 5.3.0 | Task Queue |
| **AI** | Gemini API | Latest | Text-to-3D |
| | Open3D | 0.17.0 | 3D Processing |
| | PyTorch | 2.0.0 | ML (CPU) |
| **Database** | SQLite | 3.0 | Development |
| | PostgreSQL | 15.0 | Production |

## 🚀 Quick Start

### Prerequisites
- **Node.js** 18.0 or higher
- **Python** 3.9 or higher
- **Git** (for cloning)
- **Gemini API Key** (from Google AI Studio)

### Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/ai-3d-forge-platform.git
cd ai-3d-forge-platform

# Navigate to backend
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
cp .env.example .env

# Edit .env with your Gemini API key
# GEMINI_API_KEY=your_api_key_here

# Initialize database
cd database
sqlite3 data.db < schema.sql
cd ..

# Run migrations
alembic upgrade head

# Start backend server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Open new terminal
cd frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env

# Start development server
npm run dev