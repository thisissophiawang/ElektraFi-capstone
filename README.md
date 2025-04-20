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

- [ElektraFi: Project Showcase video (1-mins)](https://youtu.be/e54t63F5Mwk)  
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
<img src="https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/data flow.png" alt="Workflow" width="60%">

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


## Frontend Development


<img src="https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/frontend%20data%20flow.png"  alt="Frontend Data Flow" width="50%">


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


<img src="https://github.com/thisissophiawang/ElektraFi-capstone/blob/main/backend%20flow.png" alt="Backend Data Flow" width="50%">

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
## Architecture

### Frontend Components
1. **TaskStreakContext** (`frontend/src/contexts/taskStreakContext.tsx`)
   - Manages streak state and task completion logic
   - Handles automatic login task completion
   - Provides streak information to components

2. **TasksPage** (`frontend/src/pages/Tasks/TasksPage.tsx`)
   - Displays available tasks and their status
   - Shows streak information and rewards
   - Handles task completion UI

### Backend Components
1. **TaskStreakService** (`nest-backend/src/task-streak/task-streak.service.ts`)
   - Core business logic for streak management
   - Handles task completion and streak calculations
   - Manages points and level progression

2. **Database Schema**
   - `task_streaks` table: Stores user streaks and progress
   - `task_completions` table: Records individual task completions
   - `user_badges` table: Tracks earned rewards

## Task Types
The system supports several task types:
- `LOGIN`: Weekly login task (50 points)
- `BUDGET_CHECKIN`: Weekly budget review (300 points)
- `EXPENSE_TRACKING`: Weekly expense tracking (500 points)
- Additional financial tasks (SAVINGS_TRANSFER, EMERGENCY_FUND, etc.)

## Streak Mechanics

### Frequency Types
- `DAILY`: Tasks reset at midnight
- `WEEKLY`: Tasks reset at midnight on Monday
- `MONTHLY`: Tasks reset at midnight on the first of the month

### Streak Rewards
Each task has three reward levels:
1. **Bronze**: Complete 1 week
2. **Silver**: Complete 8 weeks consecutively
3. **Gold**: Complete 12 weeks consecutively

## Points System

### Milestone Progression
Points are awarded based on task completion and streak length:
- Base points per task completion
- Streak multiplier increases points earned
- Level progression based on total points

### Level Thresholds
- Level 1: 0-999 points
- Level 2: 1000-2499 points
- Level 3: 2500-4999 points
- Level 4: 5000-9999 points
- Level 5: 10000-19999 points
- Level 6: 20000+ points

## API Endpoints

### GraphQL Queries
```graphql
query GetUserStreaks($userId: String!) {
  getUserStreaks(userId: $userId) {
    id
    userId
    taskType
    currentStreak
    longestStreak
    lastCompletionDate
    frequency
    updatedAt
    totalPoints
    currentPointThreshold
    nextPointThreshold
    level
  }
}

query GetUserPointsInfo($userId: String!) {
  getUserPointsInfo(userId: $userId) {
    totalPoints
    currentPointThreshold
    nextPointThreshold
    level
  }
}
```

### GraphQL Mutations
```graphql
mutation CompleteTask($userId: String!, $taskType: TaskType!) {
  completeTask(userId: $userId, taskType: $taskType) {
    id
    userId
    taskType
    currentStreak
    longestStreak
    lastCompletionDate
    frequency
    updatedAt
    totalPoints
    currentPointThreshold
    nextPointThreshold
    level
  }
}
```

## Testing

### Frontend Tests
Run task streak context tests:
```bash
cd frontend
vitest taskStreakContext.spec.tsx
```

### Backend Tests
Run task streak service tests:
```bash
cd backend
npm run test:unit task-streak.service.spec.ts
```

## Development Notes

### Key Files
- `frontend/src/contexts/taskStreakContext.tsx`: Frontend streak management
- `frontend/src/pages/Tasks/TasksPage.tsx`: Task display and interaction
- `nest-backend/src/task-streak/task-streak.service.ts`: Backend streak logic
- `nest-backend/src/task-streak/config/available-tasks.config.ts`: Task configuration

### Important Considerations
1. Task availability is checked based on:
   - Last completion date
   - Task frequency
   - Reset period and time
2. Points are calculated as: `basePoints * currentStreak`
3. Level progression is based on total points reaching thresholds
4. Streak rewards are awarded automatically when conditions are met

## Maintenance

### Database Migrations
- `1733500000000-CreateTaskStreakTables.ts`: Initial table creation
- `1733500000001-add-points-to-task-streak.ts`: Added points and level tracking

### Configuration
Task settings can be modified in `available-tasks.config.ts`:
- Points per task
- Required streak lengths for rewards
- Task frequency and reset times
- Task categories and descriptions

## Task Configuration

### Task Levels and Streak Requirements
Each task has two types of levels:

1. **Required Level** (`requiredLevel` in TaskConfig)
   - This is the minimum user level needed to access the task
   - Currently, all tasks have `requiredLevel: 1`, meaning they're available from the start
   - This is separate from the streak reward levels

2. **Streak Reward Levels** (`streakRewards` in TaskConfig)
   - These are achievement levels based on consecutive completions
   - Each task has three reward levels:
     - Level 1 (Bronze): 1 week of consecutive completion
     - Level 2 (Silver): 8 weeks of consecutive completion
     - Level 3 (Gold): 12 weeks of consecutive completion
   - The level number in `streakRewards` corresponds to the achievement tier, not the required weeks

Example from the Login task:
```typescript
streakRewards: [
  { level: 1, medal: '🥉', name: 'Bronze', description: 'Complete 1 week of login' },
  { level: 2, medal: '🥈', name: 'Silver', description: 'Complete 8 weeks of login consecutively' },
  { level: 3, medal: '🥇', name: 'Gold', description: 'Complete 12 weeks of login consecutively' }
]
```

Note: The `level` in `streakRewards` is just an identifier for the achievement tier (1=Bronze, 2=Silver, 3=Gold) and doesn't need to match the number of weeks required. The actual streak requirements are defined in the descriptions. 

---

## Demo Instructions

1. Start both servers using `yarn develop` and `yarn dev`  
2. Open [http://localhost:3000](http://localhost:3000)  
3. Log in using the demo test account  
4. Explore:
   - Weekly progress tracker  
   - Task card system with real-time feedback  
   - Badge collections and points dashboard











