## ElektraFi: Gamified Financial Wellness Platform

This project is part of our capstone research at Northeastern University Vancouver, focused on redesigning financial wellness engagement through Self-Determination Theory (SDT) and gamification principles. ElektraFi is a web-based platform aimed at increasing user motivation to build consistent financial habits, such as saving, budgeting, and debt reduction.

**Table of Contents:**
- [Meet the Team \& Explore Our Project](#meet-the-team--explore-our-project)
- [Concepts and Resources](#Team-Members)
- [Main Features](#Main-Features)
- [Frontend Development Summary](#Frontend-Development) 
- [Backend Development Summary](#Backend-Development) 
- [Notes](#notes)

# Team Members
- Xinyi (Sophia) Wang  
- Yijia Cao  
- Haoyi Gao


# Meet the Team & Explore Our Project

- [ElektraFi Project: Official Trailer](https://youtu.be/e54t63F5Mwk)
- [10 Minutes Detailed Video](https://youtu.be/e54t63F5Mwk)
- [Our Research Paper](https://www.overleaf.com/read/wyvwgxnnvqcr#c6339b)
- [Get the PDF of Our Poster](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/Poster.pdf)
 ![Our Poster](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/poster%20.png)

 

# Main Features
## 1. Weekly Progress Tracking
- Visual display of weekly task completion progress
- Progress bar showing completed vs. total tasks
- Clear indication of weekly goals and achievements
- Easy-to-understand progress metrics

## 2. Active Task Management
- Display of current available tasks
- Task cards showing title, description, and points
- Completion status indicators
- Quick action buttons for task completion
- Task categories and organization

## 3. Points System
- Total accumulated points display
- Points earned per task completion
- Visual representation of point accumulation
- Points history tracking

## 4. Weekly Login Task
- Dedicated login task card
- Streak tracking for consecutive logins
- Reward system for consistent login
- Progress indicators for login frequency

## 5. Badge Collection System
- Organized badge display by category
- Visual representation of earned badges
- Badge progress tracking
- Achievement milestones
- Medal system (Bronze, Silver, Gold)

## 6. User Interface Features
- Clean and intuitive task card layout
- Responsive design for all devices
- Real-time status updates
- Progress visualization
- Easy navigation between features

## 7. Task Completion System
- Simple one-click task completion
- Immediate feedback on completion
- Progress updates in real-time
- Streak maintenance tracking

## 8. Error Handling
- Clear error messages
- Graceful failure handling
- User-friendly error notifications
- Recovery mechanisms for failed operations


![Workflow](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/workflow.png)

# Frontend Development 

![Frontend Data Flow](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/frontend%20data%20flow.png)

## 1. First Commit - Foundation Building
- Established core React TypeScript architecture
- Created essential type definitions for tasks and rewards
- Implemented basic task page UI components
- Set up navigation and routing structure
- Built foundational task card components
- Implemented basic state management

## 2. Second Commit - Data Integration
- Integrated GraphQL for data management
- Implemented task fetching and completion mutations
- Added loading states and error handling
- Enhanced UI with progress indicators
- Implemented points tracking system
- Added basic streak tracking functionality

## 3. Third Commit - Feature Enhancement
- Implemented badge collection system
- Enhanced streak tracking with visual indicators
- Added weekly progress tracking
- Improved error handling and user feedback
- Enhanced UI with responsive design
- Added achievement notifications
- Implemented task completion animations

## Development Approach
- Progressive enhancement strategy
- Focus on core functionality first
- Iterative UI improvements
- Continuous error handling refinement
- User experience optimization
- Performance considerations

## Key Achievements
- Clean and intuitive user interface
- Real-time progress tracking
- Reliable task completion system
- Comprehensive error handling
- Responsive design implementation
- Efficient state management


# Backend Development 
![Backend Data Flow](https://github.com/thisissophiawang/Sp25_Elektrafi/blob/main/backend%20data%20flow.png)

# Task System Data Flow Overview

## 1. User Interaction Layer
- User initiates task completion through the UI
- System provides immediate visual feedback
- Progress indicators update in real-time

## 2. Frontend Processing
- Task completion request is formatted
- GraphQL mutation is prepared
- Local state management updates
- Error handling mechanisms activated

## 3. API Communication Layer
- GraphQL endpoint receives request
- Authentication and authorization checks
- Request validation and sanitization
- Response formatting and error handling

## 4. Backend Business Logic
- Task availability verification
- Completion eligibility checks
- Streak calculation and updates
- Reward qualification assessment

## 5. Data Management Layer
- Task completion records created
- User streak data updated
- Points and rewards calculated
- Badge achievements processed

## 6. State Synchronization
- Frontend cache updates
- UI components refresh
- Progress indicators update
- Achievement notifications trigger

## 7. Error Handling & Recovery
- Frontend error display
- Backend error logging
- Transaction rollback if needed
- User notification system

## 8. Data Persistence
- Task completion history stored
- User progress tracked
- Achievement records maintained
- Analytics data collected

## 9. Feedback Loop
- User receives completion confirmation
- Progress updates displayed
- New achievements highlighted
- Next steps suggested
