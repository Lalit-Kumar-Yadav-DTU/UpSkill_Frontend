
# StudyNotion - EdTech Learning Platform

A full-stack MERN (MongoDB, Express, React, Node.js) application for an online learning platform with course management, user authentication, payment integration, and interactive learning features.

## 🎯 Project Overview

StudyNotion is a comprehensive EdTech platform that enables:
- User authentication and authorization
- Course creation and management
- Course enrollment and progress tracking
- Interactive course sections and subsections
- Student reviews and ratings
- Payment processing via Razorpay
- Email notifications and verification
- Responsive user dashboard
- Course catalog and search

## 🛠️ Tech Stack

### Frontend
- **React 18.2.0** - UI library
- **Redux & Redux Toolkit** - State management
- **React Router v6** - Client-side routing
- **Tailwind CSS** - Styling
- **Axios** - HTTP client
- **React Hook Form** - Form handling
- **React Hot Toast** - Notifications
- **Chart.js & React-ChartJS-2** - Data visualization
- **Swiper** - Carousel component
- **React Icons** - Icon library

### Backend
- **Node.js & Express.js** - Server framework
- **MongoDB & Mongoose** - Database
- **JWT** - Authentication
- **Razorpay** - Payment gateway
- **Cloudinary** - Image hosting
- **Nodemailer** - Email service
- **BCrypt** - Password hashing
- **Dotenv** - Environment variables

## 📁 Project Structure

```
EdTech Project/
├── src/                          # Frontend (React)
│   ├── components/               # React components
│   │   ├── Common/              # Shared components (Navbar, Footer, etc.)
│   │   └── core/                # Core feature components
│   │       ├── AboutPage/
│   │       ├── Auth/
│   │       ├── Catalog/
│   │       ├── ContactUsPage/
│   │       ├── Course/
│   │       ├── Dashboard/
│   │       ├── HomePage/
│   │       └── ViewCourse/
│   ├── pages/                    # Page components
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Signup.jsx
│   │   ├── Dashboard.jsx
│   │   ├── Catalog.jsx
│   │   ├── CourseDetails.jsx
│   │   ├── ViewCourse.jsx
│   │   ├── Contact.jsx
│   │   └── About.jsx
│   ├── services/                 # API services
│   │   ├── apiConnector.js       # Axios setup
│   │   ├── apis.js               # API endpoints
│   │   └── operations/           # API operations
│   │       └── authAPI.js
│   ├── slices/                   # Redux slices
│   │   ├── authSlice.js
│   │   ├── cartSlice.js
│   │   ├── courseSlice.js
│   │   ├── profileSlice.js
│   │   └── viewCourseSlice.js
│   ├── utils/                    # Utility functions
│   ├── hooks/                    # Custom React hooks
│   ├── data/                     # Static data
│   ├── assets/                   # Images, logos, etc.
│   └── App.jsx
├── server/                       # Backend (Node.js/Express)
│   ├── config/                   # Configuration files
│   │   ├── database.js           # MongoDB connection
│   │   ├── cloudinary.js         # Cloudinary setup
│   │   └── razorpay.js          # Razorpay setup
│   ├── controllers/              # Request handlers
│   │   ├── Auth.js              # Authentication logic
│   │   ├── Course.js            # Course management
│   │   ├── payments.js          # Payment processing
│   │   ├── RatingandReview.js   # Reviews and ratings
│   │   ├── Category.js          # Category management
│   │   ├── courseProgress.js    # Progress tracking
│   │   ├── profile.js           # User profile
│   │   ├── ContactUs.js         # Contact form
│   │   ├── Section.js           # Course sections
│   │   ├── Subsection.js        # Course subsections
│   │   ├── payments.js          # Payment handlers
│   │   └── resetPassword.js     # Password reset
│   ├── models/                   # Database schemas
│   │   ├── User.js
│   │   ├── Course.js
│   │   ├── Category.js
│   │   ├── Section.js
│   │   ├── Subsection.js
│   │   ├── CourseProgress.js
│   │   ├── RatingandReview.js
│   │   ├── OTP.js
│   │   └── Profile.js
│   ├── routes/                   # API routes
│   │   ├── user.js
│   │   ├── Course.js
│   │   ├── Payments.js
│   │   ├── Contact.js
│   │   └── profile.js
│   ├── middleware/               # Express middleware
│   │   └── auth.js              # Authentication middleware
│   ├── mail/                     # Email templates
│   │   └── templates/
│   │       ├── emailVerificationTemplate.js
│   │       ├── passwordUpdate.js
│   │       ├── courseEnrollmentEmail.js
│   │       ├── paymentSuccessEmail.js
│   │       └── contactFormRes.js
│   ├── utils/                    # Utility functions
│   │   ├── mailSender.js        # Email sending
│   │   ├── imageUploader.js     # Image upload to Cloudinary
│   │   └── secToDuration.js     # Time formatting
│   ├── index.js                  # Server entry point
│   └── package.json
├── public/                       # Static files
├── build/                        # Production build
├── package.json                  # Frontend dependencies
└── tailwind.config.js           # Tailwind CSS configuration
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14+)
- MongoDB database
- Cloudinary account
- Razorpay account
- SMTP credentials for email

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd EdTech\ Project
   ```

2. **Setup Frontend**
   ```bash
   npm install
   ```

3. **Setup Backend**
   ```bash
   cd server
   npm install
   ```

### Environment Variables

Create a `.env` file in the `server/` directory:

```env
# Database
MONGODB_URL=your_mongodb_connection_string

# Email Configuration
MAIL_HOST=your_smtp_host
MAIL_USER=your_email
MAIL_PASS=your_email_password
MAIL_FROM_EMAIL=your_email

# JWT
JWT_SECRET=your_jwt_secret

# Cloudinary
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Razorpay
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret

# Server Port
PORT=4000

# Frontend URL
FRONTEND_URL=http://localhost:3000
```

Create a `.env.local` file in the root directory for frontend:

```env
REACT_APP_API_BASE_URL=http://localhost:4000/api
```

## 📝 Available Scripts

### Frontend
```bash
# Start development server
npm start

# Build for production
npm build

# Run tests
npm test
```

### Backend
```bash
# Start server in development mode (with nodemon)
npm run dev

# Start server in production
npm start

# Install dependencies
npm run build
```

## ✨ Key Features

### Authentication
- User signup and login
- Email verification with OTP
- Password reset functionality
- JWT-based authorization
- Secure password hashing with bcrypt

### Course Management
- Create, update, and delete courses
- Organize courses into sections and subsections
- Upload course materials and videos
- Course categories and filtering
- Course search and catalog

### Learning Experience
- Interactive course viewing
- Video streaming support
- Course progress tracking
- Subsection completion tracking
- Course ratings and reviews

### User Dashboard
- Personal profile management
- Enrolled courses view
- Learning progress analytics
- Wishlist management
- Purchase history

### Payments
- Razorpay payment gateway integration
- Order creation and tracking
- Payment verification
- Receipt generation
- Email confirmation

### Notifications
- Email verification
- Course enrollment confirmation
- Payment success emails
- Password update notifications
- Contact form responses

### File Management
- Image upload via Cloudinary
- Video hosting support
- Responsive image optimization

## 🔐 Security Features

- Password encryption with bcrypt
- JWT-based authentication
- Protected API routes with middleware
- CORS configuration
- Environment variable protection
- Input validation and sanitization

## 📊 Database Models

- **User** - User account information
- **Course** - Course details and metadata
- **Section** - Course sections
- **Subsection** - Lesson content within sections
- **Category** - Course categories
- **CourseProgress** - Student progress tracking
- **RatingandReview** - Student reviews
- **OTP** - Email verification tokens
- **Profile** - Extended user profile information

## 🎨 UI/UX Features

- Responsive design with Tailwind CSS
- Interactive charts and visualizations
- Toast notifications
- Modal confirmations
- Form validation
- Loading states
- Error handling

## 📚 API Documentation

The backend provides RESTful API endpoints for:

- **Authentication**: `/api/v1/auth/*`
- **Courses**: `/api/v1/courses/*`
- **User Profile**: `/api/v1/profile/*`
- **Payments**: `/api/v1/payments/*`
- **Contact**: `/api/v1/contact/*`

## 🤝 Contributing

1. Create a new branch for your feature
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 📄 License

ISC License

## 🙋 Support

For issues and questions, please open an issue in the repository or contact the development team.

---

**Happy Learning! 🎓**





