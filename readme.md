# Blog It 📝

A modern, full-stack blogging platform built with Node.js, Express, MongoDB, and Bootstrap. Create, share, and discuss blog posts with a clean and responsive interface.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat&logo=bootstrap&logoColor=white)

## ✨ Features

### 📖 Blog Management

- **Create & Edit** - Write and format blog posts with ease
- **Delete** - Remove your own blog posts
- **View All** - Browse all published blogs in a responsive grid layout
- **Individual Pages** - Each blog has its own dedicated page

### 👤 User Authentication

- **Sign Up** - Create new accounts with username and password
- **Login/Logout** - Secure session-based authentication using Passport.js
- **User Profiles** - View your profile with all your published blogs

### 💬 Comments System

- **Add Comments** - Engage with blog posts through comments
- **Delete Comments** - Authors can delete their own comments
- **Moderation** - Blog owners can remove any comments on their posts
- **Author Display** - See who commented and when

### 🔒 Security Features

- Password hashing with passport-local-mongoose
- Session management with express-session
- Input validation using Joi
- MongoDB injection prevention with ObjectId validation
- Authorization checks for edit/delete operations

### 🎨 User Interface

- Responsive Bootstrap 5 design
- Mobile-friendly navigation
- Flash messages for user feedback
- Clean and modern card-based layout
- Intuitive user experience

## 🚀 Getting Started

Capstone Project/
├── models/
│   ├── blog.js          # Blog schema with comments
│   └── user.js          # User schema with passport plugin
├── routes/
│   ├── blogs.js         # Blog and comment routes
│   └── user.js          # Authentication routes
├── views/
│   ├── layouts/
│   │   ├── boilerplate.ejs  # Main layout template
│   │   ├── header.ejs       # Navigation header
│   │   ├── footer.ejs       # Footer
│   │   └── flash.ejs        # Flash messages
│   ├── users/
│   │   ├── login.ejs        # Login page
│   │   ├── signup.ejs       # Registration page
│   │   └── profile.ejs      # User profile page
│   ├── index.ejs        # Blog listing page
│   ├── add.ejs          # Create blog page
│   ├── edit.ejs         # Edit blog page
│   └── show.ejs         # Single blog view with comments
├── public/
│   └── style.css        # Custom styles
├── middlewares.js       # Authentication middlewares
├── models.js            # Joi validation schemas
├── app.js               # Main application file
├── package.json         # Dependencies
└── readme.md            # This file
```

## 🛠️ Technologies Used

### Backend

- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling

### Authentication

- **Passport.js** - Authentication middleware
- **passport-local** - Local authentication strategy
- **passport-local-mongoose** - Mongoose plugin for Passport

### Templating & Styling

- **EJS (Embedded JavaScript)** - Templating engine
- **ejs-mate** - Layout support for EJS
- **Bootstrap 5** - CSS framework

### Validation & Security

- **Joi** - Data validation
- **express-session** - Session management
- **connect-flash** - Flash messages
- **method-override** - HTTP method override

## 📚 API Routes

### Blog Routes

| Method | Endpoint          | Description      | Auth Required |
| ------ | ----------------- | ---------------- | ------------- |
| GET    | `/blogs`          | List all blogs   | No            |
| GET    | `/blogs/new`      | New blog form    | Yes           |
| GET    | `/blogs/:id`      | View single blog | No            |
| GET    | `/blogs/:id/edit` | Edit blog form   | Yes (Owner)   |
| POST   | `/blogs`          | Create new blog  | Yes           |
| PUT    | `/blogs/:id`      | Update blog      | Yes (Owner)   |
| DELETE | `/blogs/:id`      | Delete blog      | Yes (Owner)   |

### Comment Routes

| Method | Endpoint                         | Description    | Auth Required      |
| ------ | -------------------------------- | -------------- | ------------------ |
| POST   | `/blogs/:id/comments`            | Add comment    | Yes                |
| DELETE | `/blogs/:id/comments/:commentId` | Delete comment | Yes (Author/Owner) |

### User Routes

| Method | Endpoint        | Description   | Auth Required |
| ------ | --------------- | ------------- | ------------- |
| GET    | `/user/login`   | Login page    | No            |
| GET    | `/user/signup`  | Signup page   | No            |
| GET    | `/user/profile` | User profile  | Yes           |
| POST   | `/user/login`   | Login user    | No            |
| POST   | `/user/signup`  | Register user | No            |
| POST   | `/user/logout`  | Logout user   | Yes           |

Built with ❤️ by Aman

**Note**: This is a capstone project demonstrating full-stack web development skills with Node.js, Express, MongoDB, and modern web technologies.# BlogIt
