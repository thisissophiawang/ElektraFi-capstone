## ElektraFi: Gamified Financial Wellness Platform

This project is part of our capstone research at Northeastern University Vancouver, focused on redesigning financial wellness engagement through Self-Determination Theory (SDT) and gamification principles. ElektraFi is a web-based platform aimed at increasing user motivation to build consistent financial habits, such as saving, budgeting, and debt reduction.

**Table of Contents:**
- [Team Members](#team-members)
- [Meet the Team & Explore Our Project](#meet-the-team--explore-our-project)
- [Tech Stack Overview](#tech-stack-overview)
- [Main Features](#main-features)
- [Frontend Development](#frontend-development)
- [Backend Development](#backend-development)
- [Setup Instructions](#setup-instructions)
- [Demo Instructions](#demo-instructions)

---

## 👥 Team Members
- Xinyi (Sophia) Wang  
- Yijia Cao  
- Haoyi Gao

---

## 📽️ Meet the Team & Explore Our Project

- [ElektraFi Project: Official Trailer](https://youtu.be/e54t63F5Mwk)  
- [10-Minute Detailed Video](https://youtu.be/e54t63F5Mwk)  
- [Our Research Paper (Overleaf)](https://www.overleaf.com/read/wyvwgxnnvqcr#c6339b)  
- [Poster PDF](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/Poster.pdf)

![Our Poster](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/poster%20.png)

---

## ⚙️ Tech Stack Overview
- **Frontend**: React (Vite), TypeScript, Tailwind CSS  
- **Backend**: Node.js 22, GraphQL, MongoDB  
- **Dev Tools**: Yarn, Apollo Client, GitHub Actions

---

## 🧩 Main Features

### 1. Weekly Progress Tracking
- Visual display of weekly task completion
- Progress bar with weekly goals

### 2. Active Task Management
- Organized task cards with points
- Quick completion buttons and categories

### 3. Points System
- Real-time points display
- Accumulated history and feedback

### 4. Weekly Login Task
- Streaks for consistent logins
- Rewards and indicators

### 5. Badge Collection System
- Bronze/Silver/Gold badge milestones
- Progress and gallery display

### 6. User Interface Features
- Responsive, intuitive task cards
- Navigation between task, progress, badges

### 7. Task Completion System
- One-click interaction
- Immediate visual updates

### 8. Error Handling
- Friendly error messages
- Retry and fallback mechanisms

![Workflow](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/workflow.png)

---

## 💻 Frontend Development

![Frontend Data Flow](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/frontend%20data%20flow.png)

### 1. First Commit - Foundation Building
- React + TypeScript architecture
- Navigation, task UI components

### 2. Second Commit - Data Integration
- GraphQL tasks and mutations
- Progress + error handling UI

### 3. Third Commit - Feature Enhancement
- Badge system, streak tracker
- Weekly progress, animation, notifications

### Development Strategy
- Progressive enhancement
- State management, feedback, responsive UI

### Key Achievements
- Real-time tracking, error tolerance
- Clean and scalable frontend logic

---

## 🔧 Backend Development

![Backend Data Flow](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/backend%20data%20flow.png)

### Task System Data Flow

1. **User Interaction Layer**
   - Task completion initiated via UI
2. **Frontend Processing**
   - Prepares GraphQL mutation
3. **API Communication Layer**
   - Validates + handles request
4. **Backend Logic**
   - Verifies completion, updates streaks
5. **Data Management Layer**
   - Updates user task and badge data
6. **State Synchronization**
   - UI reflects success, shows feedback
7. **Error Handling**
   - Recovery strategies, rollback logic
8. **Persistence**
   - Saves to MongoDB
9. **Feedback Loop**
   - Updates frontend, shows achievements

---

## 📦 Setup Instructions

### Prerequisites

- [Node.js 22](https://nodejs.org/)
- [Yarn](https://yarnpkg.com/)

### Installation & Running Project

```bash
# Clone the repository
git clone https://github.com/thisissophiawang/Sp25_Elektrafi.git
cd Sp25_Elektrafi

# Install dependencies
yarn install

# Set up environment variables
# For macOS/Linux:
cp ops/dev.env .env

# For Windows (Command Prompt):
copy ops/dev.env .env

# For Windows (PowerShell):
Copy-Item ops/dev.env -Destination .env

# Start the Backend Server
yarn develop

# Start the Frontend (open a second terminal)
yarn dev

# The React app will run at: http://localhost:3000
# Log in with the test account and explore the gamified features
```

---

## 🎬 Demo Instructions

1. Start both servers using `yarn develop` and `yarn dev`  
2. Open [http://localhost:3000](http://localhost:3000)  
3. Log in using the demo test account  
4. Explore:
   - Weekly progress tracker  
   - Task card system with real-time feedback  
   - Badge collections and points dashboard











