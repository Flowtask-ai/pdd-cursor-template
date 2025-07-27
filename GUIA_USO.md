# 🚀 Guía Práctica: Cómo Usar PDD

Una guía paso a paso para usar esta plantilla y aplicar el método de PDD (Prompt Driven Design) en tus proyectos.

## 📋 Tabla de Contenidos

1. [Configuración Inicial](#configuración-inicial)
2. [Flujo de Trabajo Básico](#flujo-de-trabajo-básico)
3. [Casos de Uso Específicos](#casos-de-uso-específicos)
4. [Troubleshooting](#troubleshooting)

---

## ⚙️ Configuración Inicial

### Paso 1: Clonar y Configurar

```bash
# 1. Clona la plantilla
git clone https://github.com/coleam00/Context-Engineering-Intro.git
cd Context-Engineering-Intro

# 2. Abre en Cursor
cursor .
```

### Paso 2: Personalizar Reglas Globales

Edita `GLOBAL_RULES.md` para tu proyecto:

```markdown
## 🧱 Estructura de Código

- **Lenguaje**: Python 3.11+
- **Framework**: FastAPI
- **Base de datos**: PostgreSQL
- **Testing**: pytest
- **Formato**: Black + isort
```

### Paso 3: Agregar Ejemplos

Crea ejemplos en `examples/` siguiendo esta estructura:

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

## 🔄 Flujo de Trabajo Básico

### Escenario: Crear un Sistema de Usuarios

#### Paso 1: Crear Solicitud de Característica

Edita `FEATURE_REQUEST.md`:

```markdown
## 🎯 CARACTERÍSTICA

Crear un sistema de gestión de usuarios con autenticación JWT, roles de usuario, y API REST completa.

### Funcionalidades específicas:
- Registro de usuarios con validación de email
- Login con JWT tokens
- Roles: admin, user, guest
- CRUD completo de usuarios
- Middleware de autenticación
- Tests unitarios y de integración

## 📚 EJEMPLOS

- `examples/api/fastapi_basic/` - Estructura básica de FastAPI
- `examples/database/sqlalchemy_models/` - Patrones de modelos
- `examples/testing/unit_tests/` - Patrones de testing

## 📖 DOCUMENTACIÓN

- FastAPI: https://fastapi.tiangolo.com/
- SQLAlchemy: https://docs.sqlalchemy.org/
- JWT: https://pyjwt.readthedocs.io/
```

#### Paso 2: Generar PRP

En Cursor, usa este prompt:

```
Genera un PRP siguiendo las reglas del proyecto, tomando como referencia FEATURE_REQUEST.md y los ejemplos en examples/. El PRP debe incluir:

1. Arquitectura del sistema
2. Estructura de archivos
3. Implementación paso a paso
4. Tests de validación
5. Comandos de ejecución
```

#### Paso 3: Ejecutar Implementación

Una vez generado el PRP en `PRPs/sistema-usuarios.md`, usa:

```
Ejecuta el PRP en PRPs/sistema-usuarios.md siguiendo todas las validaciones y reglas del proyecto. Asegúrate de que todos los tests pasen.
```

---

## 🎯 Casos de Uso Específicos

### Caso 1: Proyecto Nuevo desde Cero

**Situación**: Quieres crear un nuevo proyecto de cero.

**Pasos**:
1. **Configurar reglas**: Edita `GLOBAL_RULES.md` con tu stack tecnológico
2. **Agregar ejemplos**: Crea ejemplos básicos en `examples/`
3. **Definir MVP**: Usa `FEATURE_REQUEST.md` para describir la primera característica
4. **Generar PRP**: "Genera un PRP para el MVP siguiendo las reglas"
5. **Ejecutar**: "Ejecuta el PRP completo"

**Ejemplo de prompt**:
```
Genera un PRP para crear un MVP de una aplicación de tareas con FastAPI, PostgreSQL y React. Incluye autenticación básica y CRUD de tareas.
```

### Caso 2: Refactorizar Proyecto Existente

**Situación**: Tienes un proyecto que necesita mejoras.

**Pasos**:
1. **Analizar código**: "Analiza el código existente y genera un plan de refactorización"
2. **Crear solicitud**: Usa `FEATURE_REQUEST.md` para describir las mejoras
3. **Generar PRP**: "Genera un PRP para refactorizar siguiendo las mejores prácticas"
4. **Ejecutar incrementalmente**: "Ejecuta el PRP paso a paso, validando cada cambio"

**Ejemplo de prompt**:
```
Analiza el código actual y genera un PRP para refactorizar la arquitectura, agregar tests, y mejorar la documentación siguiendo las reglas del proyecto.
```

### Caso 3: Agregar Nueva Funcionalidad

**Situación**: Proyecto bien estructurado, agregar nueva característica.

**Pasos**:
1. **Definir característica**: Usa `FEATURE_REQUEST.md` para la nueva funcionalidad
2. **Generar PRP específico**: "Genera un PRP para esta característica específica"
3. **Ejecutar con validación**: "Ejecuta el PRP asegurando que no rompa funcionalidad existente"

**Ejemplo de prompt**:
```
Genera un PRP para agregar un sistema de notificaciones push al proyecto existente, integrando con Firebase y manteniendo la arquitectura actual.
```

---

## 🛠️ Troubleshooting

### Problema: La IA no sigue las reglas

**Solución**:
1. Verifica que `.cursor/rules/00-project-global.mdc` esté bien configurado
2. Usa prompts más específicos: "Sigue EXACTAMENTE las reglas en GLOBAL_RULES.md"
3. Referencia ejemplos específicos: "Usa el patrón de examples/api/fastapi_basic/"

### Problema: Tests fallan después de implementación

**Solución**:
1. Asegúrate de que el PRP incluya comandos de validación
2. Usa: "Ejecuta el PRP y corrige cualquier error de test automáticamente"
3. Verifica que los ejemplos en `examples/` sean correctos

### Problema: Código no sigue el estilo del proyecto

**Solución**:
1. Agrega reglas de formato en `GLOBAL_RULES.md`
2. Incluye ejemplos de estilo en `examples/`
3. Usa: "Asegúrate de seguir el estilo de código definido en las reglas"

### Problema: La IA no entiende el contexto

**Solución**:
1. Sé más específico en `FEATURE_REQUEST.md`
2. Agrega más ejemplos en `examples/`
3. Usa prompts más detallados con contexto específico

---

## 💡 Tips Pro

### 1. Usa Roles Específicos

Para tareas complejas, especifica el rol:

```
Actúa como arquitecto y genera un PRP para diseñar la arquitectura de microservicios.
```

```
Actúa como desarrollador y ejecuta el PRP implementando el código paso a paso.
```

### 2. Valida Incrementalmente

No ejecutes todo de una vez. Valida cada paso:

```
Ejecuta solo la primera sección del PRP y valida que funcione antes de continuar.
```

### 3. Documenta Decisiones

Agrega comentarios en el código explicando decisiones importantes:

```python
# Usamos SQLAlchemy 2.0 para mejor performance con async
# Ver: https://docs.sqlalchemy.org/en/20/changelog/migration_20.html
```

### 4. Mantén Ejemplos Actualizados

Actualiza `examples/` con patrones que funcionen bien en tu proyecto.

---

## 🎯 Checklist de Éxito

Antes de empezar, verifica:

- [ ] `GLOBAL_RULES.md` está personalizado para tu proyecto
- [ ] `examples/` tiene patrones relevantes
- [ ] `.cursor/rules/` está configurado correctamente
- [ ] Entiendes el flujo de trabajo básico
- [ ] Tienes un `FEATURE_REQUEST.md` claro

Después de cada implementación, verifica:

- [ ] Todos los tests pasan
- [ ] El código sigue las reglas del proyecto
- [ ] La documentación está actualizada
- [ ] Los ejemplos reflejan los patrones usados

---

## 🆘 ¿Necesitas Ayuda?

1. **Revisa esta guía** paso a paso
2. **Verifica los ejemplos** en `examples/`
3. **Consulta las reglas** en `GLOBAL_RULES.md`
4. **Usa prompts específicos** como los de esta guía

¡PDD te hará 10x más productivo! 🚀 