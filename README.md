Name: Harman  
UID: 24BCF10046  
Section: 24BCF -1(B)  

# Smart Todo Manager - Full Stack Application

## Project Overview
This is a comprehensive full-stack todo management application that demonstrates modern web development practices. The application features a React frontend with a Node.js/Express backend, providing complete CRUD operations, real-time statistics, and persistent data storage with both localStorage and API integration.

## Approach & Architecture

### 1. **Full-Stack Architecture**
   - **Backend**: Node.js/Express REST API server
   - **Frontend**: React application with hooks and state management
   - **Data Flow**: Frontend ↔ REST API ↔ In-memory storage
   - **Dual Persistence**: localStorage fallback + backend API

### 2. **Backend Implementation (Express Server)**
   - **Framework**: Express.js with CORS middleware
   - **Data Storage**: In-memory array (todos)
   - **API Endpoints**:
     - `POST /todos` - Create new todo
     - `GET /todos` - Retrieve all todos
     - `PUT /todos/:id` - Update todo completion status
     - `DELETE /todos/:id` - Remove todo
   - **Port**: 5001 (to avoid conflicts with frontend dev server)

### 3. **Frontend State Management**
   - **useState Hooks**: Multiple state variables for complex UI
     - `todos`: Array of todo objects
     - `text`: Input field value
     - `filter`: Current filter selection
     - `editingId` & `editText`: Inline editing state
   - **useEffect Hooks**: Side effects for data persistence and API calls

### 4. **Data Persistence Strategy**
   - **Primary**: Backend API with axios HTTP client
   - **Fallback**: localStorage for offline functionality
   - **Synchronization**: localStorage loaded first, then API data
   - **Real-time Updates**: API calls after every CRUD operation

### 5. **CRUD Operations Implementation**
   - **Create**: Add new todos via API POST request
   - **Read**: Fetch todos from API or localStorage
   - **Update**: Toggle completion status via API PUT
   - **Delete**: Remove todos via API DELETE
   - **Edit**: Inline editing with local state management

### 6. **Advanced Features**
   - **Filtering System**: All/Completed/Pending views
   - **Statistics Dashboard**: Total, completed count, and progress percentage
   - **Inline Editing**: Click-to-edit functionality for todo text
   - **Visual Feedback**: Strike-through for completed items
   - **Responsive Design**: Centered layout with modern styling

### 7. **UI/UX Design Approach**
   - **Dark Theme**: Professional color scheme with high contrast
   - **Component Layout**: Centered container with rounded corners
   - **Interactive Elements**: Hover effects and button styling
   - **Status Indicators**: Visual completion states
   - **Gallery Section**: Screenshots demonstrating functionality

## File Structure
```
exp10/
├── root folder/
│   ├── backend/
│   │   ├── package.json     # Backend dependencies
│   │   └── server.js        # Express server with API routes
│   └── frontend/
│       ├── package.json     # Frontend dependencies
│       ├── public/
│       │   ├── images/      # Screenshots for demo
│       │   └── index.html   # HTML template
│       └── src/
│           ├── App.js       # Main React component
│           ├── App.css      # Component styling
│           ├── index.js     # React entry point
│           └── ...          # Other React files
└── README.md                # This documentation file
```

## Technologies Used
- **Backend**:
  - Node.js & Express.js
  - CORS middleware
  - RESTful API design
- **Frontend**:
  - React 19.2.5 with hooks
  - Axios for HTTP requests
  - localStorage API
  - CSS3 for styling

## Key Features
✅ Full CRUD operations via REST API  
✅ Real-time statistics and progress tracking  
✅ Inline editing with state management  
✅ Multiple filter options  
✅ Dual persistence (API + localStorage)  
✅ Modern dark theme UI  
✅ Responsive and accessible design  

## Learning Outcomes
- Building REST APIs with Express.js
- Implementing full-stack applications
- Managing complex React state with multiple hooks
- Handling API integration with axios
- Creating persistent data storage solutions
- Designing modern web application UIs
- Implementing filtering and statistics features

## Running the Project

### Backend Setup
```bash
cd root folder/backend
npm install
node server.js
```
Server runs on `http://localhost:5001`

### Frontend Setup
```bash
cd root folder/frontend
npm install
npm start
```
Frontend runs on `http://localhost:3000`

## API Endpoints

### Create Todo
```http
POST http://localhost:5001/todos
Content-Type: application/json

{
  "text": "Learn React hooks"
}
```

### Get All Todos
```http
GET http://localhost:5001/todos
```

### Update Todo Status
```http
PUT http://localhost:5001/todos/1234567890
Content-Type: application/json

{
  "completed": true
}
```

### Delete Todo
```http
DELETE http://localhost:5001/todos/1234567890
```

## Application Features

### Todo Management
- **Add Tasks**: Input field with add button
- **Mark Complete**: Click todo text to toggle status
- **Delete Tasks**: Remove button for each todo
- **Edit Tasks**: Inline editing with save functionality

### Filtering & Stats
- **Filter Buttons**: All, Completed, Pending views
- **Statistics Bar**: Shows total, completed, and progress percentage
- **Visual Indicators**: Strike-through for completed items

### Data Persistence
- **API Integration**: Real-time sync with backend
- **Offline Support**: localStorage fallback
- **Automatic Saving**: Changes persist across sessions

## Future Enhancements
- Add user authentication and multi-user support
- Implement real database (MongoDB/PostgreSQL)
- Add due dates and priority levels
- Create categories/tags for todos
- Add search functionality
- Implement drag-and-drop reordering
- Add notifications and reminders
- Create mobile app version
- Add data export/import features
- Implement undo/redo functionality</content>
<parameter name="filePath">/Users/harmansingh/Documents/experiment 1.33/exp10/README.md