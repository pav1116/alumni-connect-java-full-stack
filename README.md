# alumni-connect-java-full-stack

A comprehensive full-stack web application that connects students, alumni, and faculty members to foster career development, mentorship, and community engagement.

## 🎯 Project Overview

Alumni Connect is a three-role platform designed to strengthen the relationship between students, alumni, and faculty. It facilitates:
- **Career Growth**: Job postings, internship opportunities, and referrals
- **Mentorship**: Connecting students with experienced alumni for guidance
- **Networking**: Alumni search, messaging, and community discussions
- **Events Management**: Webinars, workshops, and alumni reunions
- **Analytics**: Faculty insights into student-alumni engagement and placements

## 🏗️ Architecture

This is a modern full-stack application built with:

### Frontend
- **Next.js** - React-based framework for server-side rendering and static generation
- **TypeScript** - For type-safe development
- **Responsive Design** - Mobile-first approach with full responsiveness

### Backend
- **Next.js API Routes** - Serverless backend implementation
- **Prisma ORM** - Database management and migrations
- **Clerk Authentication** - Google Sign-in integration and JWT-based auth

### Database
- **SQLite** (Production) - Lightweight, reliable database with fallback handling

### Deployment
- **Vercel** - Hosting and continuous deployment

## 👥 User Roles

### Student
- Create and manage profile (name, branch, year, skills)
- Upload resume and cover materials
- Browse and apply for jobs/internships
- Request referrals and mentorship from alumni
- Search alumni by company
- Participate in forums and discussions
- Attend webinars and events
- Message alumni for networking

### Alumni
- Create professional profile (company, role, experience, LinkedIn)
- Post jobs and internship opportunities
- Provide referrals to students
- Accept mentorship requests from students
- Answer student questions in forums
- Participate in discussions
- Attend alumni reunions and events
- Share career experiences

### Faculty
- Verify faculty access and manage permissions
- Monitor student-alumni engagement statistics
- Track placements and opportunities
- Review referral activities
- Moderate discussions and content
- Create and manage events
- Access alumni directory

## ✨ Key Features

### Core Functionality
- ✅ Role-based login and authentication via Clerk
- ✅ Google Sign-in integration
- ✅ Personalized dashboards for each role
- ✅ One-to-one messaging system
- ✅ Discussion forums
- ✅ Search and filter users
- ✅ Logout functionality

### Student Features
- ✅ Job and internship browsing
- ✅ Job application tracking
- ✅ Referral requests
- ✅ Alumni search by company
- ✅ Mentorship requests
- ✅ Event attendance
- ✅ Forum participation

### Alumni Features
- ✅ Job and internship posting
- ✅ Referral management
- ✅ Mentorship provision
- ✅ Forum participation
- ✅ Event browsing

### Faculty Features
- ✅ Faculty verification
- ✅ Student-alumni engagement analytics
- ✅ Placement tracking
- ✅ Opportunity and referral monitoring
- ✅ Event management
- ✅ Alumni directory access

### Coming Soon 🚀
- Profile enrichment (resume uploads, skills, career interests)
- OTP verification
- Group chat functionality
- Privacy settings
- Event registration
- AI-based alumni recommendations
- Smart job matching
- Alumni achievements showcase
- PWA support

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | Next.js, React, TypeScript |
| **Authentication** | Clerk (Google Sign-in) |
| **Backend** | Next.js API Routes |
| **Database** | SQLite with Prisma ORM |
| **API/RPC** | tRPC (optional implementation) |
| **Deployment** | Vercel |
| **Middleware** | Clerk middleware for route protection |

## 📁 Project Structure

alumni-connect-java-full-stack/ ├── app/ # Next.js app directory (main application) ├── components/ # Reusable React components ├── lib/ # Utility functions and helpers ├── prisma/ # Prisma schema and migrations ├── scripts/ # Utility scripts ├── proxy.ts # Clerk authentication middleware ├── tsconfig.json # TypeScript configuration ├── vercel.json # Vercel deployment config ├── IMPLEMENTATION_CHECKLIST.md # Feature completion tracking └── README.md # This file

Code

## 🔐 Authentication & Security

- **Clerk** handles authentication with Google Sign-in
- Protected routes are configured in `proxy.ts`:
  - `/api/mentorship`
  - `/api/referrals`
  - `/api/opportunities`
  - `/api/forum`
  - `/api/chat`
  - `/api/events`
  - `/api/admin`
- JWT-based session management
- Fallback handling for database stability

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm/yarn
- Clerk account with Google OAuth configured
- (Optional) SQLite installed locally for development

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/pav1116/alumni-connect-java-full-stack.git
   cd alumni-connect-java-full-stack
Install dependencies

bash
npm install
# or
yarn install
Set up environment variables Create a .env.local file:

Code
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_publishable_key
CLERK_SECRET_KEY=your_secret_key
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

# Database
DATABASE_URL=file:./dev.db

# API
NEXT_PUBLIC_API_URL=http://localhost:3000
Set up the database

bash
npx prisma migrate dev
npx prisma generate
Run the development server

bash
npm run dev
# or
yarn dev
Open http://localhost:3000 in your browser.

Building for Production
bash
npm run build
npm start
📊 Implementation Status
Track feature completion in IMPLEMENTATION_CHECKLIST.md.

Current Progress:

Common Features: ~56% complete
Student Features: ~57% complete
Alumni Features: ~57% complete
Faculty Features: ~67% complete
🗄️ Database
The application uses Prisma ORM for database management.

Prisma Schema Location
/prisma/schema.prisma

Common Prisma Commands
bash
# Run migrations
npx prisma migrate dev

# Generate Prisma Client
npx prisma generate

# Access database with Prisma Studio
npx prisma studio
🤝 Contributing
Create a feature branch
Make your changes
Test thoroughly
Submit a pull request
📝 Documentation
IMPLEMENTATION_CHECKLIST.md - Detailed feature tracking and role permissions
vercel.json - Vercel deployment configuration
tsconfig.json - TypeScript compiler options
🐛 Known Issues & Notes
SQLite is used in production; fallback handling is implemented for reliability
Mentorship request visibility has hardened fallback storage
Group chat functionality is in development
OTP verification system is pending
📧 Support & Contact
For questions or issues, please open a GitHub issue or contact the maintainers.

📄 License
This project is open source and available under the MIT License.

Built with ❤️ for fostering alumni connections and career growth.
