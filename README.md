# PingUp - Social Media Application

A modern, full-stack social media platform built with React and Node.js that enables users to connect, share posts, send messages, and engage with content in real-time.

## 🚀 Features

### Core Features
- **User Authentication** - Secure login/signup with Clerk
- **User Profiles** - Customizable profiles with cover photos, avatars, and bio
- **Post Creation** - Create text posts with images/videos
- **Real-time Feed** - Scrollable feed with latest posts from connections
- **Stories** - Share temporary 24-hour stories
- **Messaging** - Real-time chat with connections
- **Connections** - Send/accept connection requests
- **Discover** - Find new people and trending content
- **Notifications** - Real-time notifications for interactions

### Advanced Features
- **Responsive Design** - Works seamlessly on desktop and mobile
- **Image Upload** - Cloud-based image storage with ImageKit
- **Real-time Updates** - Live notifications and messages
- **Search Functionality** - Search users and content

## 🛠️ Tech Stack

### Frontend
- **React** - UI library
- **Vite** - Build tool and dev server
- **Redux Toolkit** - State management
- **Tailwind CSS** - Styling framework
- **Axios** - HTTP client
- **React Router** - Client-side routing
- **Clerk** - Authentication service

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - MongoDB ODM
- **Clerk** - Authentication middleware
- **ImageKit** - Image storage service
- **Inngest** - Background job processing
- **Nodemailer** - Email services

## 📁 Project Structure

```
pingup-full-stack/
├── client/                 # React frontend
│   ├── src/
│   │   ├── api/           # API service layer
│   │   ├── app/           # Redux store configuration
│   │   ├── assets/        # Static assets
│   │   ├── components/    # Reusable UI components
│   │   ├── features/      # Redux slices
│   │   ├── pages/         # Page components
│   │   └── App.jsx        # Main app component
│   ├── public/            # Static files
│   └── package.json       # Frontend dependencies
├── server/                # Node.js backend
│   ├── controllers/       # Route controllers
│   ├── models/           # MongoDB models
│   ├── routes/           # API routes
│   ├── middlewares/      # Custom middleware
│   ├── configs/          # Configuration files
│   ├── inngest/          # Background jobs
│   └── server.js         # Entry point
└── README.md             # This file
```

## 🚦 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/pingup.git
cd pingup-full-stack
```

2. **Install server dependencies**
```bash
cd server
npm install
```

3. **Install client dependencies**
```bash
cd ../client
npm install
```

4. **Environment Variables**
Create `.env` files in both server and client directories:

**Server `.env`**
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/pingup
CLERK_PUBLISHABLE_KEY=your-clerk-publishable-key
CLERK_SECRET_KEY=your-clerk-secret-key
IMAGEKIT_PUBLIC_KEY=your-imagekit-public-key
IMAGEKIT_PRIVATE_KEY=your-imagekit-private-key
IMAGEKIT_URL_ENDPOINT=your-imagekit-url
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-email-password
INNGEST_EVENT_KEY=your-inngest-key
```

**Client `.env`**
```env
VITE_CLERK_PUBLISHABLE_KEY=your-clerk-publishable-key
VITE_API_URL=http://localhost:5000/api
```

5. **Start MongoDB**
```bash
mongod
```

6. **Run the development servers**

**Backend**
```bash
cd server
npm run server
```

**Frontend**
```bash
cd client
npm run dev
```

The application will be available at `http://localhost:5173`

## 🧪 Available Scripts

### Client Scripts
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

### Server Scripts
- `npm run server` - Start development server with nodemon
- `npm start` - Start production server

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login

### Users
- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user profile
- `GET /api/users/search` - Search users

### Posts
- `GET /api/posts` - Get all posts
- `POST /api/posts` - Create new post
- `GET /api/posts/:id` - Get post by ID
- `PUT /api/posts/:id` - Update post
- `DELETE /api/posts/:id` - Delete post
- `POST /api/posts/:id/like` - Like/unlike post
- `POST /api/posts/:id/comment` - Comment on post

### Stories
- `GET /api/stories` - Get all active stories
- `POST /api/stories` - Create new story
- `DELETE /api/stories/:id` - Delete story

### Messages
- `GET /api/messages/:userId` - Get messages with user
- `POST /api/messages` - Send new message
- `PUT /api/messages/:id/read` - Mark message as read

### Connections
- `POST /api/connections/request` - Send connection request
- `PUT /api/connections/:id/accept` - Accept connection request
- `DELETE /api/connections/:id` - Remove connection
- `GET /api/connections` - Get user connections

## 🎯 Usage

### Creating a Post
1. Click the "Create Post" button
2. Add your content and optionally upload images
3. Click "Post" to share with your connections

### Sending Messages
1. Navigate to Messages from the sidebar
2. Select a connection to start chatting
3. Type your message and press Enter to send

### Adding Stories
1. Click the "Add Story" button in stories section
2. Upload an image or video
3. Your story will be visible for 24 hours

### Managing Connections
1. Search for users in the Discover page
2. Send connection requests
3. Accept incoming requests from the Connections page

## 🛡️ Security Features

- JWT token-based authentication
- Password hashing with bcrypt
- CORS protection
- Input validation and sanitization
- Rate limiting
- Secure file upload handling

## 📱 Responsive Design

The application is fully responsive and works seamlessly across:
- Desktop computers
- Tablets
- Mobile phones

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 👥 Team

- **Vishal Sahu** - Initial work - [GitHub](https://github.com/Vishalsahu1510)
