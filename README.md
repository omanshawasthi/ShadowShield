# 🛡️ ShadowShield

<div align="center">

![ShadowShield Logo](https://img.shields.io/badge/ShadowShield-Secure%20Communication-blue?style=for-the-badge)

**A comprehensive secure file sharing and communication platform with advanced security features**

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![Node.js](https://img.shields.io/badge/Node.js-v16+-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5+-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-7+-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/)

</div>

---

## 📖 Table of Contents

- [About](#-about)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Configuration](#environment-configuration)
  - [Running the Application](#running-the-application)
- [Project Structure](#-project-structure)
- [API Documentation](#-api-documentation)
- [Security Features](#-security-features)
- [Usage Guide](#-usage-guide)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [Roadmap](#-roadmap)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 About

**ShadowShield** is a modern, security-focused file sharing and communication platform built to protect sensitive data through multiple layers of security. Developed as a hackathon project, it combines secure file uploads, encrypted messaging, activity tracking, and AI-powered security monitoring into a seamless user experience.

The platform is designed for teams and individuals who need to share files securely with features like:
- **Time-limited access** to shared files
- **One-time access links** that self-destruct after use
- **Real-time security monitoring** with AI analysis
- **Encrypted file storage** and secure messaging
- **Comprehensive activity logging** and audit trails

---

## ✨ Key Features

### 🔐 Security & Authentication
- **JWT-based authentication** with secure token management
- **Rate limiting** to prevent brute-force attacks
- **CORS protection** for cross-origin security
- **Cookie-based session management**
- **AI-powered security event monitoring**

### 📁 File Management
- **Secure file upload** with validation
- **One-time access link generation** with expiration
- **Time-limited file access** controls
- **File encryption** at rest
- **Automatic cleanup** of expired files
- **User-specific file organization**

### 💬 Secure Messaging
- **Encrypted message storage**
- **User-to-user messaging** system
- **Message history** and retrieval
- **Real-time message composer** interface

### 📊 Monitoring & Analytics
- **Real-time activity feed**
- **Security event logging**
- **User activity tracking**
- **Dashboard with quick actions**
- **Notification system**

### 🎨 Modern UI/UX
- **Responsive design** with Tailwind CSS
- **Dark theme** interface
- **Component library** with Radix UI
- **Smooth animations** with Framer Motion
- **Accessible** components

---

## 🚀 Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| **React 18** | UI framework |
| **TypeScript** | Type-safe development |
| **Vite** | Build tool and dev server |
| **React Router** | Client-side routing |
| **Tailwind CSS** | Utility-first styling |
| **Radix UI** | Accessible component primitives |
| **Framer Motion** | Animation library |
| **Axios** | HTTP client |
| **Lucide React** | Icon library |

### Backend
| Technology | Purpose |
|------------|---------|
| **Node.js** | Runtime environment |
| **Express.js** | Web framework |
| **MongoDB** | NoSQL database |
| **Mongoose** | ODM for MongoDB |
| **JWT** | Authentication tokens |
| **bcryptjs** | Password hashing |
| **express-fileupload** | File upload handling |
| **express-rate-limit** | Rate limiting |
| **Morgan** | HTTP request logging |

### DevOps & Tools
- **nodemon** - Development auto-restart
- **dotenv** - Environment variable management
- **ESLint** - Code linting
- **CORS** - Cross-origin resource sharing

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                         Frontend (React)                     │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────────┐  │
│  │  Auth Pages │  │  Dashboard   │  │  File Management │  │
│  └─────────────┘  └──────────────┘  └──────────────────┘  │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────────┐  │
│  │  Messaging  │  │  Security    │  │   Activity Feed  │  │
│  └─────────────┘  └──────────────┘  └──────────────────┘  │
└─────────────────────────────────────────────────────────────┘
                            │
                    API Calls (Axios)
                            │
┌─────────────────────────────────────────────────────────────┐
│                      Backend (Express.js)                    │
│  ┌──────────────────────────────────────────────────────┐  │
│  │                   Middleware Layer                    │  │
│  │  • Auth • Error Handler • Rate Limiter • CORS        │  │
│  └──────────────────────────────────────────────────────┘  │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                    API Routes                        │   │
│  │  /auth  /files  /messages  /security  /activity     │   │
│  └─────────────────────────────────────────────────────┘   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                   Controllers                        │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                            │
                    Database Layer
                            │
┌─────────────────────────────────────────────────────────────┐
│                      MongoDB Atlas                           │
│  ┌──────┐  ┌──────┐  ┌──────┐  ┌──────┐  ┌──────────┐    │
│  │Users │  │Files │  │Msgs  │  │Events│  │Activity  │    │
│  └──────┘  └──────┘  └──────┘  └──────┘  └──────────┘    │
└─────────────────────────────────────────────────────────────┘
```

---

## 🏁 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16 or higher) - [Download](https://nodejs.org/)
- **npm** or **yarn** - Comes with Node.js
- **MongoDB** - [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) (cloud) or local installation
- **Git** - [Download](https://git-scm.com/)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Ritik-Malviya/ShadowShield.git
   cd ShadowShield
   ```

2. **Install Backend Dependencies**
   ```bash
   cd Backend
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../Frontend
   npm install
   ```

### Environment Configuration

#### Backend Environment Variables

Create a `.env` file in the `Backend` directory:

```env
# Server Configuration
NODE_ENV=development
PORT=5000

# Database
MONGO_URI=mongodb://localhost:27017/shadowshield
# For MongoDB Atlas:
# MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/shadowshield

# JWT Configuration
JWT_SECRET=your_super_secret_jwt_key_change_this_in_production
JWT_EXPIRE=30d
JWT_COOKIE_EXPIRE=30

# File Upload Configuration
FILE_UPLOAD_PATH=./public/uploads
MAX_FILE_UPLOAD=10000000

# CORS (if frontend is on different domain)
# CORS_ORIGIN=http://localhost:5173
```

#### Frontend Environment Variables

Create a `.env` file in the `Frontend` directory:

```env
# API Configuration
VITE_API_URL=http://localhost:5000/api

# Optional: If using Supabase for additional features
# VITE_SUPABASE_URL=your_supabase_url
# VITE_SUPABASE_ANON_KEY=your_supabase_key
```

### Running the Application

#### Development Mode

1. **Start the Backend Server**
   ```bash
   cd Backend
   npm run dev
   ```
   The backend will run on `http://localhost:5000`

2. **Start the Frontend Development Server** (in a new terminal)
   ```bash
   cd Frontend
   npm run dev
   ```
   The frontend will run on `http://localhost:5173`

3. **Access the Application**
   Open your browser and navigate to `http://localhost:5173`

#### Production Mode

1. **Build the Frontend**
   ```bash
   cd Frontend
   npm run build
   ```

2. **Start the Backend in Production**
   ```bash
   cd Backend
   npm start
   ```

---

## 📂 Project Structure

```
ShadowShield/
├── Backend/
│   ├── config/
│   │   └── db.js                    # Database configuration
│   ├── controllers/
│   │   ├── authController.js        # Authentication logic
│   │   ├── fileController.js        # File operations
│   │   ├── messageController.js     # Message handling
│   │   ├── securityController.js    # Security events
│   │   └── activityController.js    # Activity tracking
│   ├── middleware/
│   │   ├── auth.js                  # JWT authentication
│   │   ├── error.js                 # Error handling
│   │   ├── async.js                 # Async wrapper
│   │   └── debugUpload.js           # Upload debugging
│   ├── models/
│   │   ├── User.js                  # User schema
│   │   ├── File.js                  # File schema
│   │   ├── Message.js               # Message schema
│   │   ├── SecurityEvent.js         # Security event schema
│   │   └── Activity.js              # Activity schema
│   ├── routes/
│   │   ├── authRoutes.js            # Authentication endpoints
│   │   ├── fileRoutes.js            # File endpoints
│   │   ├── messageRoutes.js         # Message endpoints
│   │   ├── securityRoutes.js        # Security endpoints
│   │   └── activityRoutes.js        # Activity endpoints
│   ├── public/
│   │   └── uploads/                 # File storage directory
│   ├── utils/
│   │   └── errorResponse.js         # Custom error class
│   ├── .env                         # Environment variables
│   ├── server.js                    # Express server setup
│   └── package.json
│
├── Frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── auth/                # Login, Register, OneTimeAccess
│   │   │   ├── dashboard/           # Dashboard components
│   │   │   ├── files/               # File management UI
│   │   │   ├── messages/            # Messaging interface
│   │   │   ├── security/            # Security monitoring
│   │   │   ├── layout/              # Layout components
│   │   │   ├── shared/              # Shared components
│   │   │   └── ui/                  # UI primitives (Radix)
│   │   ├── contexts/
│   │   │   └── AuthContext.tsx      # Authentication context
│   │   ├── services/
│   │   │   └── api.ts               # API service layer
│   │   ├── lib/
│   │   │   └── utils.ts             # Utility functions
│   │   ├── types/
│   │   │   └── supabase.ts          # Type definitions
│   │   ├── App.tsx                  # Main app component
│   │   ├── main.tsx                 # Entry point
│   │   └── index.css                # Global styles
│   ├── public/
│   ├── .env                         # Environment variables
│   ├── index.html
│   ├── vite.config.ts               # Vite configuration
│   ├── tailwind.config.js           # Tailwind configuration
│   ├── tsconfig.json                # TypeScript config
│   └── package.json
│
└── README.md
```

---

## 📡 API Documentation

### Authentication Endpoints

#### Register User
```http
POST /api/auth/register
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "securePassword123"
}
```

#### Login
```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "securePassword123"
}
```

#### Get Current User
```http
GET /api/auth/me
Authorization: Bearer {token}
```

### File Endpoints

#### Upload File
```http
POST /api/files/upload
Authorization: Bearer {token}
Content-Type: multipart/form-data

file: [binary]
```

#### Get User Files
```http
GET /api/files
Authorization: Bearer {token}
```

#### Generate One-Time Access Link
```http
POST /api/files/:id/generate-access
Authorization: Bearer {token}
Content-Type: application/json

{
  "expiresIn": 3600  // seconds
}
```

#### Access File (One-Time Link)
```http
GET /api/files/access/:accessId
```

### Message Endpoints

#### Send Message
```http
POST /api/messages
Authorization: Bearer {token}
Content-Type: application/json

{
  "recipientId": "user_id",
  "content": "Message content",
  "encrypted": true
}
```

#### Get User Messages
```http
GET /api/messages
Authorization: Bearer {token}
```

### Security Endpoints

#### Get Security Events
```http
GET /api/security/events
Authorization: Bearer {token}
```

#### Log Security Event
```http
POST /api/security/log
Authorization: Bearer {token}
Content-Type: application/json

{
  "type": "LOGIN_ATTEMPT",
  "severity": "medium",
  "description": "Failed login attempt"
}
```

### Activity Endpoints

#### Get User Activity
```http
GET /api/activity
Authorization: Bearer {token}
```

---

## 🔒 Security Features

### 1. **Authentication & Authorization**
- JWT-based stateless authentication
- Secure password hashing with bcryptjs (10 rounds)
- HTTP-only cookies for token storage
- Token expiration and refresh mechanism

### 2. **Rate Limiting**
- Configurable rate limits per endpoint
- Protection against brute-force attacks
- IP-based request tracking

### 3. **File Security**
- File type validation
- Size limit enforcement (configurable)
- Secure file storage with unique naming
- One-time access link generation
- Automatic file cleanup for expired links

### 4. **Data Protection**
- CORS configuration
- Input sanitization
- MongoDB injection prevention with Mongoose
- XSS protection

### 5. **Monitoring**
- Real-time security event logging
- Activity tracking
- AI-powered anomaly detection
- Comprehensive audit trails

### 6. **Network Security**
- HTTPS enforcement (production)
- Secure headers
- CORS whitelist configuration

---

## 📖 Usage Guide

### 1. **Creating an Account**
- Navigate to `/register`
- Fill in your name, email, and password
- Click "Register" to create your account
- You'll be automatically logged in

### 2. **Uploading Files**
- Log in to your account
- Navigate to the Files section
- Click "Upload File" button
- Select your file and click "Upload"
- File will be encrypted and stored securely

### 3. **Generating One-Time Access Links**
- Go to your uploaded files
- Click on a file to view details
- Click "Generate Access Link"
- Set expiration time (optional)
- Copy and share the link
- Link will expire after first use or timeout

### 4. **Sending Secure Messages**
- Navigate to Messages section
- Click "Compose New Message"
- Select recipient
- Type your message
- Enable encryption (optional)
- Click "Send"

### 5. **Monitoring Security**
- Access the Security Log from the sidebar
- View real-time security events
- Check AI analysis of suspicious activities
- Review activity feed for user actions

### 6. **Accessing Shared Files**
- Receive a one-time access link
- Click the link
- File will be displayed/downloaded
- Link becomes invalid after access

---

## 🚢 Deployment

### Backend Deployment (Render/Railway/Heroku)

1. **Prepare for Deployment**
   ```bash
   # Ensure package.json has start script
   "scripts": {
     "start": "NODE_ENV=production node server"
   }
   ```

2. **Set Environment Variables**
   - Set all required environment variables in your hosting platform
   - Ensure `NODE_ENV=production`
   - Use MongoDB Atlas connection string

3. **Deploy**
   ```bash
   git push heroku main
   # or use Render/Railway's Git integration
   ```

### Frontend Deployment (Vercel/Netlify)

1. **Build the Project**
   ```bash
   cd Frontend
   npm run build
   ```

2. **Deploy to Vercel**
   ```bash
   npm install -g vercel
   vercel --prod
   ```

3. **Configure Environment Variables**
   - Set `VITE_API_URL` to your backend URL
   - Configure any other required variables

### Docker Deployment (Optional)

Create `Dockerfile` in Backend:
```dockerfile
FROM node:16-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 5000
CMD ["npm", "start"]
```

Build and run:
```bash
docker build -t shadowshield-backend .
docker run -p 5000:5000 --env-file .env shadowshield-backend
```

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Getting Started

1. **Fork the repository**
   ```bash
   git clone https://github.com/your-username/ShadowShield.git
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make your changes**
   - Write clean, documented code
   - Follow existing code style
   - Add tests if applicable

4. **Commit your changes**
   ```bash
   git commit -m "Add amazing feature"
   ```

5. **Push to your branch**
   ```bash
   git push origin feature/amazing-feature
   ```

6. **Open a Pull Request**

### Code Style Guidelines

- Use ESLint for JavaScript/TypeScript
- Follow Airbnb style guide
- Write meaningful commit messages
- Document complex logic
- Add JSDoc comments for functions

### Areas for Contribution

- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Test coverage
- ♿ Accessibility improvements

---

## 🗺️ Roadmap

### Phase 1: Core Features ✅
- [x] User authentication system
- [x] File upload and storage
- [x] One-time access links
- [x] Secure messaging
- [x] Activity tracking
- [x] Security event logging

### Phase 2: Enhanced Security 🚧
- [ ] End-to-end encryption for messages
- [ ] Two-factor authentication (2FA)
- [ ] Blockchain-based file verification
- [ ] Advanced AI threat detection
- [ ] Audit log export

### Phase 3: Advanced Features 📋
- [ ] File versioning system
- [ ] Collaborative file editing
- [ ] Team workspaces
- [ ] Role-based access control (RBAC)
- [ ] Mobile app (React Native)
- [ ] Desktop app (Electron)

### Phase 4: Enterprise Features 🎯
- [ ] SSO integration (SAML, OAuth)
- [ ] Compliance reports (GDPR, HIPAA)
- [ ] Custom branding
- [ ] Advanced analytics dashboard
- [ ] API webhooks
- [ ] Plugin system

### Phase 5: Performance & Scale 🚀
- [ ] CDN integration for file delivery
- [ ] Redis caching layer
- [ ] Microservices architecture
- [ ] Kubernetes deployment
- [ ] Load balancing
- [ ] Auto-scaling

---

## 📄 License

This project is licensed under the **MIT License** - see below for details:

```
MIT License

Copyright (c) 2025 Ritik Malviya

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📞 Contact

**Ritik Malviya** - Project Maintainer

- GitHub: [@Ritik-Malviya](https://github.com/Ritik-Malviya)
- Project Link: [https://github.com/Ritik-Malviya/ShadowShield](https://github.com/Ritik-Malviya/ShadowShield)

### Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/Ritik-Malviya/ShadowShield/issues) page
2. Search for existing solutions
3. Create a new issue with detailed information

### Acknowledgments

- Built during a hackathon with ❤️
- Inspired by the need for secure file sharing
- Thanks to all contributors and the open-source community
- UI components from [shadcn/ui](https://ui.shadcn.com/)
- Icons from [Lucide](https://lucide.dev/)

---

<div align="center">

**⭐ Star this repository if you find it helpful!**

Made with ❤️ by [Ritik Malviya](https://github.com/Ritik-Malviya)

</div>
