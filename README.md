## ElektraFi: Gamified Financial Wellness Platform

This project is part of our capstone research at Northeastern University Vancouver, focused on increasing user retention in financial wellness platforms by introducing a gamified task page. Built on the principles of Self-Determination Theory (SDT), ElektraFi uses features like streaks, badges, and progress tracking to enhance user motivation and foster consistent financial habits such as saving, budgeting, and debt reduction.

---

## Team Members
- Xinyi (Sophia) Wang
- Haoyi Gao
- Yijia Cao 

---

## Main Features

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


---


## 📦 Setup Instructions

### Prerequisites

- [Node.js 22](https://nodejs.org/)
- [Yarn](https://yarnpkg.com/)

### Installation & Running Project

```bash
# Clone the repository
git clone https://github.com/reframegroup/frontend.git
cd feat/streak-gamification

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

## Overview of project structure
The ElektraFi project follows a modular full-stack architecture with a clearly separated frontend and backend. It is built using modern web development tools and frameworks such as React, GraphQL, and Node.js.


Sp25_Elektrafi/
├── frontend/                      # React + Vite frontend
│   ├── src/components/               # Reusable UI components (TaskCard, Badge, StreakBar)
│   ├── src/pages/                    # Page-level components (TaskPage, Dashboard)
│   ├── src/context/                  # Global state (UserContext, TaskContext)
│   ├── src/graphql/                  # GraphQL queries & mutations (tasks, users, rewards)
│   └── src/assets/                   # Icons, badges, and UI resources
│
├── nest-backend/                      # Node.js backend with GraphQL
│   ├── modules/
│   │   ├── tasks/                # Task completion logic, streak tracking
│   │   ├── rewards/             # Points and badge system logic
│   │   ├── verification/        # Flinks API + fallback verification
│   ├── graphql/                 # Schema definitions and resolvers
│   └── utils/                   # Shared utilities and error handling
│
├── ops/                          # Environment and deployment configs
│
├── public/                       # Static assets
│
└── README.md                     # Project documentation

---

## 🎬 Demo Instructions

1. Start both servers using `yarn develop` and `yarn dev`  
2. Open [http://localhost:3000](http://localhost:3000)  
3. Log in using the demo test account  
4. Explore:
   - Weekly progress tracker  
   - Task card system with real-time feedback  
   - Badge collections and points dashboard
