# AGRISAHAYAK
an ai driven website for agricultural purposes 
AgriSahayak - AI-Powered Agricultural Assistant
A comprehensive web application that provides AI-powered agricultural assistance to farmers, featuring multilingual support, weather data, crop recommendations, and interactive chat functionality.

Features
🤖 AI-powered agricultural chatbot using Google Gemini
🌍 Multilingual support (English, Hindi, Tamil, Telugu, and more)
🌤️ Real-time weather data integration
📹 YouTube video recommendations for farming techniques
🎤 Voice-to-text and text-to-speech capabilities
📧 Email verification and password reset functionality
📱 Responsive design for mobile and desktop
Tech Stack
Backend: Flask, Python
Database: PostgreSQL (Supabase)
AI: Google Gemini API
Authentication: Flask-Login
Email: Flask-Mail
Deployment: Vercel
Local Development
Clone the repository
Install dependencies: pip install -r requirements.txt
Set up environment variables (see .env.example)
Run the application: python main.py
Environment Variables
Create a .env file with the following variables:

SECRET_KEY=your_secret_key
DATABASE_URL=your_supabase_database_url
MAIL_USERNAME=your_email@gmail.com
MAIL_PASSWORD=your_email_app_password
GEMINI_API_KEY=your_gemini_api_key
YOUTUBE_API_KEY=your_youtube_api_key
WEATHER_API_KEY=your_weather_api_key
BASE_URL=http://localhost:5000
Vercel Deployment
Prerequisites
Supabase Database: Set up a PostgreSQL database on Supabase
API Keys: Obtain API keys for Gemini, YouTube, and Weather APIs
Email Service: Configure Gmail with app password
Deployment Steps
Connect to Vercel:

Install Vercel CLI: npm i -g vercel
Login: vercel login
Deploy: vercel
Set Environment Variables in Vercel:

Go to your Vercel project dashboard
Navigate to Settings > Environment Variables
Add all required environment variables
Database Configuration:

Ensure your Supabase DATABASE_URL is properly formatted
The URL should be: postgresql://username:password@host:port/database
If using Supabase, the URL format is: postgresql://postgres:[password]@[host]:5432/postgres
Troubleshooting
Database Connection Issues
If you encounter database connection errors:

Check DATABASE_URL format: Ensure it starts with postgresql://
Verify Supabase credentials: Check username, password, and host
Test connection: Use a database client to verify connectivity
Check Vercel logs: Monitor deployment logs for specific errors
Common Error: "could not translate host name"
This error occurs when the DATABASE_URL is malformed. The application now includes automatic URL parsing and fallback mechanisms.

Health Check
After deployment, test the health endpoint:

https://your-app.vercel.app/health
This will show the application status and database connection state.

API Endpoints
GET / - Home page
GET /health - Health check endpoint
POST /login - User login
POST /register - User registration
GET /dashboard - User dashboard (requires authentication)
POST /api/send_message - Send chat message
POST /api/get_crop_recommendations - Get crop recommendations
POST /api/translate - Translate text
POST /api/text_to_speech - Convert text to speech
POST /api/speech_to_text - Convert speech to text
Contributing
Fork the repository
Create a feature branch
Make your changes
Test thoroughly
Submit a pull request
