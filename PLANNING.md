# Bali E-Commerce MVP - Project Planning

## 🎯 Project Overview

**Name**: Bali-Themed Dropshipping E-Commerce Website MVP  
**Goal**: Create a production-ready e-commerce platform for authentic Bali-themed products  
**Timeline**: 2-4 weeks for MVP completion  
**Target Users**: Global nomads and eco-conscious consumers

## 🏗️ Architecture & Structure

### Tech Stack
- **Frontend**: Next.js 14 + TypeScript + Tailwind CSS
- **Backend**: Node.js + Express + TypeScript  
- **Database**: MongoDB (primary) / PostgreSQL (alternative)
- **Payments**: Stripe integration
- **Caching**: Redis for sessions and performance
- **Email**: Nodemailer with SMTP
- **Testing**: Jest + Playwright + Testing Library
- **Deployment**: Vercel (frontend) + Docker containers

### Code Organization Principles
- **Monorepo structure** with separate frontend/backend packages
- **Modular architecture** - max 500 lines per file
- **Feature-based grouping** for components and services
- **Consistent naming conventions** throughout codebase
- **Type-safe development** with comprehensive TypeScript usage

### File Structure Rules
```
├── frontend/
│   ├── components/          # React components by feature
│   │   ├── Layout/         # Header, Footer, Navigation
│   │   ├── Product/        # Product catalog components  
│   │   ├── Cart/           # Shopping cart functionality
│   │   └── UI/             # Reusable UI components
│   ├── pages/              # Next.js pages and API routes
│   ├── lib/                # Utility functions and configurations
│   └── types/              # TypeScript type definitions
├── backend/
│   ├── models/             # Data models (Product, Order, User)
│   ├── routes/             # API route handlers
│   ├── services/           # Business logic layer
│   └── middleware/         # Express middleware
└── tests/                  # Test files mirroring app structure
```

## 🎨 Design System & Style Guide

### Bali-Inspired Color Palette
- **Primary**: Orange (#ed8936) - Representing Balinese sunsets
- **Secondary**: Ocean Blue (#0ea5e9) - Reflecting island waters
- **Earth Tones**: Warm browns and tans (#d49870) - Natural materials
- **Nature Green**: (#22c55e) - Lush vegetation
- **Accent Gray**: (#64748b) - Modern neutral

### Component Patterns
- **Consistent spacing**: Use Tailwind's spacing scale
- **Responsive design**: Mobile-first approach
- **Accessible components**: WCAG 2.1 AA compliance
- **Performance-focused**: Lazy loading and optimization
- **Reusable patterns**: Button, Card, Input field variants

## 🛠️ Development Standards

### Code Quality Rules
- **Follow PEP8 equivalent**: ESLint + Prettier for formatting
- **Type annotations**: Full TypeScript coverage
- **Function documentation**: Google-style docstrings for all functions
- **Error handling**: Comprehensive try-catch blocks
- **Environment variables**: Use .env for all configuration

### Testing Requirements
- **Unit tests**: Jest for components and functions
- **Integration tests**: API endpoint testing
- **E2E tests**: Playwright for user journeys
- **Coverage target**: 80%+ test coverage
- **Test structure**: Mirror main app directory structure

### Performance Targets
- **Lighthouse Performance**: 90+
- **Lighthouse SEO**: 95+
- **Page Load Time**: <2 seconds
- **Bundle Size**: Optimized with tree-shaking
- **Image Optimization**: Next.js Image component usage

## 🔄 Workflow & Constraints

### Development Process
1. **Feature Planning**: Add tasks to TASK.md before starting
2. **Branch Strategy**: Feature branches from main
3. **Code Review**: All changes via pull requests
4. **Quality Gates**: Lint, type-check, test before merge
5. **Documentation**: Update README.md for new features

### Module Organization
- **Agent Pattern**: For complex business logic
  - `agent.py` - Main logic and execution
  - `tools.py` - Utility functions  
  - `prompts.py` - Templates and messaging
- **Database Layer**: Models with proper validation
- **API Layer**: RESTful endpoints with proper error handling
- **Service Layer**: Business logic separation

### Technology Constraints
- **Python Environment**: Use venv_linux for all Python commands
- **File Size Limit**: Maximum 500 lines per file
- **Import Strategy**: Prefer relative imports within packages
- **Database**: Pydantic for data validation
- **API Framework**: FastAPI for backend APIs
- **ORM**: SQLAlchemy or SQLModel for database operations

## 🎯 Success Criteria

### Functional Requirements
- [ ] Product catalog with filtering and search
- [ ] Shopping cart with session persistence  
- [ ] Secure checkout with Stripe integration
- [ ] Automated order processing and supplier notification
- [ ] Admin dashboard for product/order management
- [ ] SEO optimization with meta tags and structured data
- [ ] Mobile-responsive design

### Technical Requirements
- [ ] Sub-2 second page load times
- [ ] 90+ Lighthouse performance score
- [ ] 95+ Lighthouse SEO score
- [ ] 80%+ test coverage
- [ ] Zero linting errors
- [ ] Full TypeScript type coverage
- [ ] Comprehensive error handling

### Business Requirements
- [ ] Automated dropshipping workflow
- [ ] Multi-supplier order routing
- [ ] Customer email confirmations
- [ ] Inventory management integration
- [ ] Analytics and tracking setup
- [ ] Customer support integration

## 🚨 Risk Mitigation

### Development Risks
- **Scope Creep**: Stick to MVP features only
- **Performance Issues**: Regular Lighthouse audits
- **Security Vulnerabilities**: Security headers and validation
- **Integration Failures**: Comprehensive API testing

### Business Risks  
- **Supplier Dependencies**: Email fallback for API failures
- **Payment Issues**: Stripe test mode validation
- **Compliance**: Indonesian e-commerce regulations (PSE)
- **Scalability**: Database indexing and caching strategy

---

**Next Steps**: Review TASK.md for immediate action items and development priorities.
