# Career Advisor - Backend API

Career Advisor is a robust Node.js and Express-based backend application that powers the Career Advisor AI platform, providing RESTful API endpoints for resume analysis, skill extraction, and integration with Gemini AI for personalized feedback.

## Features

- Upload and parse PDF resumes
- Extract and match skills against a predefined dataset
- Generate improvement tips using Gemini API
- MongoDB for data storage (if configured)
- Organized routing and middleware structure
- Error handling and logging

## Tech Stack

- Node.js
- Express.js
- Google Gemini AI API
- PDF parsing libraries
- MongoDB (optional)
- RESTful API architecture

## Prerequisites

- Node.js (LTS version recommended)
- npm (Node Package Manager)

## Getting Started

1. Clone the repository:
```bash
git clone <repository-url>
cd career-advisor-backend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory and add your environment variables:
```
PORT=5000
GEMINI_API_KEY=your_google_gemini_api_key
MONGODB_URI=your_mongodb_connection_string (optional)
```

4. Start the server:
```bash
npm start
```

The API will be available at `http://localhost:5000`

## Available Scripts

- `npm start` - Start the production server
- `npm run dev` - Start the development server with nodemon
- `npm test` - Run tests
- `npm run lint` - Run ESLint to check code quality

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/upload` | Upload a resume PDF |
| GET | `/skills` | Get matched skills |
| GET | `/tips` | Get Gemini-based improvement tips |

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Request handlers
├── middleware/       # Express middleware
├── models/           # Data models
├── routes/           # API routes
├── services/         # Business logic
├── utils/            # Helper functions
└── app.js            # Express application setup
```

## Error Handling

The API uses consistent error response formats:

```json
{
  "success": false,
  "error": "Error message",
  "code": 400
}
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
