# Reglas Globales del Proyecto - PDD

Reglas que rigen el desarrollo en este proyecto usando PDD (Prompt Driven Design). Se aplican automáticamente a través del sistema de Cursor Rules.

## 🔄 Conciencia del Proyecto

- **Lee `README.md`** al inicio de cada conversación
- **Analiza patrones existentes** antes de implementar
- **Mantén consistencia** con el estilo del proyecto

## 🧱 Estructura de Código

- **Máximo 500 líneas por archivo** - refactoriza si es necesario
- **Organiza en módulos** por característica o responsabilidad
- **Usa imports relativos** dentro de paquetes
- **Usa `python-dotenv`** para variables de entorno

### Patrones de Arquitectura

**Para agentes de IA:**
```
agents/
├── __init__.py
├── agent.py          # Lógica principal
├── tools.py          # Herramientas
├── prompts.py        # Prompts del sistema
└── models.py         # Modelos de datos
```

**Para APIs:**
```
api/
├── __init__.py
├── routes/           # Endpoints
├── models/           # Modelos
├── services/         # Lógica de negocio
└── middleware/       # Middleware
```

## 🧪 Testing y Calidad

- **Crea tests unitarios** para cada característica
- **Mantén cobertura >90%**
- **Ejecuta validaciones automáticas** después de cambios
- **Corrige errores automáticamente** cuando sea posible

### Validaciones Automáticas
```bash
# Sintaxis y estilo
ruff check --fix && mypy .

# Tests unitarios
pytest tests/ -v

# Cobertura
pytest --cov=src --cov-report=html
```

## 📎 Estilo y Convenciones

- **Python** como lenguaje principal
- **Sigue PEP8** con type hints
- **Usa `pydantic`** para validación
- **FastAPI** para APIs, **SQLAlchemy** para ORM

### Documentación de Código
```python
def example_function(param1: str, param2: int) -> bool:
    """
    Breve resumen.

    Args:
        param1 (str): Descripción.
        param2 (int): Descripción.

    Returns:
        bool: Descripción.
    """
```

## 🧠 Reglas de IA

- **Nunca asumas contexto faltante** - pregunta si no estás seguro
- **Nunca alucines librerías** - solo usa paquetes verificados
- **Confirma rutas de archivos** antes de referenciarlos
- **No elimines código existente** sin instrucción explícita

## 🔧 Configuración

- **Usa `.env`** para variables locales
- **Nunca commits `.env`** con información sensible
- **Mantén `requirements.txt`** actualizado
- **Documenta dependencias** requeridas

## 📚 Documentación

- **Actualiza `README.md`** con nuevas características
- **Mantén docstrings** actualizados
- **Documenta patrones** en `examples/`
- **Usa versionado semántico** para releases

## 🎯 Metodología Context Engineering

### Flujo de Trabajo
1. **Definir Requisitos**: Usar `FEATURE_REQUEST.md`
2. **Generar PRP**: Crear Product Requirements Prompt
3. **Ejecutar**: Seguir PRP con validaciones
4. **Refinamiento**: Iterar basado en feedback

### Criterios de Éxito
- Todos los tests pasan
- Código cumple estándares de estilo
- Documentación actualizada
- Funcionalidad cumple requisitos
- No hay regresiones 