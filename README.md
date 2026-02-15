# Web Code Snippet Miner 💎

A high-compute scraping project that extracts, categorizes, and semantically indexes code snippets from across the web. Build a developer knowledge graph with intelligent search capabilities.

## 🎯 Project Overview

**Goal**: Create a comprehensive searchable database of code snippets from:
- Stack Overflow and developer forums
- GitHub Gists and READMEs
- Technical blogs and documentation
- Tutorial sites and code repositories

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                   Web Code Snippet Miner                     │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────┐   │
│  │   Scraper   │  │  Parser &  │  │   Semantic      │   │
│  │   Engine    │──▶│  Extractor │──▶│   Indexer       │   │
│  └─────────────┘  └─────────────┘  └─────────────────┘   │
│                   └─────────────┘  ┌─────────────────┐   │
│  ┌─────────────┐  ┌─────────────┐  │   Search API   │   │
│  │  Web Crawler│  │  Vector DB  │  │   (FastAPI)    │   │
│  │  (Custom)  │  │ (Qdrant)   │  └─────────────────┘   │
│  └─────────────┘  └─────────────┘                          │
└─────────────────────────────────────────────────────────────┘
```

## 📊 Data Sources

- **Stack Overflow**: Questions, answers, code blocks
- **GitHub Gists**: Public gists and their code
- **Dev.to & Hashnode**: Technical articles with code
- **Medium & Blogs**: Developer tutorials
- **Documentation**: Code examples from official docs

## 🔧 Tech Stack

- **Language**: Python
- **Scraping**: Playwright, Scrapy
- **Code Parsing**: Tree-sitter, AST analysis
- **Vector Store**: Qdrant / Pinecone
- **Embeddings**: CodeBERT, UnixCoder
- **API**: FastAPI
- **Queue**: Redis + Celery

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/yksanjo/web-code-snippet-miner.git
cd web-code-snippet-miner

# Install dependencies
pip install -r requirements.txt

# Set up environment
cp .env.example .env

# Run the miner
python src/miner/stackoverflow_miner.py

# Start search API
uvicorn src.api.main:app --reload
```

## 📈 Features

- [ ] Multi-source web scraping
- [ ] Code block extraction and parsing
- [ ] Language detection (50+ languages)
- [ ] Semantic embeddings generation
- [ ] Similarity search
- [ ] Code deduplication
- [ ] Usage analytics

## 📊 Project Phases

### Phase 1: Source Collection
- Stack Overflow scraper
- GitHub Gists miner
- Blog aggregator

### Phase 2: Extraction Pipeline
- Code block detection
- Language identification
- AST-based normalization

### Phase 3: Semantic Indexing
- Code embeddings
- Vector storage
- Similarity search

### Phase 4: API & UI
- REST API
- Search interface
- Usage analytics

## 📝 License

MIT License - See [LICENSE](LICENSE) for details.

## 👤 Author

Yoshi Kondo - [@yksanjo](https://github.com/yksanjo)

---

🔍 Search smarter with mined code snippets!
