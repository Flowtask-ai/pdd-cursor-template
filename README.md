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

### Prompt Engineering vs PDD

**Prompt Engineering:**
- Focuses on specific phrases
- Limited to how you formulate a task
- Like giving someone a sticky note

**PDD (Prompt Driven Design):**
- Complete system for providing comprehensive context
- Includes documentation, examples, rules, and validation
- Like writing a complete script with all details

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

### 🏗️ Architect
- Designs robust architectures
- Makes high-level technical decisions
- Creates architecture documentation

### 💻 Developer
- Implements features
- Writes clean code
- Creates unit tests

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

## 📞 Contact

- **GitHub**: [Flowtask-ai](https://github.com/Flowtask-ai)
- **Issues**: [Report issues](https://github.com/Flowtask-ai/pdd-cursor-template/issues)
- **Discussions**: [Discussions](https://github.com/Flowtask-ai/pdd-cursor-template/discussions)