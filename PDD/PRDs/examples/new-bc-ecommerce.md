# New Bounded Context: E-commerce Platform

## 🎯 Project Overview
**BC Name**: E-commerce Platform
**Purpose**: Create a complete online shopping platform that allows users to browse products, manage accounts, and complete purchases securely
**Scope**: Complete project with frontend and backend

## 🏗️ Architecture Requirements
**Frontend**: React 18 with TypeScript, Tailwind CSS
**Backend**: FastAPI with Python 3.11+
**Database**: PostgreSQL 15 with SQLAlchemy 2.0
**Infrastructure**: Docker containers, AWS deployment
**Deployment**: GitHub Actions CI/CD, AWS ECS

## ✨ Core Features
1. **User Management**: Registration, login, profile management, password reset
2. **Product Catalog**: Product browsing, search, filtering, categories
3. **Shopping Cart**: Add/remove items, quantity management, cart persistence
4. **Checkout Process**: Address management, payment integration, order confirmation
5. **Order Management**: Order history, tracking, status updates
6. **Admin Panel**: Product management, order processing, user management

## 🔗 External Integrations
- **Stripe API**: Payment processing and subscription management
- **SendGrid API**: Email notifications and marketing emails
- **AWS S3**: Product image storage and CDN delivery

## 📊 Data Models
- **User**: id, email, password_hash, first_name, last_name, created_at, updated_at
- **Product**: id, name, description, price, stock, category_id, images, created_at
- **Category**: id, name, description, parent_id
- **Cart**: id, user_id, created_at, updated_at
- **CartItem**: id, cart_id, product_id, quantity
- **Order**: id, user_id, status, total_amount, shipping_address, created_at
- **OrderItem**: id, order_id, product_id, quantity, price_at_time

## 🔐 Security Requirements
- JWT-based authentication with refresh tokens
- Role-based authorization (customer, admin)
- Password hashing with bcrypt
- HTTPS enforcement
- Input validation and sanitization
- Rate limiting on API endpoints

## 📱 User Interface
- **Homepage**: Featured products, categories, search bar
- **Product Pages**: Product details, images, reviews, add to cart
- **User Dashboard**: Profile, orders, wishlist
- **Checkout Flow**: Cart review, address, payment, confirmation
- **Admin Dashboard**: Product management, order processing, analytics

## 🧪 Testing Strategy
- Unit tests with pytest for all business logic
- Integration tests for API endpoints
- E2E tests with Playwright for critical user flows
- Performance testing with locust
- Security testing with OWASP ZAP

## 📚 Examples to Follow
- Check `PDD/PRDs/examples/` for similar project examples
- Review `.cursor/rules/code-examples/` for implementation patterns
- Reference `PDD/customization-examples/` for your specific tech stack

## 📖 Documentation
- FastAPI: https://fastapi.tiangolo.com/
- React: https://react.dev/
- SQLAlchemy: https://docs.sqlalchemy.org/
- Stripe API: https://stripe.com/docs/api
- AWS ECS: https://docs.aws.amazon.com/ecs/

## 🎯 Success Criteria
- [ ] MVP features implemented (user auth, product catalog, cart, checkout)
- [ ] All tests passing with >90% coverage
- [ ] Documentation complete (API docs, deployment guide)
- [ ] Deployment working on AWS
- [ ] Performance benchmarks met (<2s page load, <500ms API response)
- [ ] Security audit passed
- [ ] Payment processing working with Stripe 