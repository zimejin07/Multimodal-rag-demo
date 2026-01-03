# AI Assistant Platform with RAG Technology

A Next.js 15 application implementing Retrieval-Augmented Generation (RAG) with multimodal inputs. The system integrates client-side image classification with vector-based document retrieval to generate context-aware responses.

# The platform combines:

Image classification via TensorFlow.js

Semantic document retrieval via Pinecone

LLM orchestration via LangChain and OpenAI

Image-derived labels are used to enrich retrieval queries, improving relevance and grounding of generated responses.

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm/yarn/pnpm
- OpenAI API key
- Pinecone account and API key

### Environment Setup
Create a `.env.local` file in the root directory:

```bash
# OpenAI Configuration
OPENAI_API_KEY=your_openai_api_key_here

# Pinecone Configuration
PINECONE_API_KEY=your_pinecone_api_key_here
PINECONE_INDEX=your_pinecone_index_name
```

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ai-assistant-platform
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up your vector database**
   ```bash
   # Run the Pinecone setup script
   npx tsx scripts/setup-pinecone.ts
   ```

4. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Access the application**
   Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🌐 Deployment

### Vercel (Recommended)
1. Connect your repository to [Vercel](https://vercel.com)
2. Add your environment variables in the Vercel dashboard
3. Deploy with automatic CI/CD

### Other Platforms
This Next.js application can be deployed on any platform supporting Node.js:
- Railway
- Render
- AWS Amplify
- Netlify (with serverless functions)

## 📚 Learn More

### Documentation
- [Next.js Documentation](https://nextjs.org/docs) - Next.js features and API
- [LangChain Documentation](https://docs.langchain.com/) - RAG and LLM orchestration
- [Pinecone Documentation](https://docs.pinecone.io/) - Vector database setup
- [OpenAI API Documentation](https://platform.openai.com/docs) - AI model integration

### Key Concepts
- **RAG (Retrieval-Augmented Generation)**: Enhances AI responses with relevant document retrieval
- **Vector Embeddings**: Mathematical representations enabling semantic search
- **Semantic Search**: Finding relevant information based on meaning, not just keywords

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔍 Troubleshooting

### Common Issues
- **Model Loading**: Ensure stable internet connection for initial TensorFlow.js model download
- **Pinecone Connection**: Verify API keys and index names in environment variables
- **Upload Failures**: Check file sizes (max 10MB) and supported formats (PDF, TXT, DOCX, MD)
- **Memory Issues**: Refresh page if experiencing performance degradation

### Support
For issues and questions:
1. Check the [Issues](../../issues) page
2. Review documentation links above
3. Create a new issue with detailed reproduction steps

---

Deployment

Designed for Vercel and compatible with any Node.js runtime supporting server functions.

License

MIT
