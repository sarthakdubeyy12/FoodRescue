# 🍽️ FoodRescue - Connecting Compassion with Technology

> **"Har thali bhar jaaye, har pet muskaraaye"** - *Let every plate be full, let every stomach smile*

[![React](https://img.shields.io/badge/React-19.1.0-61DAFB?logo=react)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-5.1.0-339933?logo=node.js)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.17.0-47A248?logo=mongodb)](https://mongodb.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4.17-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)
[![Express](https://img.shields.io/badge/Express-5.1.0-000000?logo=express)](https://expressjs.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🌟 Overview

**FoodRescue** is a comprehensive food donation and redistribution platform that connects donors, volunteers, and shelters to combat food waste and hunger. Built with modern web technologies, it provides a seamless experience for managing food donations from creation to delivery.

### 🎯 Mission
To create a sustainable ecosystem where surplus food reaches those who need it most, reducing waste while feeding communities with dignity and respect.

### 📊 Impact
- **Multi-role user system** supporting donors, volunteers, shelters, and administrators
- **Real-time tracking** of food donations from pickup to delivery
- **Comprehensive analytics** for impact measurement

## ✨ Key Features

### 🏠 **Multi-Role Dashboard System**
- **Donor Dashboard**: Track donations, manage pickups, view delivery status
- **Volunteer Dashboard**: Claim donations, manage deliveries, track routes
- **Shelter Dashboard**: Receive donations, acknowledge deliveries, provide feedback
- **Admin Dashboard**: User management, analytics, system oversight

### 🍱 **Food Donation Management**
- Create detailed food donation listings with expiry times
- Real-time status tracking (pending → claimed → in-transit → delivered)
- Location-based pickup coordination
- Expiry time management to ensure food safety

### 📱 **User Experience**
- Responsive design optimized for all devices
- Intuitive navigation with role-based access
- Real-time notifications and status updates
- Professional UI with Tailwind CSS

### 📊 **Analytics & Reporting**
- Interactive charts and graphs using Recharts
- Donation status overview with visual analytics
- User role distribution statistics
- Delivery time tracking and optimization

### 🔐 **Security & Authentication**
- JWT-based authentication system
- Role-based access control (RBAC)
- Secure password hashing with bcrypt
- Protected API endpoints

### 💳 **Payment Integration**
- Razorpay integration for monetary donations
- Secure payment processing
- Transaction history tracking

## 🛠️ Technology Stack

### Frontend
- **React 19.1.0** - Modern UI framework
- **React Router DOM 7.6.2** - Client-side routing
- **Tailwind CSS 3.4.17** - Utility-first CSS framework
- **Recharts 2.15.4** - Interactive charts and graphs
- **Axios 1.10.0** - HTTP client for API communication
- **React Icons 5.5.0** - Icon library
- **React DatePicker 8.4.0** - Date selection components

### Backend
- **Node.js 5.1.0** - JavaScript runtime
- **Express.js 5.1.0** - Web application framework
- **MongoDB 6.17.0** - NoSQL database
- **Mongoose 8.15.2** - MongoDB object modeling
- **JWT 9.0.2** - JSON Web Token authentication
- **bcrypt 6.0.0** - Password hashing
- **Razorpay 2.9.6** - Payment gateway integration

### Development Tools
- **Nodemon 3.1.10** - Development server with auto-restart
- **CRACO 5.9.0** - Create React App Configuration Override
- **ESLint** - Code linting and formatting

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/foodrescue.git
   cd foodrescue
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

4. **Environment Setup**
   
   Create `.env` file in the server directory:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   RAZORPAY_KEY_ID=your_razorpay_key_id
   RAZORPAY_KEY_SECRET=your_razorpay_secret_key
   PORT=5000
   ```

5. **Start the development servers**

   **Terminal 1 - Backend:**
   ```bash
   cd server
   npm run dev
   ```

   **Terminal 2 - Frontend:**
   ```bash
   cd client
   npm start
   ```

6. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000

## 📁 Project Structure

```
FoodRescue/
├── client/                 # React frontend
│   ├── public/            # Static assets
│   ├── src/
│   │   ├── components/    # React components
│   │   │   ├── pages/     # Page components
│   │   │   └── ...
│   │   ├── context/       # React context
│   │   └── api.js         # API configuration
│   └── package.json
├── server/                # Node.js backend
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/          # MongoDB schemas
│   ├── routes/          # API routes
│   └── server.js        # Server entry point
└── README.md
```

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user

### Food Donations
- `POST /api/food/create` - Create food donation
- `GET /api/food/recent` - Get recent donations
- `GET /api/food/available` - Get available donations
- `PATCH /api/food/claim/:id` - Claim donation
- `PATCH /api/food/:id/delivered` - Mark as delivered

### Admin
- `GET /api/admin/users` - Get all users
- `GET /api/admin/donations` - Get all donations
- `PATCH /api/admin/approve-user/:id` - Approve user

### Payments
- `POST /api/payment/create` - Create payment
- `POST /api/payment/verify` - Verify payment

## 👥 User Roles & Permissions

### 🏠 **Donor**
- Create food donations
- Track donation status
- View delivery confirmations
- Manage donation history

### 🚚 **Volunteer**
- Browse available donations
- Claim donations for pickup
- Update delivery status
- Track delivery routes

### 🏘️ **Shelter**
- Receive incoming donations
- Acknowledge deliveries
- Provide feedback
- Manage inventory

### 👨‍💼 **Admin**
- User management and approval
- System analytics and reporting
- Donation oversight
- Platform configuration

## 📊 Dashboard Features

### Admin Dashboard
- **User Analytics**: Role distribution, approval status
- **Donation Analytics**: Status overview, delivery times
- **System Metrics**: Total users, completed deliveries
- **User Management**: Approve users, view profiles
- **Donation Management**: Monitor all donations

### Role-Specific Dashboards
- **Donor**: My donations, pickup requests, delivery status
- **Volunteer**: Available pickups, claimed donations, delivery tracking
- **Shelter**: Incoming donations, delivery acknowledgments

## 🎨 UI/UX Highlights

- **Responsive Design**: Optimized for desktop, tablet, and mobile
- **Modern Interface**: Clean, intuitive design with Tailwind CSS
- **Interactive Charts**: Data visualization with Recharts
- **Smooth Animations**: Enhanced user experience
- **Accessibility**: WCAG compliant design patterns

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: bcrypt for secure password storage
- **CORS Protection**: Cross-origin resource sharing security
- **Input Validation**: Server-side validation for all inputs
- **Role-Based Access**: Granular permission system

## 🚀 Deployment

### Frontend (Vercel)
```bash
cd client
npm run build
# Deploy build folder to Vercel
```

### Backend (Heroku/Railway)
```bash
cd server
# Set environment variables
npm start
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Follow ESLint configuration
- Write meaningful commit messages
- Test your changes thoroughly
- Update documentation as needed

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **React Team** for the amazing framework
- **Tailwind CSS** for the utility-first CSS framework
- **MongoDB** for the flexible database solution
- **Razorpay** for payment integration
- **Open Source Community** for inspiration and support


---

<div align="center">

**Built with ❤️ for a hunger-free world**

*"Main badlaav lana chahta hoon. Apne code se, apni soch se — ek behtar kal ke liye."*

*"I want to bring change. Through my code, through my thoughts — for a better tomorrow."*

</div> 
