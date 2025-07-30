# PDD - Prompt Driven Design Template for Cursor

A comprehensive template for **PDD (Prompt Driven Design)** specifically adapted for Cursor, providing a complete framework for AI-assisted development.

> **PDD is much better than prompt engineering and vibe coding.**

## 🚀 Quick Start

> **📖 For a complete step-by-step guide, see [PDD/USAGE_GUIDE.md](PDD/USAGE_GUIDE.md)**

```bash
# 1. Clone this template
git clone https://github.com/Flowtask-ai/pdd-cursor-template.git
cd pdd-cursor-template

# 2. Review project structure
# Check PDD/PRDs/templates/ for available templates
# Check PDD/PRDs/examples/ for inspiration

# 3. Create your PRD
# Copy a template from PDD/PRDs/templates/ to PDD/PRDs/requests/
# Fill it with your specific requirements

# 4. Generate a PRP
"Generate a PRP from PDD/PRDs/requests/your-file.md"

# 5. Execute the PRP
"Execute the PRP in PDD/PRPs/generated/your-file.md"
```

## 📚 What is PDD (Prompt Driven Design)?

### The Foundation: Context Engineering

**Context Engineering** is the foundational methodology that PDD builds upon. It's a comprehensive approach to providing AI assistants with complete context through:

- **Structured Documentation**: Complete project context and requirements
- **Code Examples**: Working patterns and implementations
- **Validation Systems**: Automated tests and quality checks
- **Rule-Based Guidance**: Clear conventions and standards

### 🎯 Specialized for Your Stack

This template comes with **Python/FastAPI/React** specialization out of the box. If you use a different tech stack, check [PDD/HOW_TO_CUSTOMIZE.md](PDD/HOW_TO_CUSTOMIZE.md) for adaptation guides and examples.

### Prompt Engineering vs Context Engineering vs PDD

**Prompt Engineering:**
- Focuses on specific phrases
- Limited to how you formulate a task
- Like giving someone a sticky note

**Context Engineering:**
- Complete system for providing comprehensive context
- Includes documentation, examples, rules, and validation
- Like writing a complete script with all details
- **Original**: Developed for Claude Code

**PDD (Prompt Driven Design):**
- **Evolution** of Context Engineering specifically for Cursor
- **Enhanced** with role-based development and Cursor Rules
- **Optimized** for modern AI-assisted development workflows
- **International** and accessible to global developers
- Like having a complete development team with specialized roles

## 📋 What is a PRP (Product Requirements Prompt)?

A **PRP (Product Requirements Prompt)** is the core deliverable of the PDD methodology. Think of it as a comprehensive blueprint that an AI assistant can follow to implement a feature or system.

### PRP vs Traditional PRD

**Traditional PRD (Product Requirements Document):**
- Written for human developers
- High-level requirements and specifications
- Requires interpretation and implementation decisions
- Often needs clarification and back-and-forth

**PRP (Product Requirements Prompt):**
- Written specifically for AI assistants
- Includes complete implementation context
- Contains executable validation commands
- Provides step-by-step implementation guidance
- Self-contained and actionable

### What Makes a Good PRP?

A comprehensive PRP includes:

1. **Complete Context**
   - Project background and architecture
   - Existing code patterns and conventions
   - Technical constraints and requirements

2. **Detailed Specifications**
   - Exact functionality requirements
   - API specifications and data models
   - User interface requirements

3. **Implementation Plan**
   - Step-by-step development process
   - File structure and organization
   - Code patterns to follow

4. **Validation Commands**
   - Executable test commands
   - Quality checks and linting
   - Performance benchmarks

5. **Success Criteria**
   - Clear definition of "done"
   - Measurable outcomes
   - Acceptance criteria

### Example PRP Structure

```markdown
# PRP: User Authentication System

## Context
- Project: E-commerce platform
- Tech Stack: FastAPI, PostgreSQL, JWT
- Existing patterns: examples/auth/

## Requirements
- User registration with email validation
- JWT-based authentication
- Password reset functionality

## Implementation Steps
1. Create user model with SQLAlchemy
2. Implement registration endpoint
3. Add JWT token generation
4. Create authentication middleware

## Validation Commands
\`\`\`bash
pytest tests/test_auth.py -v
ruff check src/auth/
mypy src/auth/
\`\`\`

## Success Criteria
- [ ] Registration endpoint returns 201
- [ ] Login generates valid JWT
- [ ] All tests pass
- [ ] Code coverage >90%
```

## 🎯 Evolution and Inspiration

### Original Context Engineering
This template is inspired by the **Context Engineering** methodology originally developed for Claude Code. The original creators pioneered the concept of providing comprehensive context to AI assistants through structured documentation, examples, and validation systems.

**Context Engineering** is the foundation upon which PDD is built. It established the core principles of:
- Providing complete context to AI assistants
- Using structured documentation and examples
- Implementing validation systems
- Creating rule-based development workflows

**Original Repository**: [Context Engineering Intro](https://github.com/coleam00/Context-Engineering-Intro) by [@coleam00](https://github.com/coleam00)

### Adaptation for Cursor
We've adapted and evolved this methodology specifically for **Cursor**, leveraging its unique features:

- **Cursor Rules**: Automatic context provision through `.cursor/rules/` system
- **Hybrid Approach**: Combining automatic rules with manual prompts for maximum effectiveness
- **Enhanced Workflow**: Streamlined process optimized for Cursor's AI capabilities

### Innovation: Role-Based Development
Inspired by the **Subagents** concept from Claude Code, we've introduced a **role-based development system** that enables:

- **Specialized AI Roles**: Architect, Developer, Tester, Reviewer, Documenter
- **Parallel Conversations**: Work with multiple specialized AI agents simultaneously
- **Extended Context Windows**: Each role maintains focused context for better results
- **Collaborative Workflow**: Agents can pass information through standardized files

This approach not only provides specialization but also leverages Cursor's ability to work with multiple conversations, effectively expanding the context window and improving AI performance.

### Key Improvements Over Original Context Engineering
- **Cursor-Native**: Designed specifically for Cursor's ecosystem and Cursor Rules
- **Role System**: Multi-agent collaboration inspired by Subagents concept
- **Enhanced Automation**: Better integration with Cursor's AI capabilities
- **International**: Fully documented in English for global adoption
- **Simplified**: Streamlined for easier adoption and use
- **Evolution**: Builds upon Context Engineering's solid foundation

## 🏗️ Template Structure

```
pdd-cursor-template/
├── .cursor/
│   └── rules/
│       ├── core-rules/
│       │   ├── 00-project-global.mdc      # Global rules (executable)
│       │   ├── 01-feature-request.mdc     # Feature request guide
│       │   ├── 02-prp-generator.mdc       # PRP generation
│       │   ├── 03-prp-executor.mdc        # PRP execution
│       │   ├── roles/
│       │   │   ├── 01-architect.mdc       # Architect role
│       │   │   └── 02-developer.mdc       # Developer role
│       │   └── templates/
│       │       └── prp-base.md           # Base PRP template
│       ├── commands/
│       │   ├── 01-generate-prp.mdc       # Prompt to generate PRPs
│       │   └── 02-execute-prp.mdc         # Prompt to execute PRPs
│       └── code-examples/
│           ├── 01-auth.mdc                # Auth example
│           └── 02-user-management.mdc     # User management example
├── PRDs/
│   ├── templates/
│   └── requests/
├── PRPs/
└── README.md                         # This file
```

## 🎯 Workflow

### 1. Configure Global Rules
Edit `GLOBAL_RULES.md` to define your project rules.

### 2. Create Feature Request
Use `FEATURE_REQUEST.md` to describe what you want to build:

```markdown
## 🎯 FEATURE
[Describe the feature specifically]

## 📚 EXAMPLES
[Reference examples in examples/]

## 📖 DOCUMENTATION
[Include documentation URLs]

## ⚠️ OTHER CONSIDERATIONS
[Technical requirements, security, etc.]
```

### 3. Generate PRP
Use the prompt:
```
"Generate a PRP following the project rules, taking as reference FEATURE_REQUEST.md and examples in examples/"
```

The AI will create a comprehensive **Product Requirements Prompt** that includes:
- Complete implementation context
- Step-by-step development plan
- Validation commands
- Success criteria

### 4. Execute Implementation
Use the prompt:
```
"Execute the PRP in PRPs/your-feature.md following all validations"
```

The AI will follow the PRP blueprint to implement the feature, running validations at each step and ensuring all success criteria are met.

## 🎭 Role System

Our **role-based development system** is conceptually inspired by the Subagents approach from Claude Code, enabling specialized AI collaboration:

### 🏗️ Architect
- Designs robust architectures
- Makes high-level technical decisions
- Creates architecture documentation
- **Context**: Focuses on system design and technical strategy

### 💻 Developer
- Implements features
- Writes clean code
- Creates unit tests
- **Context**: Focuses on implementation and code quality

### 🔍 Tester
- Creates comprehensive test suites
- Validates functionality
- Ensures code quality
- **Context**: Focuses on testing and validation

### 📝 Reviewer
- Reviews code and architecture
- Suggests improvements
- Ensures best practices
- **Context**: Focuses on code review and optimization

### 📚 Documenter
- Creates and maintains documentation
- Writes user guides
- Updates technical specs
- **Context**: Focuses on documentation and knowledge sharing

### 🚀 Benefits of Role-Based Development
- **Specialized Expertise**: Each role has focused knowledge and context
- **Parallel Processing**: Work with multiple specialized agents simultaneously
- **Extended Context**: Each conversation maintains relevant context
- **Collaborative Workflow**: Agents share information through standardized files
- **Better Results**: Specialized focus leads to higher quality outputs

## 🔧 Best Practices

### 1. Be Specific
- Don't assume the AI knows your preferences
- Include specific requirements and constraints
- Reference examples liberally

### 2. Provide Examples
- More examples = better implementations
- Show what to do and what not to do
- Include error handling patterns

### 3. Use Validations
- PRPs include test commands that must pass
- AI will iterate until all validations succeed
- This ensures functional code on first attempt

### 4. Leverage Documentation
- Include official API documentation
- Add relevant resources
- Reference specific sections

### 5. Customize Rules
- Add your conventions
- Include project-specific rules
- Define coding standards

## 📊 Benefits

1. **Reduces AI Failures**: Most failures are not from the model, but from context
2. **Ensures Consistency**: AI follows project patterns and conventions
3. **Enables Complex Features**: Handles multi-step implementations
4. **Self-Correction**: Validation loops allow automatic correction

## 🚀 Use Cases

PDD adapts to different project scenarios and complexity levels. Choose the approach that matches your current situation:

> **💡 Tech Stack**: This template is specialized for Python/FastAPI/React. For other stacks, see [PDD/HOW_TO_CUSTOMIZE.md](PDD/HOW_TO_CUSTOMIZE.md).

### 🏗️ **New Bounded Context** (Complete Project)
**When**: Starting a completely new project with frontend and backend
**Complexity**: High - Full system architecture
**Scope**: Complete application with multiple features

**Workflow**:
1. **Create PRD**: Copy `PDD/PRDs/templates/new-bc-XXX.md` to `PDD/PRDs/requests/` and fill it
2. **Generate PRP**: Use "Generate a PRP from PDD/PRDs/requests/your-file.md"
3. **Execute Foundation**: Use "Execute the PRP in PDD/PRPs/generated/your-file.md"
4. **Iterate**: Add features incrementally using the same methodology

**Example**: *"Create a complete e-commerce platform with React frontend, FastAPI backend, PostgreSQL database, and payment integration"*

---

### ✨ **New Feature** (Existing Bounded Context)
**When**: Adding new functionality to an existing, well-structured project
**Complexity**: Medium - Feature-specific implementation
**Scope**: Single feature or module within existing architecture

**Workflow**:
1. **Create PRD**: Copy `PDD/PRDs/templates/new-feature-YYY-bc-XXX.md` to `PDD/PRDs/requests/` and fill it
2. **Generate Feature PRP**: Use "Generate a PRP from PDD/PRDs/requests/your-file.md"
3. **Execute with Validation**: Use "Execute the PRP in PDD/PRPs/generated/your-file.md"
4. **Integrate**: Connect with existing systems and validate

**Example**: *"Add push notifications to existing user management system"*

---

### 🔧 **Improve Existing Bounded Context** (Refactoring)
**When**: Enhancing quality, performance, or maintainability of existing project
**Complexity**: Variable - Based on improvement scope
**Scope**: Code quality, architecture improvements, technical debt

**Workflow**:
1. **Create PRD**: Copy `PDD/PRDs/templates/improve-bc-XXX.md` to `PDD/PRDs/requests/` and fill it
2. **Generate Improvement Plan**: Use "Generate a PRP from PDD/PRDs/requests/your-file.md"
3. **Execute Incrementally**: Use "Execute the PRP in PDD/PRPs/generated/your-file.md"
4. **Validate Continuously**: Ensure no regressions during improvements
5. **Document Changes**: Update documentation and examples

**Example**: *"Refactor authentication system to use modern JWT patterns and improve security"*

---

### 🎯 **Choose Your Path**

| Scenario | Template File | AI Approach | Expected Outcome |
|----------|---------------|-------------|------------------|
| **New BC** | `PDD/PRDs/templates/new-bc-XXX.md` | Architect + Developer roles | Complete project foundation |
| **New Feature** | `PDD/PRDs/templates/new-feature-YYY-bc-XXX.md` | Developer role | Integrated feature |
| **Improve BC** | `PDD/PRDs/templates/improve-bc-XXX.md` | Architect + Developer roles | Enhanced codebase |

### 💡 **Pro Tips for Each Use Case**

#### **For New Bounded Context**:
- Start with MVP features first
- Use `examples/` to establish patterns early
- Focus on architecture before implementation details

#### **For New Features**:
- Reference existing `examples/` for consistency
- Ensure integration with current patterns
- Validate against existing test suite

#### **For Improvements**:
- Document current state before changes
- Use incremental approach to avoid breaking changes
- Update `examples/` with new best practices

## 📚 Resources

- [Cursor Documentation](https://docs.cursor.com/)
- [PDD Best Practices](https://www.philschmid.de/context-engineering)
- [Cursor Rules Documentation](https://docs.cursor.com/context/rules)
- [PDD Usage Guide](PDD/USAGE_GUIDE.md)
- [Customization Guide](PDD/HOW_TO_CUSTOMIZE.md)

## 🚀 Flowtask-ai

This project is part of [Flowtask-ai](https://github.com/Flowtask-ai), an organization dedicated to creating tools and methodologies to improve AI-assisted development productivity.

### 🌟 Flowtask-ai Features

- **Proven Methodologies**: PDD and other AI development techniques
- **Optimized Templates**: Ready-to-use templates
- **Active Community**: Continuous support and collaboration
- **Constant Innovation**: New tools and improvements

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### 📋 Contribution Guidelines

- **Follow PDD**: Use this same methodology to contribute
- **Document Changes**: Update README.md and USAGE_GUIDE.md
- **Maintain Quality**: Ensure tests pass
- **Be Specific**: Clearly describe your changes

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

### Original Inspiration
This template builds upon the groundbreaking **Context Engineering** methodology. We extend our gratitude to the original creators who pioneered this approach for AI-assisted development. Their work on providing comprehensive context to AI assistants has fundamentally changed how we think about AI collaboration.

### Cursor Team
Special thanks to the **Cursor team** for creating such a powerful development environment. Their continuous innovation in AI-assisted development tools makes projects like this possible.

### Claude Code Team
We also acknowledge the **Claude Code team** for the **Subagents** concept that inspired our role-based development approach. While we use Cursor, the conceptual inspiration from their multi-agent collaboration features has been valuable.

### Community
To the open-source community and all contributors who believe in the power of AI-assisted development. Your feedback, contributions, and adoption help us improve and evolve this methodology.

## 📞 Contact

- **GitHub**: [Flowtask-ai](https://github.com/Flowtask-ai)
- **Issues**: [Report issues](https://github.com/Flowtask-ai/pdd-cursor-template/issues)
- **Discussions**: [Discussions](https://github.com/Flowtask-ai/pdd-cursor-template/discussions)