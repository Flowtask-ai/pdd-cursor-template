# Prompt to Generate PRP

## 🎯 Instructions

Act as an expert in PDD (Prompt Driven Design). Generate a complete PRP (Product Requirements Prompt) following these instructions:

## 📋 Process

### 1. Analysis
- **Read completely** `FEATURE_REQUEST.md`
- **Identify all technical and functional requirements**
- **Analyze referenced examples**
- **Review provided documentation**

### 2. Research
- **Search for similar patterns** in existing code
- **Consult official documentation** of libraries
- **Identify best practices** and known gotchas

### 3. Creation
- **Use the template** in `.cursor/rules/templates/prp-base.mdc`
- **Include complete context** and documentation
- **Define detailed implementation steps**
- **Specify executable validations**

## 📝 Required Structure

1. **Purpose and Context**
   - Clear description of objective
   - Project context and architecture

2. **Technical Requirements**
   - Detailed specifications
   - Dependencies and libraries

3. **Architecture and Design**
   - Proposed file structure
   - Design patterns to follow

4. **Implementation Plan**
   - Detailed and sequential steps
   - Validations at each step

5. **Testing and Validation**
   - Testing strategy
   - Acceptance criteria

6. **Success Criteria**
   - Specific metrics
   - Required functionality

## 🔍 Validations

### Automatic
```bash
# Syntax and style
ruff check --fix && mypy .

# Unit tests
pytest tests/ -v

# Coverage
pytest --cov=src --cov-report=html
```

### Manual
- [ ] Functionality meets requirements
- [ ] Code follows project patterns
- [ ] Documentation updated

## 📊 Quality

### Checklist
- [ ] **Complete context**: All necessary information
- [ ] **Clear steps**: Step-by-step implementation
- [ ] **Executable validations**: Commands that can be executed
- [ ] **Correct references**: Existing files and patterns
- [ ] **Measurable criteria**: Success clearly defined

### Scoring
**Evaluate the PRP on a scale of 1-10** based on:
- Context completeness (1-3 points)
- Implementation clarity (1-3 points)
- Validation quality (1-2 points)
- References and documentation (1-2 points)

## 📤 Output

### File to Create
Save the PRP in `PRPs/[feature-name].md`

### Content
- **Complete PRP** following the template
- **Confidence score** (1-10)
- **Score justification** 