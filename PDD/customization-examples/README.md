# 🎯 Customization Examples

This directory contains ready-to-use adaptations of the PDD template for different tech stacks.

## 📁 Available Examples

### 🟢 Node.js + Express + React
**Directory**: `nodejs-express-react/`
- **Backend**: Node.js with Express.js
- **Frontend**: React with TypeScript
- **Database**: MongoDB with Mongoose
- **Testing**: Jest + Supertest + Playwright

### 🔵 Java + Spring Boot + Vue.js
**Directory**: `java-spring-vue/`
- **Backend**: Java with Spring Boot
- **Frontend**: Vue.js with TypeScript
- **Database**: PostgreSQL with JPA/Hibernate
- **Testing**: JUnit 5 + Mockito + Playwright

### 🟣 .NET + ASP.NET Core + Angular
**Directory**: `dotnet-aspnet-angular/`
- **Backend**: C# with ASP.NET Core
- **Frontend**: Angular with TypeScript
- **Database**: SQL Server with Entity Framework
- **Testing**: xUnit + Moq + Playwright

## 🚀 How to Use

1. **Choose your stack** from the examples above
2. **Copy the files** from the corresponding directory
3. **Replace** the default `.cursor/rules/core-rules/` and `.cursor/rules/code-examples/`
4. **Update** any project-specific configurations
5. **Test** the customization with a sample PRD

## 📝 Adding New Examples

To contribute a new customization example:

1. **Create a new directory** with your stack name
2. **Include** adapted core-rules and code-examples
3. **Add** a README.md explaining your stack
4. **Test** that the examples work correctly
5. **Submit** a pull request

## 🎯 Example Structure

```
customization-examples/
├── your-stack-name/
│   ├── README.md              # Stack description and setup
│   ├── core-rules/            # Adapted core rules
│   │   ├── 00-global-rules.mdc
│   │   ├── 01-domain-architecture.mdc
│   │   ├── 02-backend-development.mdc
│   │   ├── 03-frontend-development.mdc
│   │   ├── 04-testing-strategy.mdc
│   │   ├── 05-quality-assurance.mdc
│   │   └── 06-ci-cd-pipeline.mdc
│   └── code-examples/         # Adapted code examples
│       ├── 01-domain.mdc
│       ├── 02-backend.mdc
│       ├── 03-frontend.mdc
│       ├── 04-testing.mdc
│       ├── 05-quality.mdc
│       └── 06-ci-cd.mdc
```

## 🔧 Customization Tips

- **Keep it real**: Use actual patterns from production projects
- **Be specific**: Include framework-specific conventions
- **Document well**: Explain why certain patterns are chosen
- **Test thoroughly**: Ensure examples work correctly
- **Stay updated**: Keep examples current with framework versions

---

**Need help?** Check the main [HOW_TO_CUSTOMIZE.md](../HOW_TO_CUSTOMIZE.md) guide for detailed instructions. 