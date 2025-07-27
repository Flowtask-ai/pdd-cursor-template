# PDD - Prompt Driven Design Template for Cursor

A comprehensive template for **PDD (Prompt Driven Design)** specifically adapted for Cursor, providing a complete framework for AI-assisted development.

> **PDD is 10x better than prompt engineering and 100x better than vibe coding.**

## 🚀 Quick Start

> **📖 For a complete step-by-step guide, see [USAGE_GUIDE.md](USAGE_GUIDE.md)**

```bash
# 1. Clone this template
git clone https://github.com/Flowtask-ai/pdd-cursor-template.git
cd pdd-cursor-template

# 2. Configure project rules
edit GLOBAL_RULES.md

# 3. Add examples
# Place code examples in examples/

# 4. Create your feature request
edit FEATURE_REQUEST.md

# 5. Generate a PRP
"Generate a PRP following the project rules"

# 6. Execute the PRP
"Execute the PRP in PRPs/your-feature.md"
```

## 📚 What is PDD (Prompt Driven Design)?

### The Foundation: Context Engineering

**Context Engineering** is the foundational methodology that PDD builds upon. It's a comprehensive approach to providing AI assistants with complete context through:

- **Structured Documentation**: Complete project context and requirements
- **Code Examples**: Working patterns and implementations
- **Validation Systems**: Automated tests and quality checks
- **Rule-Based Guidance**: Clear conventions and standards

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
├── GLOBAL_RULES.md                    # Global project rules
├── FEATURE_REQUEST.md                 # Feature request template
├── FEATURE_REQUEST_EXAMPLE.md         # Feature request example
├── .cursor/
│   └── rules/
│       ├── 00-project-global.mdc      # Global rules (executable)
│       ├── 01-feature-request.mdc     # Feature request guide
│       ├── 02-prp-generator.mdc       # PRP generation
│       ├── 03-prp-executor.mdc        # PRP execution
│       ├── roles/
│       │   ├── 01-architect.mdc       # Architect role
│       │   └── 02-developer.mdc       # Developer role
│       └── templates/
│           └── prp-base.mdc           # Base PRP template
├── prompts/
│   ├── generate-prp.md                # Prompt to generate PRPs
│   └── execute-prp.md                 # Prompt to execute PRPs
├── examples/                          # Code examples
├── PRPs/                             # Generated PRPs
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

### 4. Execute Implementation
Use the prompt:
```
"Execute the PRP in PRPs/your-feature.md following all validations"
```

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

### New Project
1. Initial setup
2. Define initial feature
3. Generate complete PRP
4. Execute implementation

### Existing Project
1. Automatic code analysis
2. Generate refactoring plan
3. Execute incremental improvements
4. Automatic validation

### Feature Extension
1. Define new feature
2. Generate specialized PRP
3. Implementation with automatic validation

## 📚 Resources

- [Cursor Documentation](https://docs.cursor.com/)
- [PDD Best Practices](https://www.philschmid.de/context-engineering)
- [Cursor Rules Documentation](https://docs.cursor.com/context/rules)

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