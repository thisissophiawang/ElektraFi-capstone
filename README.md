## ElektraFi: Gamified Financial Wellness Platform

This project is part of our capstone research at Northeastern University Vancouver, focused on increasing user retention in financial wellness platforms by introducing a gamified task page. Built on the principles of Self-Determination Theory (SDT), ElektraFi uses features like streaks, badges, and progress tracking to enhance user motivation and foster consistent financial habits such as saving, budgeting, and debt reduction.

Note: The code resides in ElekraFi's GitHub repository and is not available for external sharing


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

## Team Members
- Sophia Wang
- Haoyi Gao
- Yijia Cao  


---

## Meet the Team & Explore Our Project

- [ElektraFi Panel Review 2: Project Showcase](https://youtu.be/e54t63F5Mwk)  
- [10-Minute Detailed Video](https://youtu.be/e54t63F5Mwk)  
- [Our Research Paper (Overleaf)](https://www.overleaf.com/read/wyvwgxnnvqcr#c6339b)  
- [Poster PDF](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/Poster.pdf)

![Our Poster](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/poster%20.png)

---

## Tech Stack Overview
- **Frontend**: React (Vite), TypeScript, Tailwind CSS  
- **Backend**: Node.js 22, GraphQL, MongoDB  
- **Dev Tools**: Yarn, Apollo Client, GitHub Actions

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


<img src="https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/data flow.png" alt="Workflow" width="60%">


---

## Frontend Development


<img src="https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/frontend%20data%20flow.png"  alt="Frontend Data Flow" width="60%">


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

## Backend Development

<img src="https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/backend%20data%20flow.png"  alt="Backend Data Flow" width="60%">


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

## Setup Instructions

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


## 🧱 Overview of Project Structure

The ElektraFi project follows a modular full-stack architecture with a clearly separated frontend and backend. It is built using modern web development tools and frameworks such as React, GraphQL, and Node.js.

Note: The code resides in ElekraFi's GitHub repository and is not available for external sharing

```
feat/streak-gamification/
├── frontend/                     # React + Vite frontend
│   ├── src/components/          # Reusable UI components (TaskCard, Badge, StreakBar)
│   ├── src/pages/               # Page-level views (TaskPage, Dashboard)
│   ├── src/context/             # Global state (UserContext, TaskContext)
│   ├── src/graphql/             # GraphQL queries & mutations (tasks, users, rewards)
│   └── src/assets/              # Icons, badge illustrations, and UI resources
│
├── nest-backend/                # Node.js backend with GraphQL
│   ├── modules/
│   │   ├── tasks/               # Task completion logic, streak tracking
│   │   ├── rewards/            # Points and badge system logic
│   │   ├── verification/       # Flinks API + fallback verification
│   ├── graphql/                # Schema definitions and resolvers
│   └── utils/                  # Shared utilities and error handling
│
├── ops/                         # Environment and deployment configs
├── public/                      # Static assets (favicon, logos)
└── README.md                    # Project documentation
```

---
## Demo Instructions

1. Start both servers using `yarn develop` and `yarn dev`  
2. Open [http://localhost:3000](http://localhost:3000)  
3. Log in using the demo test account  
4. Explore:
   - Weekly progress tracker  
   - Task card system with real-time feedback  
   - Badge collections and points dashboard











