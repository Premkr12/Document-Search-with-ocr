📄 DocuSearch – OCR Document Management & Search System

A full-stack MERN application for uploading documents, extracting text using Tesseract OCR, storing results in MongoDB, and enabling fast keyword search with highlighted results.
Includes authentication, drag & drop upload, search highlighting, document actions, and a polished React dashboard UI.

🚀 Features
🔐 Authentication

User Registration & Login (JWT based)

Protected Dashboard Routes

Auth Context with persistent login

📤 Document Upload

Drag & Drop upload UI

Upload using Multer

OCR extraction via Tesseract.js

Stores extracted text + filename + timestamps

🔍 Smart Search

Search across all extracted OCR results

Keyword highlighting in search preview

Regex-based flexible search

📚 Dashboard

View all uploaded documents

Modal preview

Delete document

Reprocess document (mock reprocess)

⚙️ Backend

Express.js REST API

MongoDB Atlas / Local MongoDB

Models: User, OCRResult, Document

🛠️ Tech Stack
Frontend

React.js

Tailwind CSS

Axios

React Router

Context API (auth)

Backend

Node.js / Express.js

Multer (file uploads)

Tesseract.js (OCR)

JWT Auth

MongoDB + Mongoose

📂 Project Structure
/backend
 ├── controllers
 ├── models
 ├── routes
 ├── server.js
 ├── db.js

/frontend
 ├── components
 ├── pages
 ├── layouts
 ├── context
 ├── App.js
 ├── index.js

⚙️ Setup Instructions
1️⃣ Clone the Repository
git clone <your-repo-url>
cd project-folder

🗄️ Backend Setup
📌 Go to backend folder
cd backend

📌 Install dependencies
npm install

📌 Create .env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000

📌 Start server
npm start


Your backend will run on:
👉 http://localhost:5000

🖥️ Frontend Setup
📌 Go to frontend folder
cd frontend

📌 Install dependencies
npm install

📌 Start frontend
npm start


Runs on:
👉 http://localhost:3000

🔌 API Endpoints
Auth Routes
Method	Endpoint	Description
POST	/api/users/register	Register a new user
POST	/api/users/login	Login & get JWT
OCR Routes
Method	Endpoint	Description
POST	/api/ocr/upload	Upload image & extract text
POST	/api/ocr/search	Search extracted text
GET	/api/ocr/list	List all documents
DELETE	/api/ocr/delete/:id	Delete document
PUT	/api/ocr/reprocess/:id	Reprocess OCR
🧪 How It Works
1. User uploads a document → backend saves it via Multer
2. Tesseract.js runs OCR and extracts text
3. Text is saved into MongoDB under OCRResult
4. Search endpoint does regex matching
5. React highlights the matched keywords dynamically
6. Dashboard allows view, delete, reprocess
🎯 Screens / UI Features
Dashboard

All documents listed

Preview modal

Reprocess/Delete modals

Upload Page

Drag & drop

Live visual feedback

File preview

Search Page

Highlight matched text

Responsive grid results

Auth Pages

Gradient design

Login / Signup UI

📦 Deployment Guide
Backend (Render, Railway, etc.)

Add env vars

Set build command: npm install

Start command: node server.js

Frontend (Vercel)

Set environment: REACT_APP_API_URL

Build command:

npm run build


Output:

build

🤝 Contributing

Feel free to contribute by opening issues or PRs.

📜 License

This project is open-source and free to use.
