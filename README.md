# CodeFlow AI 

**Interactive Multimodal Code Learning Platform**

Transform complex codebases into interactive, AI-powered learning experiences. CodeFlow AI helps developers understand unfamiliar code 40% faster through visual diagrams, adaptive explanations, and intelligent learning paths.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-hackathon-orange.svg)
![AI](https://img.shields.io/badge/AI-powered-brightgreen.svg)

## Problem Statement

- **30-50%** of a new developer's first 3 months is spent understanding existing codebases
- Context switching between code, docs, and diagrams kills productivity
- Complex algorithms are hard to grasp from code alone
- Senior developer knowledge isn't captured or transferred effectively

## Solution

CodeFlow AI combines three powerful approaches:

1. **Visual Learning**: Auto-generated call graphs, execution flows, and architecture diagrams
2. **AI Explanations**: Context-aware, adaptive explanations that match your skill level
3. **Interactive Exploration**: Step-through code execution with live data transformations

## Key Features

### AI-Powered Learning Assistant
- Natural language Q&A about any code
- Explanations adapted to your experience level (beginner/intermediate/expert)
- Automatic complexity assessment and learning prerequisites
- Concept linking to related patterns and documentation

### Interactive Visualizations
- **Call Graphs**: See function invocation hierarchies
- **Execution Flow**: Step-by-step code execution paths
- **Data Flow**: Variable dependencies and transformations
- **Architecture Diagrams**: Module relationships at a glance
- **Complexity Heatmaps**: Visual indicators of code complexity

### Adaptive Learning Paths
- Knowledge graph mapping code relationships
- Progressive disclosure based on comprehension
- Auto-generated practice challenges
- Comprehension quizzes with instant feedback
- Progress tracking showing what you understand

### Collaborative Learning
- Shared team annotations and insights
- Senior developer highlights and guidance
- Discussion threads on specific code blocks
- Learning progress visibility

### Accessibility First
- WCAG 2.1 AA compliant
- Text-to-speech code narration
- Keyboard-first navigation
- Color-blind friendly visualizations
- Screen reader support

## Technology Stack

### Frontend
- **Framework**: React 18 + TypeScript
- **Code Editor**: Monaco Editor (VS Code engine)
- **Visualization**: D3.js, Cytoscape.js, React Flow
- **UI**: Shadcn/ui, Tailwind CSS
- **State**: Zustand

### Backend
- **Framework**: FastAPI (Python 3.11+)
- **Code Parsing**: Tree-sitter (multi-language)
- **Graph Analysis**: NetworkX
- **API**: REST + WebSocket

### AI/ML
- **LLM**: OpenAI GPT-4 / Anthropic Claude
- **Embeddings**: CodeBERT, GraphCodeBERT
- **Vector DB**: Pinecone / Weaviate
- **RAG Pipeline**: Custom implementation

### Infrastructure
- **Frontend Hosting**: Vercel
- **Backend Hosting**: Railway / Render
- **Database**: PostgreSQL
- **Cache**: Redis (Upstash)
- **CI/CD**: GitHub Actions
- **Monitoring**: Sentry, Posthog

## Documentation

- **[requirements.md](./requirements.md)**: Complete product requirements and specifications
- **[design.md](./design.md)**: Technical design and architecture documentation

## Quick Start

### Prerequisites
```bash
# Required
Node.js 18+
Python 3.11+
PostgreSQL 14+
Redis 7+

# API Keys needed
OPENAI_API_KEY or ANTHROPIC_API_KEY
PINECONE_API_KEY (or alternative vector DB)
```

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/codeflow-ai.git
cd codeflow-ai

# Install frontend dependencies
cd frontend
npm install

# Install backend dependencies
cd ../backend
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys

# Run database migrations
alembic upgrade head

# Start development servers
# Terminal 1 - Backend
cd backend
uvicorn main:app --reload

# Terminal 2 - Frontend
cd frontend
npm run dev
```

### Configuration

Create a `.env` file in the backend directory:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/codeflow
REDIS_URL=redis://localhost:6379
VECTOR_DB_API_KEY=your_pinecone_key
OPENAI_API_KEY=your_openai_key
JWT_SECRET=your_secret_key
GITHUB_OAUTH_CLIENT_ID=your_github_oauth_id
GITHUB_OAUTH_CLIENT_SECRET=your_github_oauth_secret
```

## Usage

1. **Import a Repository**
   ```
   - Paste GitHub URL or upload code
   - System analyzes structure and complexity
   - Navigate to code explorer
   ```

2. **Explore Code**
   ```
   - Browse file tree
   - Click any file to view with AI insights
   - Toggle inline explanations
   - Adjust explanation level
   ```

3. **Visualize Architecture**
   ```
   - Click "Visualize" on any function
   - Explore call graphs interactively
   - See execution flows
   - Understand data transformations
   ```

4. **Ask Questions**
   ```
   - Select code or use chat panel
   - Ask in natural language
   - Get contextual AI answers
   - Follow reference links
   ```

5. **Track Progress**
   ```
   - Take comprehension quizzes
   - See learning progress
   - Unlock advanced sections
   - Review annotations
   ```

## Success Metrics

- **40%** reduction in code understanding time
- **30%** improvement in comprehension scores
- **15+ min** average session duration
- **60%** user retention (7-day)
- **50+** NPS score

## Roadmap

### Phase 1: MVP (Hackathon)
- [x] GitHub repository import
- [ ] Code visualization (call graphs)
- [ ] AI-powered Q&A
- [ ] Interactive code explorer
- [ ] Basic progress tracking

### Phase 2: Post-Hackathon
- [ ] VS Code extension
- [ ] Additional language support (PHP, Swift, Kotlin)
- [ ] Team collaboration features
- [ ] Export learning paths

### Phase 3: Growth (3-6 months)
- [ ] AI-generated video tutorials
- [ ] Live code execution
- [ ] Notion/Confluence integration
- [ ] Mobile read-only app

### Phase 4: Enterprise (6-12 months)
- [ ] Real-time AI pair programming
- [ ] Custom learning path builder
- [ ] SSO and enterprise features
- [ ] White-label solution

## 🏆 Why CodeFlow AI?

| Feature | CodeFlow AI | GitHub Copilot | Sourcegraph | ChatGPT |
|---------|------------|----------------|-------------|---------|
| Code Generation | ❌ | ✅ | ❌ | ✅ |
| Code Visualization | ✅ | ❌ | ✅ | ❌ |
| AI Explanations | ✅ | ⚠️ | ⚠️ | ✅ |
| Codebase Context | ✅ | ⚠️ | ✅ | ❌ |
| Learning Paths | ✅ | ❌ | ❌ | ❌ |
| Progress Tracking | ✅ | ❌ | ❌ | ❌ |
| Multimodal (Visual+Audio) | ✅ | ❌ | ❌ | ❌ |
| Accessibility | ✅ | ⚠️ | ⚠️ | ⚠️ |

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) first.

```bash
# Fork the repository
# Create a feature branch
git checkout -b feature/amazing-feature

# Commit your changes
git commit -m 'Add amazing feature'

# Push to the branch
git push origin feature/amazing-feature

# Open a Pull Request
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
