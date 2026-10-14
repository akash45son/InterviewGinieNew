
#InterviewGinie: AI-Powered Interview Strategy Generator

An intelligent platform that uses Google's Generative AI to create personalized interview preparation strategies by analyzing job descriptions and candidate profiles.

## 🎯 Features

- **AI-Powered Analysis**: Leverages Google Generative AI to understand job requirements and candidate profiles
- **Technical & Behavioral Questions**: Generates relevant interview questions with model answers and interviewer intentions
- **Skill Gap Analysis**: Identifies areas for improvement and their severity levels
- **Personalized Preparation Plan**: Creates a 7-day customized roadmap based on the job requirements
- **Match Score**: Calculates how well the candidate's profile matches the job description
- **Resume Generation**: Creates an AI-optimized resume tailored to the specific job position
- **PDF Download**: Generates and downloads the customized resume as a PDF file
- **User Authentication**: Secure login and registration system
- **Interview History**: Maintains a history of all generated interview reports

## 🏗️ Project Structure

```
YT-GenAI/
├── Frontend/                 # React + Vite + SCSS
│   ├── src/
│   │   ├── features/
│   │   │   ├── auth/        # Authentication pages and hooks
│   │   │   └── interview/   # Interview planning pages
│   │   └── style/
│   ├── .env.example
│   ├── package.json
│   └── vite.config.js
│
└── Backend/                  # Node.js + Express + MongoDB
    ├── src/
    │   ├── controllers/      # Route handlers
    │   ├── models/           # MongoDB schemas
    │   ├── routes/           # API endpoints
    │   ├── middlewares/      # Custom middleware
    │   ├── services/         # Business logic
    │   └── config/           # Configuration files
    ├── .env.example
    ├── .gitignore
    ├── package.json
    └── server.js
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- MongoDB Atlas account (free tier available)
- Google Generative AI API key

### Backend Setup

1. Navigate to the Backend directory:
```bash
cd Backend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file by copying `.env.example`:
```bash
cp .env.example .env
```

4. Fill in your environment variables in `.env`:
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET_KEY=your_jwt_secret_key
GOOGLE_GENAI_API_KEY=your_google_genai_api_key
```

5. Start the development server:
```bash
npm run dev
```

The backend server will run on `http://localhost:3000`

### Frontend Setup

1. Open a new terminal and navigate to the Frontend directory:
```bash
cd Frontend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file by copying `.env.example`:
```bash
cp .env.example .env
```

4. Start the development server:
```bash
npm run dev
```

The frontend will run on `http://localhost:5173`

## 📋 API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/logout` - Logout user
- `GET /api/auth/get-me` - Get current user info

### Interview Reports
- `POST /api/interview/` - Generate new interview report
- `GET /api/interview/` - Get all interview reports
- `GET /api/interview/report/:interviewId` - Get specific interview report
- `POST /api/interview/resume/pdf/:interviewReportId` - Generate resume PDF

## 🛠️ Tech Stack

### Frontend
- **React 19** - UI library
- **React Router 7** - Client-side routing
- **Vite** - Build tool and dev server
- **SCSS** - Styling
- **Axios** - HTTP client

### Backend
- **Node.js & Express** - Web framework
- **MongoDB & Mongoose** - Database
- **Google Generative AI** - AI model for report generation
- **Puppeteer** - PDF generation
- **JWT** - Authentication tokens
- **Bcrypt** - Password hashing
- **Multer** - File upload handling
- **Zod** - Schema validation

## 🔐 Environment Variables

### Backend (.env)
```
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/database
JWT_SECRET_KEY=your_secret_key
GOOGLE_GENAI_API_KEY=your_api_key
```

### Frontend (.env)
```
VITE_API_URL=http://localhost:3000
```

## 📝 Usage

1. **Register/Login**: Create an account or login to your existing account
2. **Create Interview Plan**: 
   - Paste the job description
   - Upload your resume or provide a self-description
   - Click "Generate My Interview Strategy"
3. **View Results**: Explore technical questions, behavioral questions, skill gaps, and preparation roadmap
4. **Download Resume**: Click "Download PDF" to get your AI-optimized resume

## 🎨 Key Features Explained

- **Match Score**: A percentage score (0-100) indicating how well your profile matches the job requirements
- **Technical Questions**: Interview questions focused on technical skills with model answers
- **Behavioral Questions**: Questions about soft skills and past experiences with suggested responses
- **Skill Gaps**: Areas where you might need improvement, priority-ranked by severity
- **7-Day Roadmap**: Daily preparation plan with specific focus areas and tasks

## 📦 Build for Production

### Frontend
```bash
cd Frontend
npm run build
npm run preview
```

### Backend
```bash
cd Backend
npm start
```

## 🐛 Troubleshooting

### MongoDB Connection Issues
- Ensure your MongoDB Atlas account is active
- Check IP whitelist in MongoDB Atlas (allow 0.0.0.0/0 for development)
- Verify the connection string in `.env`

### Google Generative AI Issues
- Ensure you have a valid Google Generative AI API key
- Check API quotas and rate limits

### PDF Generation Issues
- Ensure Puppeteer is properly installed
- On Linux, you may need to install additional dependencies

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the ISC License - see the LICENSE file for details.

## 👨‍💼 Author

Created as an intelligent interview preparation platform powered by AI.

## 🙏 Acknowledgments

- Google Generative AI for powering the report generation
- MongoDB for the database
- React and Node.js communities for amazing frameworks

---

**Happy Interviewing! 🎯**
