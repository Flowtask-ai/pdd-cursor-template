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
├── 📄 LICENSE                     # MIT License (Flowtask-ai + Cole Medin attribution)
├── 📄 package.json                # Project metadata and dependencies
│
├── 📁 .cursor/
│   └── 📁 rules/                  # Cursor Rules (automatic AI context)
│       ├── 📁 core-rules/               # Core project rules
│       │   ├── 📄 00-global-rules.mdc   # Global project rules
│       │   ├── 📄 01-domain-architecture.mdc
│       │   ├── 📄 02-backend-development.mdc
│       │   ├── 📄 03-frontend-development.mdc
│       │   ├── 📄 04-testing-strategy.mdc
│       │   ├── 📄 05-quality-assurance.mdc
│       │   └── 📄 06-ci-cd-pipeline.mdc
│       ├── 📁 commands/                 # Commands for PDD workflow
│       │   ├── 📄 01-generate-prp.mdc   # Command to generate PRPs
│       │   └── 📄 02-execute-prp.mdc    # Command to execute PRPs
│       ├── 📁 roles/                    # Specialized AI roles
│       │   ├── 📄 01-architect.mdc      # Architecture-focused AI behavior
│       │   └── 📄 02-developer.mdc      # Development-focused AI behavior
│       └── 📁 code-examples/            # Code patterns and examples
│           ├── 📄 01-domain.mdc
│           ├── 📄 02-backend.mdc
│           ├── 📄 03-frontend.mdc
│           ├── 📄 04-testing.mdc
│           ├── 📄 05-quality.mdc
│           └── 📄 06-ci-cd.mdc
│
├── 📁 PDD/                        # Prompt Driven Design
│   ├── 📄 USAGE_GUIDE.md          # This guide - step-by-step instructions
│   ├── 📄 HOW_TO_CUSTOMIZE.md     # Guide for adapting to other tech stacks
│   ├── 📁 PRDs/                   # Product Requirements Documents
│   │   ├── 📁 templates/          # Templates for each use case
│   │   │   ├── 📄 new-bc-XXX.md   # Template for new bounded contexts
│   │   │   ├── 📄 new-feature-YYY-bc-XXX.md  # Template for new features
│   │   │   └── 📄 improve-bc-XXX.md  # Template for BC improvements
│   │   ├── 📁 examples/           # Filled examples for inspiration
│   │   │   ├── 📄 new-bc-ecommerce.md # Example: Complete e-commerce project
│   │   │   ├── 📄 new-feature-notifications-bc-auth.md  # Example: Notifications feature
│   │   │   └── 📄 improve-bc-auth.md  # Example: Auth system improvements
│   │   └── 📁 requests/           # Your PRDs go here
│   │       └── 📄 README.md       # Instructions for creating PRDs
│   ├── 📁 PRPs/                   # Product Requirements Prompts (generated)
│   │   ├── 📁 templates/          # Templates for PRPs
│   │   │   └── 📄 prp-base.md    # Base template for generating PRPs
│   │   └── 📁 generated/          # Generated PRPs go here
│   │       └── 📄 README.md       # Instructions for generated PRPs
│   └── 📁 customization-examples/ # Ready-to-use adaptations for other stacks
│       ├── 📄 README.md           # Overview of available examples
│       ├── 📁 nodejs-express-react/
│       ├── 📁 java-spring-vue/
│       └── 📁 dotnet-aspnet-angular/
│
└── 📁 .github/                    # GitHub configuration
    └── 📁 ISSUE_TEMPLATE/         # Issue templates for contributions
        ├── 📄 bug_report.md       # Template for bug reports
        └── 📄 feature_request.md  # Template for feature requests
```

### 🔑 Key Files Explained:

#### **📄 Core Documentation**
- **`README.md`**: Main project overview, methodology explanation, and quick start
- **`PDD/USAGE_GUIDE.md`**: Detailed step-by-step instructions (this file)
- **`PDD/HOW_TO_CUSTOMIZE.md`**: Guide for adapting to other tech stacks
- **`.cursor/rules/core-rules/`**: AI rules that are automatically applied by Cursor

#### **📄 Templates & Examples**
- **`PDD/PRDs/templates/`**: Templates for each use case (new BC, new feature, improve BC)
- **`PDD/PRDs/examples/`**: Filled examples for inspiration and reference
- **`.cursor/rules/code-examples/`**: Code patterns and reference implementations

#### **🤖 AI Configuration**
- **`.cursor/rules/`**: Automatic context for Cursor's AI (always active)
- **`.cursor/rules/commands/`**: Commands that guide AI behavior for specific tasks
- **`PDD/PRPs/generated/`**: Where generated Product Requirements Prompts are stored

#### **⚙️ Project Configuration**
- **`package.json`**: Project metadata, useful for publishing and dependencies
- **`.github/`**: GitHub templates for community contributions
- **`LICENSE`**: MIT License with proper attribution

### 🎯 How It All Works Together:

1. **Setup**: Review patterns in `.cursor/rules/code-examples/` and project structure
2. **Create PRD**: Copy appropriate template from `PDD/PRDs/templates/` to `PDD/PRDs/requests/` and fill it out
3. **Generate PRP**: Use "Generate a PRP from PDD/PRDs/requests/your-file.md" to create implementation plan
4. **Execute**: Use "Execute the PRP in PDD/PRPs/generated/your-file.md" to implement following all rules and validations
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

### Step 2: Review Project Structure

Familiarize yourself with the template structure:

```bash
# Review available templates
ls PDD/PRDs/templates/

# Review examples for inspiration
ls PDD/PRDs/examples/

# Review code patterns
ls .cursor/rules/code-examples/
```

### Step 3: Create Your First PRD

Copy a template to get started:

```bash
# For a new project
cp PDD/PRDs/templates/new-bc-XXX.md PDD/PRDs/requests/new-bc-myproject.md

# For a new feature
cp PDD/PRDs/templates/new-feature-YYY-bc-XXX.md PDD/PRDs/requests/new-feature-auth-bc-user.md

# For improvements
cp PDD/PRDs/templates/improve-bc-XXX.md PDD/PRDs/requests/improve-bc-auth.md
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
- `.cursor/rules/code-examples/01-backend.mdc` - Backend patterns
- `.cursor/rules/code-examples/04-testing.mdc` - Testing patterns
- `.cursor/rules/code-examples/02-backend.mdc` - Data modeling patterns
```

#### Step 2: Generate PRP

Use the command to generate a PRP:

```
Generate a PRP from PDD/PRDs/requests/new-bc-user-management.md
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
1. **Review rules**: Check `.cursor/rules/core-rules/` for your tech stack
2. **Add examples**: Add PRD examples in `PDD/PRDs/examples/` and code patterns in `.cursor/rules/code-examples/`
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
2. Use more specific prompts: "Follow EXACTLY the rules in .cursor/rules/core-rules/"
3. Reference specific examples: "Use the pattern from .cursor/rules/code-examples/01-backend.mdc"

### Problem: Tests fail after implementation

**Solution**:
1. Make sure the PRP includes validation commands
2. Use: "Execute the PRP and automatically fix any test errors"
3. Verify that code patterns in `.cursor/rules/code-examples/` are correct

### Problem: Code doesn't follow project style

**Solution**:
1. Add formatting rules in `.cursor/rules/core-rules/`
2. Include style examples in `.cursor/rules/code-examples/`
3. Use: "Make sure to follow the code style defined in the rules"

### Problem: AI doesn't understand context

**Solution**:
1. Be more specific in your PRD file
2. Add more PRD examples in `PDD/PRDs/examples/`
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

Update `.cursor/rules/code-examples/` with patterns that work well in your project.

---

## 🎯 Success Checklist

Before starting, verify:

- [ ] `.cursor/rules/core-rules/` is configured for your project
- [ ] `.cursor/rules/code-examples/` has relevant patterns
- [ ] `.cursor/rules/` is correctly configured
- [ ] You understand the basic workflow
- [ ] You have a clear PRD file in `PDD/PRDs/requests/`

After each implementation, verify:

- [ ] All tests pass
- [ ] Code follows project rules
- [ ] Documentation is updated
- [ ] Examples reflect used patterns

---

## 🆘 Need Help?

1. **Review this guide** step by step
2. **Check PRD examples** in `PDD/PRDs/examples/`
3. **Consult rules** in `.cursor/rules/core-rules/`
4. **Use specific prompts** like those in this guide

PDD will make you 10x more productive! 🚀 