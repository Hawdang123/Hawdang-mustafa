# CCTV Experts QR

A modern, full-stack service management system for CCTV installation and maintenance companies with integrated QR code tracking.

## 🚀 Features

### Authentication & Authorization
- Secure JWT-based authentication
- Role-based access control (Admin, Technician, Customer)
- Forgot password functionality
- Registration with email verification

### Customer Features
- Request CCTV installation/maintenance
- View quotations and track service status
- Appointment scheduling
- Payment history and invoice downloads
- Chat with technicians
- View installed devices and warranty info

### Admin Features
- Comprehensive dashboard analytics
- Customer and technician management
- Product inventory management
- Installation request assignment
- Sales and service reports
- QR code management

### Technician Features
- Daily job assignments
- Customer location navigation
- Installation progress tracking
- Photo uploads (before/after)
- QR code scanning for device updates
- Digital signature capture
- Job completion reports

### QR Code Integration
- Unique QR codes for each CCTV device
- Device information display
- Maintenance and repair history tracking
- Warranty status monitoring
- One-click maintenance requests

## 🛠 Tech Stack

**Frontend:**
- React 18 with TypeScript
- Tailwind CSS for styling
- Shadcn UI component library
- React Router for navigation
- Zustand for state management
- Axios for API calls

**Backend:**
- Node.js with Express.js
- PostgreSQL database
- JWT authentication
- Multer for file uploads
- QR-code library for QR generation

**Infrastructure:**
- Cloudinary for image storage
- Google Maps API for location services
- Environment-based configuration

## 📁 Project Structure

```
CCTV-Installation/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Page components
│   │   ├── hooks/         # Custom hooks
│   │   ├── services/      # API services
│   │   ├── store/         # Zustand store
│   │   ├── types/         # TypeScript types
│   │   ├── utils/         # Utility functions
│   │   └── App.tsx
│   └── package.json
├── server/                # Express backend
│   ├── src/
│   │   ├── controllers/   # Route controllers
│   │   ├── models/        # Database models
│   │   ├── routes/        # API routes
│   │   ├── middleware/    # Custom middleware
│   │   ├── services/      # Business logic
│   │   ├── utils/         # Utility functions
│   │   └── server.ts
│   ├── prisma/            # Database schema
│   └── package.json
└── docs/                  # Documentation
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- PostgreSQL 12+
- npm or yarn

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Gabiriyel/CCTV-Installation.git
cd CCTV-Installation
```

2. **Setup Backend**
```bash
cd server
npm install
cp .env.example .env
npm run prisma:migrate
npm run dev
```

3. **Setup Frontend**
```bash
cd client
npm install
cp .env.example .env
npm run dev
```

4. **Access the application**
- Frontend: http://localhost:5173
- Backend API: http://localhost:3000

## 📝 Environment Variables

### Server
```
DATABASE_URL=postgresql://user:password@localhost:5432/cctv_experts
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
GOOGLE_MAPS_API_KEY=your_maps_key
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_email_password
```

### Client
```
VITE_API_URL=http://localhost:3000
VITE_GOOGLE_MAPS_KEY=your_maps_key
```

## 📊 Database Schema

The application uses Prisma ORM with PostgreSQL. Key entities include:

- **Users** - Authentication and profiles
- **Customers** - Customer information
- **Technicians** - Technician profiles and availability
- **Products** - CCTV products catalog
- **Installations** - Installation records with location
- **QRCodes** - Unique QR codes for devices
- **MaintenanceRecords** - Maintenance history
- **RepairRecords** - Repair history
- **Appointments** - Scheduled appointments
- **Invoices** - Billing information
- **Payments** - Payment records
- **Inventory** - Stock management
- **Notifications** - System notifications

## 🔐 Security Features

- JWT token-based authentication
- Role-based access control (RBAC)
- Password hashing with bcrypt
- CORS configuration
- Rate limiting
- Input validation and sanitization
- Secure file upload handling

## 📱 Responsive Design

- Mobile-first approach
- Tailwind CSS responsive utilities
- Optimized for all screen sizes
- Touch-friendly interface
- Fast performance on mobile networks

## 🎨 UI/UX Highlights

- Glassmorphism design cards
- Smooth animations and transitions
- Dark/Light mode support
- Professional blue, white, and gray color scheme
- Intuitive navigation
- Enterprise-level polish

## 📚 API Documentation

API endpoints are organized by resource:

- `/api/auth` - Authentication
- `/api/customers` - Customer management
- `/api/technicians` - Technician management
- `/api/products` - Product management
- `/api/installations` - Installation management
- `/api/qr-codes` - QR code management
- `/api/maintenance` - Maintenance records
- `/api/appointments` - Appointment scheduling
- `/api/invoices` - Invoice management
- `/api/reports` - Analytics and reports

## 🧪 Testing

```bash
# Run backend tests
cd server
npm run test

# Run frontend tests
cd client
npm run test
```

## 🚀 Deployment

### Frontend Deployment (Vercel)
```bash
cd client
npm run build
vercel deploy
```

### Backend Deployment (Railway/Heroku)
```bash
cd server
npm run build
# Deploy to your hosting platform
```

## 📄 License

This project is proprietary and confidential.

## 👥 Contributors

- Development team for CCTV Experts

## 📞 Support

For issues and questions, please contact the development team.

---

**Version:** 1.0.0  
**Last Updated:** 2024
