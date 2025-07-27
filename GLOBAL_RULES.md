# Global Project Rules - PDD

Rules that govern development in this project using PDD (Prompt Driven Design). They are automatically applied through the Cursor Rules system.

## 🔄 Project Awareness

- **Read `README.md`** at the beginning of each conversation
- **Analyze existing patterns** before implementing
- **Maintain consistency** with project style

## 🧱 Code Structure

- **Maximum 500 lines per file** - refactor if necessary
- **Organize in modules** by feature or responsibility
- **Use relative imports** within packages
- **Use `python-dotenv`** for environment variables

### Architecture Patterns

**For AI agents:**
```
agents/
├── __init__.py
├── agent.py          # Main logic
├── tools.py          # Tools
├── prompts.py        # System prompts
└── models.py         # Data models
```

**For APIs:**
```
api/
├── __init__.py
├── routes/           # Endpoints
├── models/           # Models
├── services/         # Business logic
└── middleware/       # Middleware
```

## 🧪 Testing and Quality

- **Create unit tests** for each feature
- **Maintain coverage >90%**
- **Run automatic validations** after changes
- **Fix errors automatically** when possible

### Automatic Validations
```bash
# Syntax and style
ruff check --fix && mypy .

# Unit tests
pytest tests/ -v

# Coverage
pytest --cov=src --cov-report=html
```

## 📎 Style and Conventions

- **Python** as primary language
- **Follow PEP8** with type hints
- **Use `pydantic`** for validation
- **FastAPI** for APIs, **SQLAlchemy** for ORM

### Code Documentation
```python
def example_function(param1: str, param2: int) -> bool:
    """
    Brief summary.

    Args:
        param1 (str): Description.
        param2 (int): Description.

    Returns:
        bool: Description.
    """
```

## 🧠 AI Rules

- **Never assume missing context** - ask if you're not sure
- **Never hallucinate libraries** - only use verified packages
- **Confirm file paths** before referencing them
- **Don't delete existing code** without explicit instruction

## 🔧 Configuration

- **Use `.env`** for local variables
- **Never commit `.env`** with sensitive information
- **Keep `requirements.txt`** updated
- **Document required dependencies**

## 📚 Documentation

- **Update `README.md`** with new features
- **Keep docstrings** updated
- **Document patterns** in `examples/`
- **Use semantic versioning** for releases

## 🎯 PDD (Prompt Driven Design) Methodology

### Workflow
1. **Define feature** in `FEATURE_REQUEST.md`
2. **Generate PRP** using project rules
3. **Execute implementation** with validations
4. **Validate and iterate** until success

### Key Principles
- **Context over prompts**: Provide comprehensive context
- **Examples over explanations**: Show, don't just tell
- **Validation over assumptions**: Test everything
- **Iteration over perfection**: Improve continuously

### Success Metrics
- **All tests pass** automatically
- **Code follows patterns** from examples
- **Documentation is updated** and accurate
- **No regressions** in existing functionality 