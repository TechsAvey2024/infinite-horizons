# Infinite Horizons - Blog Application

## Project Overview

Infinite Horizons is a simple yet elegant blog web application that allows users to create, view, edit, and delete blog posts in real-time. Built with modern web technologies, this project demonstrates core concepts of server-side rendering and RESTful API design. The application provides an intuitive interface for managing personal blog content with a focus on user experience and clean design.

## Features

- **Post Creation**: Users can easily create new blog posts with a title and content
- **Post Viewing**: Display all created posts on the home page with timestamps
- **Post Editing**: Update existing posts with new titles and content
- **Post Deletion**: Remove unwanted posts with a single click
- **Responsive Design**: The application is styled and responsive, providing a good user experience on both desktop and mobile devices
- **Real-time Updates**: Posts are instantly reflected on the page after creation, editing, or deletion

## Technology Stack

### Why These Technologies?

**Node.js & Express.js**

- Node.js provides a lightweight, event-driven runtime perfect for building scalable web applications
- Express.js is a minimal and flexible web framework that simplifies routing and middleware management
- Together, they enable rapid development of server-side applications with JavaScript

**EJS (Embedded JavaScript Templating)**

- EJS allows dynamic HTML generation on the server-side
- Clean syntax that seamlessly embeds JavaScript in HTML templates
- Perfect for projects that need server-rendered views without heavy frontend frameworks

**Body-Parser Middleware**

- Handles parsing of incoming request bodies (both URL-encoded and JSON)
- Essential for processing form submissions and AJAX requests
- Simplifies data extraction from POST and PUT requests

**Nodemon**

- Automatically restarts the server during development when file changes are detected
- Significantly improves developer experience by eliminating manual server restarts
- Saves time during the development and debugging process

## Project Structure

```
infinite-horizons/
├── index.js                 # Main server file with all routes and logic
├── package.json             # Project dependencies and metadata
├── public/                  # Static assets
│   ├── css/
│   │   └── main.css        # Styling for the application
│   ├── js/
│   │   └── scripts.js      # Client-side JavaScript
│   └── images/             # Image assets
└── views/                   # EJS templates
    ├── index.ejs           # Main page template
    └── partials/
        ├── header.ejs      # Header component
        └── footer.ejs      # Footer component
```

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm (comes with Node.js)

### Installation

1. Clone or download the project
2. Navigate to the project directory
3. Install dependencies:
   ```bash
   npm install
   ```

### Running the Application

Start the server using:

```bash
node index.js
```

Or for development with auto-restart on file changes:

```bash
npx nodemon index.js
```

The application will start listening on `http://localhost:3000`

## How It Works

1. **Server Setup**: Express.js sets up a server on port 3000
2. **Static Files**: CSS and JavaScript files are served from the `public` directory
3. **Rendering**: EJS templates are rendered with dynamic post data
4. **CRUD Operations**:
   - GET `/` - Displays all posts
   - POST `/posts` - Creates a new post
   - PUT `/posts/:id` - Updates an existing post
   - DELETE `/posts/:id` - Deletes a post

## Data Storage

Posts are stored in memory during the application session. When the server restarts, all posts will be reset. This design is intentional for a prototype application; future versions could implement database persistence using MongoDB, PostgreSQL, or similar technologies.

## Deliverables

✓ Node.js/Express server with full CRUD functionality
✓ EJS templating for dynamic HTML generation
✓ CSS styling for responsive design
✓ Client-side JavaScript for interactive features
