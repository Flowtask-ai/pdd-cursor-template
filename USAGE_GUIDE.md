# 🚀 Practical Guide: How to Use PDD

A step-by-step guide to use this template and apply the PDD (Prompt Driven Design) methodology in your projects.

## 📋 Table of Contents

1. [Project Structure](#project-structure)
2. [Initial Setup](#initial-setup)
3. [Basic Workflow](#basic-workflow)
4. [Specific Use Cases](#specific-use-cases)
5. [Troubleshooting](#troubleshooting)

---

## 📁 Project Structure

Understanding the template structure is crucial for effective use. Here's what each folder and file contains:

```
pdd-cursor-template/
├── 📄 README.md                    # Main documentation and overview
├── 📄 USAGE_GUIDE.md              # This guide - step-by-step instructions
├── 📄 GLOBAL_RULES.md             # Human-readable project rules and conventions
├── 📄 LICENSE                     # MIT License (Flowtask-ai + Cole Medin attribution)
├── 📄 package.json                # Project metadata and dependencies
│
├── 📁 .cursor/
│   └── 📁 rules/                  # Cursor Rules (automatic AI context)
│       ├── 📄 00-project-global.mdc      # Global project rules for AI
│       ├── 📄 01-feature-request.mdc     # Rules for feature request interpretation
│       ├── 📄 02-prp-generator.mdc       # Rules for PRP generation
│       ├── 📄 03-prp-executor.mdc        # Rules for PRP execution
│       ├── 📁 roles/                     # Specialized AI roles
│       │   ├── 📄 01-architect.mdc       # Architecture-focused AI behavior
│       │   └── 📄 02-developer.mdc       # Development-focused AI behavior
│       └── 📁 templates/                 # AI templates
│           └── 📄 prp-base.mdc           # Base template for PRP generation
│
├── 📁 PDD/                        # Prompt Driven Design
│   ├── 📁 PRDs/                   # Product Requirements Documents
│   │   ├── 📁 templates/          # Templates for each use case
│   │   │   ├── 📄 new-bc-XXX.md   # Template for new bounded contexts
│   │   │   ├── 📄 new-feature-YYY-bc-XXX.md  # Template for new features
│   │   │   └── 📄 improve-bc-XXX.md  # Template for BC improvements
│   │   ├── 📁 examples/           # Filled examples for inspiration
│   │   │   ├── 📄 new-bc-ecommerce.md # Example: Complete e-commerce project
│   │   │   ├── 📄 new-feature-notifications-bc-auth.md  # Example: Notifications feature
│   │   │   └── 📄 improve-bc-auth.md  # Example: Auth system improvements
│   │   └── (Your PRDs will appear here)
│   │
│   └── 📁 PRPs/                   # Product Requirements Prompts (generated)
│       ├── 📁 templates/          # Templates for PRPs
│       │   └── 📄 prp-base.mdc    # Base template for generating PRPs
│       ├── 📁 commands/           # Commands for generate/execute PRPs
│       │   ├── 📄 generate-prp.md # Prompt to generate a PRP
│       │   └── 📄 execute-prp.md  # Prompt to execute a PRP
│       └── (Your generated PRPs will appear here)
│
└── 📁 .github/                    # GitHub configuration
    └── 📁 ISSUE_TEMPLATE/         # Issue templates for contributions
        ├── 📄 bug_report.md       # Template for bug reports
        └── 📄 feature_request.md  # Template for feature requests
```

### 🔑 Key Files Explained:

#### **📄 Core Documentation**
- **`README.md`**: Main project overview, methodology explanation, and quick start
- **`USAGE_GUIDE.md`**: Detailed step-by-step instructions (this file)
- **`GLOBAL_RULES.md`**: Human-readable rules that mirror the AI rules

#### **📄 Templates & Examples**
- **`PDD/PRDs/templates/`**: Templates for each use case (new BC, new feature, improve BC)
- **`PDD/PRDs/examples/`**: Filled examples for inspiration and reference
- **`.cursor/rules/pattern-examples/`**: Code patterns and reference implementations

#### **🤖 AI Configuration**
- **`.cursor/rules/`**: Automatic context for Cursor's AI (always active)
- **`PDD/PRPs/commands/`**: Manual prompts you can copy-paste to trigger specific actions
- **`PDD/PRPs/`**: Where generated Product Requirements Prompts are stored

#### **⚙️ Project Configuration**
- **`package.json`**: Project metadata, useful for publishing and dependencies
- **`.github/`**: GitHub templates for community contributions
- **`LICENSE`**: MIT License with proper attribution

### 🎯 How It All Works Together:

1. **Setup**: Configure `GLOBAL_RULES.md` and review patterns in `.cursor/rules/pattern-examples/`
2. **Create PRD**: Choose appropriate template from `PDD/PRDs/templates/` and fill it out
3. **Generate PRP**: Use `PDD/PRPs/commands/generate-prp.md` to create implementation plan
4. **Execute**: Use `PDD/PRPs/commands/execute-prp.md` to implement following all rules and validations
5. **Validate**: AI automatically runs tests and fixes issues based on rules

---

## ⚙️ Initial Setup

### Step 1: Clone and Configure

```bash
# 1. Clone the template
git clone https://github.com/Flowtask-ai/pdd-cursor-template.git
cd pdd-cursor-template

# 2. Open in Cursor
cursor .
```

### Step 2: Customize Global Rules

Edit `GLOBAL_RULES.md` for your project:

```markdown
## 🧱 Code Structure

- **Language**: Python 3.11+
- **Framework**: FastAPI
- **Database**: PostgreSQL
- **Testing**: pytest
- **Formatting**: Black + isort
```

### Step 3: Add Examples

Create examples in `examples/` following this structure:

```
examples/
├── api/
│   └── fastapi_basic/
│       ├── main.py
│       └── models.py
├── database/
│   └── sqlalchemy_models/
│       └── user.py
└── testing/
    └── unit_tests/
        └── test_user.py
```

---

## 🔄 Basic Workflow

### Scenario: Create a User Management System

#### Step 1: Create PRD

Copy and edit `PDD/PRDs/templates/new-bc-XXX.md`:

```markdown
# New Bounded Context: User Management System

## 🎯 Project Overview
**BC Name**: User Management System
**Purpose**: Create a complete user management system with authentication, authorization, and user administration
**Scope**: Complete project with frontend and backend

## 🏗️ Architecture Requirements
**Frontend**: React 18 with TypeScript
**Backend**: FastAPI with Python 3.11+
**Database**: PostgreSQL 15 with SQLAlchemy 2.0
**Infrastructure**: Docker containers

## ✨ Core Features
1. **User Authentication**: Registration, login, password reset with JWT tokens
2. **User Management**: Complete CRUD operations for users
3. **Role Management**: Admin, user, guest roles with permissions
4. **Security**: JWT authentication, password hashing, rate limiting

## 📚 Examples to Follow
- `examples/api/fastapi_basic/` - Backend patterns
- `examples/auth/jwt_authentication/` - Authentication patterns
- `examples/database/sqlalchemy_models/` - Data modeling patterns
```

#### Step 2: Generate PRP

Use the command from `PDD/PRPs/commands/generate-prp.md`:

```
Generate a PRP following the project rules, taking as reference PDD/PRDs/new-bc-user-management.md and patterns in .cursor/rules/pattern-examples/. The PRP should include:

1. System architecture
2. File structure
3. Step-by-step implementation
4. Validation tests
5. Execution commands
```

#### Step 3: Execute Implementation

Use the command from `PDD/PRPs/commands/execute-prp.md`:

```
Execute the PRP in PDD/PRPs/user-management-system.md following all validations and project rules. Make sure all tests pass.
```

---

## 🎯 Specific Use Cases

### Case 1: New Bounded Context (Complete Project)

**Situation**: You want to create a completely new project with frontend and backend.

**Steps**:
1. **Configure rules**: Edit `GLOBAL_RULES.md` with your tech stack
2. **Add examples**: Create basic examples in `examples/`
3. **Create PRD**: Copy `PDD/PRDs/templates/new-bc-XXX.md` and fill it out
4. **Generate PRP**: Use `PDD/PRPs/commands/generate-prp.md` to create implementation plan
5. **Execute**: Use `PDD/PRPs/commands/execute-prp.md` to build the system

**Example prompt**:
```
Generate a PRP to create a complete task management application with FastAPI backend, React frontend, PostgreSQL database, and JWT authentication. Include user management, task CRUD, and real-time updates.
```

### Case 2: Improve Existing Bounded Context (Refactoring)

**Situation**: You have a project that needs improvements in quality, performance, or architecture.

**Steps**:
1. **Analyze code**: "Analyze existing code and generate a refactoring plan"
2. **Create PRD**: Use `PDD/PRDs/templates/improve-bc-XXX.md` to describe improvements
3. **Generate PRP**: "Generate a PRP to refactor following best practices"
4. **Execute incrementally**: "Execute the PRP step by step, validating each change"

**Example prompt**:
```
Analyze the current authentication system and generate a PRP to improve security, performance, and code quality following the project rules.
```

### Case 3: New Feature (Existing Bounded Context)

**Situation**: Well-structured project, add new feature to existing bounded context.

**Steps**:
1. **Define feature**: Use `PDD/PRDs/templates/new-feature-YYY-bc-XXX.md` for the new functionality
2. **Generate specific PRP**: "Generate a PRP for this specific feature"
3. **Execute with validation**: "Execute the PRP ensuring it doesn't break existing functionality"

**Example prompt**:
```
Generate a PRP to add a push notification system to the existing authentication bounded context, integrating with Firebase and maintaining the current architecture.
```

---

## 🛠️ Troubleshooting

### Problem: AI doesn't follow the rules

**Solution**:
1. Verify that `.cursor/rules/00-project-global.mdc` is well configured
2. Use more specific prompts: "Follow EXACTLY the rules in GLOBAL_RULES.md"
3. Reference specific examples: "Use the pattern from examples/api/fastapi_basic/"

### Problem: Tests fail after implementation

**Solution**:
1. Make sure the PRP includes validation commands
2. Use: "Execute the PRP and automatically fix any test errors"
3. Verify that examples in `examples/` are correct

### Problem: Code doesn't follow project style

**Solution**:
1. Add formatting rules in `GLOBAL_RULES.md`
2. Include style examples in `examples/`
3. Use: "Make sure to follow the code style defined in the rules"

### Problem: AI doesn't understand context

**Solution**:
1. Be more specific in `FEATURE_REQUEST.md`
2. Add more examples in `examples/`
3. Use more detailed prompts with specific context

---

## 💡 Pro Tips

### 1. Use Specific Roles

For complex tasks, specify the role:

```
Act as an architect and generate a PRP to design a microservices architecture.
```

```
Act as a developer and execute the PRP implementing the code step by step.
```

### 2. Validate Incrementally

Don't execute everything at once. Validate each step:

```
Execute only the first section of the PRP and validate it works before continuing.
```

### 3. Document Decisions

Add comments in the code explaining important decisions:

```python
# We use SQLAlchemy 2.0 for better async performance
# See: https://docs.sqlalchemy.org/en/20/changelog/migration_20.html
```

### 4. Keep Examples Updated

Update `examples/` with patterns that work well in your project.

---

## 🎯 Success Checklist

Before starting, verify:

- [ ] `GLOBAL_RULES.md` is customized for your project
- [ ] `examples/` has relevant patterns
- [ ] `.cursor/rules/` is correctly configured
- [ ] You understand the basic workflow
- [ ] You have a clear `FEATURE_REQUEST.md`

After each implementation, verify:

- [ ] All tests pass
- [ ] Code follows project rules
- [ ] Documentation is updated
- [ ] Examples reflect used patterns

---

## 🆘 Need Help?

1. **Review this guide** step by step
2. **Check examples** in `examples/`
3. **Consult rules** in `GLOBAL_RULES.md`
4. **Use specific prompts** like those in this guide

PDD will make you 10x more productive! 🚀 