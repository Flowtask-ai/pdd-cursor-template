# 🛠️ How to Customize PDD Template for Your Stack

## 🎯 Overview

This PDD template comes with **Python/FastAPI/React** specialization out of the box. Here's how to adapt it for your specific tech stack and team conventions.

## 📋 Current Specialization

**Default Stack:**
- **Backend**: Python 3.11+ with FastAPI
- **Frontend**: React 18 with TypeScript
- **Database**: PostgreSQL with SQLAlchemy 2.0
- **Testing**: pytest + Playwright
- **Architecture**: Domain-Driven Design (DDD)
- **Code Style**: PEP8, Black, isort

## 🚀 Quick Start Customization

### Option 1: Use Customization Examples
Check `customization-examples/` for ready-to-use adaptations:
- `nodejs-express-react/` - Node.js + Express + React
- `java-spring-vue/` - Java + Spring Boot + Vue.js
- `dotnet-aspnet-angular/` - .NET + ASP.NET Core + Angular

### Option 2: Manual Customization
Follow the steps below to adapt the template to your stack.

## 📝 Step-by-Step Customization

### 1. Identify Your Tech Stack

**Backend Framework:**
- [ ] Python/FastAPI → [Your Backend Framework]
- [ ] Update `.cursor/rules/core-rules/02-backend-development.mdc`

**Frontend Framework:**
- [ ] React/TypeScript → [Your Frontend Framework]
- [ ] Update `.cursor/rules/core-rules/03-frontend-development.mdc`

**Database:**
- [ ] PostgreSQL/SQLAlchemy → [Your Database/ORM]
- [ ] Update database patterns in code examples

**Testing:**
- [ ] pytest/Playwright → [Your Testing Stack]
- [ ] Update `.cursor/rules/core-rules/04-testing-strategy.mdc`

### 2. Update Core Rules

#### Backend Development Rules
**File**: `.cursor/rules/core-rules/02-backend-development.mdc`

**What to change:**
- Framework-specific patterns
- Database ORM conventions
- API design patterns
- Error handling approaches
- Authentication/authorization patterns

**Example for Node.js/Express:**
```markdown
### Express.js (Node.js)
- Use Express.js for API development
- Implement middleware pattern
- Use JWT for authentication
- Follow RESTful conventions
- Use Mongoose for MongoDB
```

#### Frontend Development Rules
**File**: `.cursor/rules/core-rules/03-frontend-development.mdc`

**What to change:**
- Component architecture
- State management patterns
- Routing conventions
- UI library patterns
- Build tool configurations

#### Testing Strategy
**File**: `.cursor/rules/core-rules/04-testing-strategy.mdc`

**What to change:**
- Testing frameworks
- Mocking strategies
- E2E testing tools
- Coverage requirements
- Test organization patterns

### 3. Replace Code Examples

**Directory**: `.cursor/rules/code-examples/`

**Files to update:**
- `01-domain.mdc` - Domain models and business logic
- `02-backend.mdc` - API endpoints and services
- `03-frontend.mdc` - UI components and hooks
- `04-testing.mdc` - Test examples and patterns
- `05-quality.mdc` - Code quality tools and configs
- `06-ci-cd.mdc` - Pipeline configurations

**Example for Node.js:**
```javascript
// 02-backend.mdc - Express.js Controller
const express = require('express');
const router = express.Router();

router.get('/users', async (req, res) => {
  try {
    const users = await User.find();
    res.json(users);
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
});
```

### 4. Update Global Rules

**File**: `.cursor/rules/core-rules/00-global-rules.mdc`

**What to change:**
- Language-specific conventions
- File organization patterns
- Naming conventions
- Documentation standards

### 5. Adapt Commands

**Directory**: `.cursor/rules/commands/`

**Files to update:**
- `01-generate-prp.mdc` - Update validation patterns
- `02-execute-prp.mdc` - Update execution commands

## 🔧 Technology-Specific Adaptations

### For Node.js/Express Projects
- **Package Manager**: npm/yarn/pnpm
- **Testing**: Jest + Supertest
- **Database**: MongoDB/Mongoose or PostgreSQL/Sequelize
- **Validation**: Joi or Yup
- **Authentication**: Passport.js + JWT

### For Java/Spring Projects
- **Build Tool**: Maven or Gradle
- **Testing**: JUnit 5 + Mockito
- **Database**: JPA/Hibernate
- **Validation**: Bean Validation
- **Authentication**: Spring Security

### For .NET Projects
- **Framework**: ASP.NET Core
- **Testing**: xUnit + Moq
- **Database**: Entity Framework Core
- **Validation**: FluentValidation
- **Authentication**: ASP.NET Core Identity

## 📊 Validation Checklist

After customization, verify:

- [ ] **Core rules** reflect your tech stack
- [ ] **Code examples** use your frameworks
- [ ] **Testing patterns** match your tools
- [ ] **Quality standards** align with your team
- [ ] **Commands** work with your setup
- [ ] **Documentation** is updated

## 🎯 Best Practices

### 1. Keep It Consistent
- Use the same patterns throughout all rules
- Maintain consistent naming conventions
- Follow your team's established practices

### 2. Include Real Examples
- Use actual code patterns from your projects
- Include common scenarios and edge cases
- Show both simple and complex implementations

### 3. Document Assumptions
- Clearly state what the rules assume
- Include prerequisites and dependencies
- Explain why certain patterns are chosen

### 4. Test Your Customization
- Generate a PRP with your new rules
- Execute it to ensure it works correctly
- Validate that the output matches expectations

## 🆘 Need Help?

1. **Check customization examples** in `customization-examples/`
2. **Review the original rules** to understand the structure
3. **Start with one area** (e.g., backend) and expand gradually
4. **Test incrementally** to catch issues early

## 📚 Resources

- [Cursor Rules Documentation](https://docs.cursor.com/context/rules)
- [PDD Methodology Guide](PDD/USAGE_GUIDE.md)
- [Original Template Repository](https://github.com/Flowtask-ai/pdd-cursor-template)

---

**Remember**: The goal is to make PDD work seamlessly with your existing development practices, not to force you into new patterns that don't fit your team. 