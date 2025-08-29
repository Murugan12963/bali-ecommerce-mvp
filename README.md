# Bali E-Commerce MVP

A modern, responsive e-commerce website specializing in authentic Bali-themed products through dropshipping. Built with Next.js, Node.js, and Stripe, targeting global nomads and eco-conscious consumers.

## 🌺 Project Overview

This MVP delivers a complete e-commerce solution featuring:
- Responsive product catalog with Bali-themed products
- Shopping cart with session persistence
- Secure Stripe payment integration
- Automated order processing and supplier communication
- Admin dashboard for product management
- SEO optimization and performance focus
- Customer support integration

## 🚀 Tech Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **TypeScript** - Type safety and better DX
- **Tailwind CSS** - Utility-first CSS framework
- **Stripe Elements** - Secure payment processing

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB/PostgreSQL** - Database (configurable)
- **Prisma/Mongoose** - ORM/ODM

### Development & Testing
- **Jest** - Unit testing
- **Playwright** - E2E testing
- **ESLint/Prettier** - Code quality and formatting
- **Husky** - Git hooks

## 📦 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn
- MongoDB or PostgreSQL database
- Stripe account for payments

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Murugan12963/bali-ecommerce-mvp.git
cd bali-ecommerce-mvp
```

2. **Install dependencies**
```bash
# Frontend dependencies
cd frontend
npm install

# Backend dependencies  
cd ../backend
npm install
```

3. **Environment setup**
```bash
# Copy environment template
cp .env.example .env.local

# Configure your environment variables (see Configuration section)
```

4. **Database setup**
```bash
# For MongoDB
npm run db:seed

# For PostgreSQL with Prisma
npx prisma migrate dev
npx prisma db seed
```

5. **Start development servers**
```bash
# Frontend (runs on http://localhost:3000)
cd frontend
npm run dev

# Backend (runs on http://localhost:8000)  
cd backend
npm run dev
```

## ⚙️ Configuration

Copy `.env.example` to `.env.local` and configure:

```env
# Database
MONGODB_URI=mongodb://localhost:27017/bali-ecommerce
# or
DATABASE_URL=postgresql://user:pass@localhost:5432/bali-ecommerce

# Stripe
STRIPE_PUBLISHABLE_KEY=pk_test_...
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...

# Email
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password

# Authentication
JWT_SECRET=your-jwt-secret
JWT_EXPIRES_IN=7d

# Analytics
NEXT_PUBLIC_GA_TRACKING_ID=G-...
```

## 🧪 Testing

```bash
# Run all tests
npm test

# Run tests with coverage
npm run test:coverage

# Run E2E tests
npm run test:e2e

# Run Lighthouse audit
npm run lighthouse
```

## 📁 Project Structure

```
├── frontend/              # Next.js application
│   ├── components/        # React components
│   ├── pages/            # Next.js pages and API routes
│   ├── lib/              # Utility libraries
│   ├── types/            # TypeScript definitions
│   └── styles/           # CSS and styling
├── backend/              # Express.js API
│   ├── models/           # Data models
│   ├── routes/           # API routes
│   ├── services/         # Business logic
│   └── middleware/       # Express middleware
├── tests/                # Test suites
│   ├── frontend/         # Frontend tests
│   ├── backend/          # Backend tests
│   └── e2e/             # End-to-end tests
└── docs/                 # Documentation
```

## 🎯 Development Workflow

1. **Feature Development**
   - Create feature branch from `main`
   - Implement feature with tests
   - Run validation checks
   - Submit PR for review

2. **Quality Gates**
   ```bash
   npm run lint              # Code quality
   npm run type-check        # TypeScript validation  
   npm test                  # Unit tests
   npm run test:e2e          # Integration tests
   ```

3. **Performance Targets**
   - Lighthouse Performance: 90+
   - Lighthouse SEO: 95+
   - Page Load Time: <2s
   - Test Coverage: 80%+

## 🚢 Deployment

### Production Deployment (Vercel)
```bash
# Deploy to Vercel
npm run build
vercel --prod
```

### Docker Deployment
```bash
# Build and run with Docker
docker-compose up --build
```

## 📊 Key Features

- **Product Catalog**: Filterable grid with lazy-loaded images
- **Shopping Cart**: Persistent cart with real-time updates  
- **Checkout Flow**: Secure Stripe integration with validation
- **Order Management**: Automated supplier notifications
- **Admin Dashboard**: Product and order management
- **SEO Optimized**: Meta tags, structured data, sitemap
- **Mobile First**: Responsive design for all devices

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by authentic Balinese craftsmanship
- Built for the global nomad and eco-conscious community
- Powered by modern web technologies

---

**Live Demo**: Coming soon 🚀  
**Documentation**: [View Docs](./docs/)  
**Issues**: [Report Bug](https://github.com/Murugan12963/bali-ecommerce-mvp/issues)
