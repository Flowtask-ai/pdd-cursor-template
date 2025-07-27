# PDD - Prompt Driven Design Template para Cursor

Una plantilla integral para **PDD (Prompt Driven Design)** adaptada específicamente para Cursor, proporcionando un framework completo para desarrollo asistido por IA.

> **PDD es 10x mejor que prompt engineering y 100x mejor que vibe coding.**

## 🚀 Inicio Rápido

> **📖 Para una guía completa paso a paso, consulta [GUIA_USO.md](GUIA_USO.md)**

```bash
# 1. Clona esta plantilla
git clone https://github.com/coleam00/Context-Engineering-Intro.git
cd Context-Engineering-Intro

# 2. Configura las reglas del proyecto
edit GLOBAL_RULES.md

# 3. Agrega ejemplos
# Coloca ejemplos de código en examples/

# 4. Crea tu solicitud de característica
edit FEATURE_REQUEST.md

# 5. Genera un PRP
"Genera un PRP siguiendo las reglas del proyecto"

# 6. Ejecuta el PRP
"Ejecuta el PRP en PRPs/tu-caracteristica.md"
```

## 📚 ¿Qué es PDD (Prompt Driven Design)?

### Prompt Engineering vs PDD

**Prompt Engineering:**
- Se enfoca en frases específicas
- Limitado a cómo formulas una tarea
- Como darle a alguien una nota adhesiva

**PDD (Prompt Driven Design):**
- Sistema completo para proporcionar contexto integral
- Incluye documentación, ejemplos, reglas y validación
- Como escribir un guión completo con todos los detalles

## 🏗️ Estructura de la Plantilla

```
pdd-cursor-template/
├── GLOBAL_RULES.md                    # Reglas globales del proyecto
├── FEATURE_REQUEST.md                 # Plantilla para solicitudes
├── FEATURE_REQUEST_EXAMPLE.md         # Ejemplo de solicitud
├── .cursor/
│   └── rules/
│       ├── 00-project-global.mdc      # Reglas globales (ejecutable)
│       ├── 01-feature-request.mdc     # Guía para solicitudes
│       ├── 02-prp-generator.mdc       # Generación de PRPs
│       ├── 03-prp-executor.mdc        # Ejecución de PRPs
│       ├── roles/
│       │   ├── 01-architect.mdc       # Rol de arquitecto
│       │   └── 02-developer.mdc       # Rol de desarrollador
│       └── templates/
│           └── prp-base.mdc           # Plantilla base para PRPs
├── prompts/
│   ├── generate-prp.md                # Prompt para generar PRPs
│   └── execute-prp.md                 # Prompt para ejecutar PRPs
├── examples/                          # Ejemplos de código
├── PRPs/                             # PRPs generados
└── README.md                         # Este archivo
```

## 🎯 Flujo de Trabajo

### 1. Configurar Reglas Globales
Edita `GLOBAL_RULES.md` para definir las reglas de tu proyecto.

### 2. Crear Solicitud de Característica
Usa `FEATURE_REQUEST.md` para describir lo que quieres construir:

```markdown
## 🎯 CARACTERÍSTICA
[Describe la característica específicamente]

## 📚 EJEMPLOS
[Referencia ejemplos en examples/]

## 📖 DOCUMENTACIÓN
[Incluye URLs de documentación]

## ⚠️ OTRAS CONSIDERACIONES
[Requisitos técnicos, seguridad, etc.]
```

### 3. Generar PRP
Usa el prompt:
```
"Genera un PRP siguiendo las reglas del proyecto, tomando como referencia FEATURE_REQUEST.md y los ejemplos en examples/"
```

### 4. Ejecutar Implementación
Usa el prompt:
```
"Ejecuta el PRP en PRPs/tu-caracteristica.md siguiendo todas las validaciones"
```

## 🎭 Sistema de Roles

### 🏗️ Arquitecto
- Diseña arquitecturas robustas
- Toma decisiones técnicas de alto nivel
- Crea documentación de arquitectura

### 💻 Desarrollador
- Implementa funcionalidades
- Escribe código limpio
- Crea tests unitarios

## 🔧 Mejores Prácticas

### 1. Sé Específico
- No asumas que la IA conoce tus preferencias
- Incluye requisitos específicos y restricciones
- Referencia ejemplos liberalmente

### 2. Proporciona Ejemplos
- Más ejemplos = mejores implementaciones
- Muestra qué hacer y qué no hacer
- Incluye patrones de manejo de errores

### 3. Usa Validaciones
- Los PRPs incluyen comandos de test que deben pasar
- La IA iterará hasta que todas las validaciones tengan éxito
- Esto asegura código funcional en el primer intento

### 4. Aprovecha la Documentación
- Incluye documentación oficial de APIs
- Agrega recursos relevantes
- Referencia secciones específicas

### 5. Personaliza Reglas
- Agrega tus convenciones
- Incluye reglas específicas del proyecto
- Define estándares de coding

## 📊 Beneficios

1. **Reduce Fallos de IA**: La mayoría de fallos no son del modelo, sino de contexto
2. **Asegura Consistencia**: La IA sigue patrones y convenciones del proyecto
3. **Permite Características Complejas**: Maneja implementaciones multi-paso
4. **Auto-corrección**: Bucles de validación permiten corrección automática

## 🚀 Casos de Uso

### Proyecto Nuevo
1. Configuración inicial
2. Definir característica inicial
3. Generar PRP completo
4. Ejecutar implementación

### Proyecto Existente
1. Análisis automático del código
2. Generar plan de refactorización
3. Ejecutar mejoras incrementales
4. Validación automática

### Extensión de Funcionalidad
1. Definir nueva característica
2. Generar PRP especializado
3. Implementación con validación automática

## 📚 Recursos

- [Documentación de Cursor](https://docs.cursor.com/)
- [PDD Best Practices](https://www.philschmid.de/context-engineering)
- [Cursor Rules Documentation](https://docs.cursor.com/context/rules)

## 🚀 Flowtask-ai

Este proyecto es parte de [Flowtask-ai](https://github.com/Flowtask-ai), una organización dedicada a crear herramientas y metodologías para mejorar la productividad del desarrollo con IA.

### 🌟 Características de Flowtask-ai

- **Metodologías probadas**: PDD y otras técnicas de desarrollo con IA
- **Templates optimizados**: Plantillas listas para usar
- **Comunidad activa**: Soporte y colaboración continua
- **Innovación constante**: Nuevas herramientas y mejoras

## 🤝 Contribuir

1. Fork el repositorio
2. Crea una rama para tu característica (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

### 📋 Guías de Contribución

- **Sigue PDD**: Usa esta misma metodología para contribuir
- **Documenta cambios**: Actualiza README.md y GUIA_USO.md
- **Mantén calidad**: Asegúrate de que los tests pasen
- **Sé específico**: Describe claramente tus cambios

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 📞 Contacto

- **GitHub**: [Flowtask-ai](https://github.com/Flowtask-ai)
- **Issues**: [Reportar problemas](https://github.com/Flowtask-ai/pdd-cursor-template/issues)
- **Discussions**: [Discusiones](https://github.com/Flowtask-ai/pdd-cursor-template/discussions)