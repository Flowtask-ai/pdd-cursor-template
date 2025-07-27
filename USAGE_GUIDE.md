# 🚀 Practical Guide: How to Use PDD

A step-by-step guide to use this template and apply the PDD (Prompt Driven Design) methodology in your projects.

## 📋 Table of Contents

1. [Initial Setup](#initial-setup)
2. [Basic Workflow](#basic-workflow)
3. [Specific Use Cases](#specific-use-cases)
4. [Troubleshooting](#troubleshooting)

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

#### Step 1: Create Feature Request

Edit `FEATURE_REQUEST.md`:

```markdown
## 🎯 FEATURE

Create a user management system with JWT authentication, user roles, and complete REST API.

### Specific functionalities:
- User registration with email validation
- Login with JWT tokens
- Roles: admin, user, guest
- Complete CRUD for users
- Authentication middleware
- Unit and integration tests

## 📚 EXAMPLES

- `examples/api/fastapi_basic/` - Basic FastAPI structure
- `examples/database/sqlalchemy_models/` - Model patterns
- `examples/testing/unit_tests/` - Testing patterns

## 📖 DOCUMENTATION

- FastAPI: https://fastapi.tiangolo.com/
- SQLAlchemy: https://docs.sqlalchemy.org/
- JWT: https://pyjwt.readthedocs.io/
```

#### Step 2: Generate PRP

In Cursor, use this prompt:

```
Generate a PRP following the project rules, taking as reference FEATURE_REQUEST.md and examples in examples/. The PRP should include:

1. System architecture
2. File structure
3. Step-by-step implementation
4. Validation tests
5. Execution commands
```

#### Step 3: Execute Implementation

Once the PRP is generated in `PRPs/user-system.md`, use:

```
Execute the PRP in PRPs/user-system.md following all validations and project rules. Make sure all tests pass.
```

---

## 🎯 Specific Use Cases

### Case 1: New Project from Scratch

**Situation**: You want to create a new project from scratch.

**Steps**:
1. **Configure rules**: Edit `GLOBAL_RULES.md` with your tech stack
2. **Add examples**: Create basic examples in `examples/`
3. **Define MVP**: Use `FEATURE_REQUEST.md` to describe the first feature
4. **Generate PRP**: "Generate a PRP for the MVP following the rules"
5. **Execute**: "Execute the complete PRP"

**Example prompt**:
```
Generate a PRP to create an MVP of a task application with FastAPI, PostgreSQL and React. Include basic authentication and task CRUD.
```

### Case 2: Refactor Existing Project

**Situation**: You have a project that needs improvements.

**Steps**:
1. **Analyze code**: "Analyze existing code and generate a refactoring plan"
2. **Create request**: Use `FEATURE_REQUEST.md` to describe improvements
3. **Generate PRP**: "Generate a PRP to refactor following best practices"
4. **Execute incrementally**: "Execute the PRP step by step, validating each change"

**Example prompt**:
```
Analyze the current code and generate a PRP to refactor the architecture, add tests, and improve documentation following the project rules.
```

### Case 3: Add New Functionality

**Situation**: Well-structured project, add new feature.

**Steps**:
1. **Define feature**: Use `FEATURE_REQUEST.md` for the new functionality
2. **Generate specific PRP**: "Generate a PRP for this specific feature"
3. **Execute with validation**: "Execute the PRP ensuring it doesn't break existing functionality"

**Example prompt**:
```
Generate a PRP to add a push notification system to the existing project, integrating with Firebase and maintaining the current architecture.
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