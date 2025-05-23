# Task Management Application

A full-stack task management web application built with React, Express, Node.js, and MongoDB.

## Features

### Core Features
- **Task Management**
  - Create tasks with title, description, deadline, and status
  - Edit existing tasks
  - Delete tasks with confirmation
  - Update task status
  
- **Task Filtering & Search**
  - Filter tasks by status (All, To Do, In Progress, Done)
  - Search tasks by keyword in title or description
  
- **Logic Features**
  - Auto-grouping tasks in columns by status
  - Sorting tasks by most recently updated
  - Form validation (empty fields, length limits, duplicate titles)
  - Overdue detection with warning badge

### Bonus Features
- Light/Dark mode toggle
- Responsive layout for mobile and desktop
- Clean, modern UI with smooth transitions

## Tech Stack

### Frontend
- React.js
- Redux Toolkit for state management
- TailwindCSS for styling
- Lucide React for icons

### Backend
- Express.js
- MongoDB with Mongoose
- RESTful API architecture

## Folder Structure

\`\`\`
task-management-app/
├── frontend/                 # Frontend React application
│   ├── public/              # Static files
│   └── src/
│       ├── components/      # React components
│       ├── context/         # Context providers (theme)
│       ├── redux/           # Redux store and slices
│       └── ...
└── backend/                 # Backend Express application
    ├── controllers/         # Route controllers
    ├── models/              # Mongoose models
    ├── routes/              # API routes
    └── ...
\`\`\`

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas)

### Option 1: Running the entire application with one command
1. Install dependencies for the root, client, and server:
   \`\`\`
   npm run install-all
   \`\`\`

2. Create a `.env` file in the server directory with the following variables:
   \`\`\`
   MONGODB_URI=mongodb://localhost:27017/task-manager
   PORT=5000
   \`\`\`

3. Start both the client and server with one command:
   \`\`\`
   npm run dev
   \`\`\`

4. Open your browser and navigate to `http://localhost:3000`

### Option 2: Running client and server separately

#### Backend Setup
1. Navigate to the backend directory:
   \`\`\`
   cd backend
   \`\`\`

2. Install dependencies:
   \`\`\`
   npm install
   \`\`\`

3. Start the server:
   \`\`\`
   node app.js (Server File)
   \`\`\`

#### Frontend Setup
1. Navigate to the frontend directory:
   \`\`\`
   cd frontend
   \`\`\`

2. Install dependencies:
   \`\`\`
   npm install
   \`\`\`

3. Start the development server:
   \`\`\`
   npm run dev
   \`\`\`

4. Open your browser and navigate to `http://localhost:5173/`

## Demo Video

[Watch the demo video]([Loom](https://www.loom.com/share/cb0f85cf2169484387335dd67c66a064?sid=f419add2-496d-4d29-b905-7b6aa7db3ada))

## Implementation Details

### Task Management Logic
- Tasks are stored in MongoDB with fields for title, description, status, deadline, and timestamps
- The frontend uses Redux Toolkit to manage state and API interactions
- Tasks are automatically grouped by status and sorted by most recently updated

### Validation
- Frontend validation prevents empty titles and enforces character limits
- Backend validation ensures data integrity and prevents duplicate titles within the same status group
- Overdue detection compares the current date with task deadlines

### UI/UX Features
- Responsive design works on mobile and desktop
- Dark mode toggle with persistent user preference
- Interactive task cards with status dropdown
- Confirmation modal for task deletion
