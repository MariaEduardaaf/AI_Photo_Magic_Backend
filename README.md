# Morphix - AI Photo Transformation API

A powerful Node.js/Express backend API that transforms photos using artificial intelligence. Upload your photos and watch them transform into Pixar-style avatars, age progressions, anime characters, classical paintings, and more.

## Features

- **9 AI Transformations** - Multiple artistic and realistic transformation styles
- **Dual AI Provider Support** - Seamlessly switch between OpenAI DALL-E 3 and Replicate
- **Mobile-Ready** - CORS configured for Flutter/React Native integration
- **Cloud Optimized** - Memory-based file storage for container deployments
- **Production Ready** - Deployed on Railway platform

## Available Transformations

| Transformation | Description |
|----------------|-------------|
| Pixar Avatar | 3D Pixar/Disney-style character |
| Age Progression | See yourself 20 years older |
| Age Regression | See yourself as a child |
| Perfect Pet | Generate a dog matching your personality |
| Perfect Match | Generate an ideal romantic partner |
| Anime Style | Japanese anime character conversion |
| Classical Painting | Renaissance masterpiece portrait |
| Cartoon Style | Fun cartoon character version |
| Family Photo | Generate family photo with child |

## Tech Stack

- **Runtime**: Node.js 18+
- **Framework**: Express.js
- **File Upload**: Multer (memory storage)
- **AI Providers**: OpenAI DALL-E 3, Replicate SDXL
- **HTTP Client**: Axios

## API Endpoints

**Health Check**
- GET /
- GET /health

**Generate Image**
- POST /generate-image (multipart/form-data)
  - images: Image files (max 2, max 10MB each)
  - transformationType: string (optional)

**List Transformations**
- GET /transformations

## Installation

1. Clone the repository
2. Run: npm install
3. Copy .env.example to .env and add your API keys
4. Run: npm run dev (development) or npm start (production)

## Environment Variables

| Variable | Description |
|----------|-------------|
| PORT | Server port (default: 3000) |
| OPENAI_API_KEY | OpenAI API key |
| REPLICATE_API_TOKEN | Replicate API token |
| AI_PROVIDER | openai or replicate |
| MAX_FILE_SIZE | Max upload size in bytes |
| DEMO_MODE | Enable demo mode |

## Deployment

### Railway
1. Connect your GitHub repository to Railway
2. Add environment variables in Railway dashboard
3. Deploy

Works with any Node.js hosting platform (Heroku, Render, DigitalOcean, etc.)

## License

MIT
