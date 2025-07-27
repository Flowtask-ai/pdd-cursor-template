# Prompt para Generar PRP

## 🎯 Instrucciones

Actúa como un experto en PDD (Prompt Driven Design). Genera un PRP (Product Requirements Prompt) completo siguiendo estas instrucciones:

## 📋 Proceso

### 1. Análisis
- **Lee completamente** `FEATURE_REQUEST.md`
- **Identifica todos los requisitos** técnicos y funcionales
- **Analiza los ejemplos** referenciados
- **Revisa la documentación** proporcionada

### 2. Investigación
- **Busca patrones similares** en el código existente
- **Consulta documentación** oficial de librerías
- **Identifica mejores prácticas** y gotchas conocidas

### 3. Creación
- **Usa la plantilla** en `.cursor/rules/templates/prp-base.mdc`
- **Incluye contexto completo** y documentación
- **Define pasos de implementación** detallados
- **Especifica validaciones** ejecutables

## 📝 Estructura Requerida

1. **Propósito y Contexto**
   - Descripción clara del objetivo
   - Contexto del proyecto y arquitectura

2. **Requisitos Técnicos**
   - Especificaciones detalladas
   - Dependencias y librerías

3. **Arquitectura y Diseño**
   - Estructura de archivos propuesta
   - Patrones de diseño a seguir

4. **Plan de Implementación**
   - Pasos detallados y secuenciales
   - Validaciones en cada paso

5. **Testing y Validación**
   - Estrategia de testing
   - Criterios de aceptación

6. **Criterios de Éxito**
   - Métricas específicas
   - Funcionalidad requerida

## 🔍 Validaciones

### Automáticas
```bash
# Sintaxis y estilo
ruff check --fix && mypy .

# Tests unitarios
pytest tests/ -v

# Cobertura
pytest --cov=src --cov-report=html
```

### Manuales
- [ ] Funcionalidad cumple requisitos
- [ ] Código sigue patrones del proyecto
- [ ] Documentación actualizada

## 📊 Calidad

### Checklist
- [ ] **Contexto completo**: Toda la información necesaria
- [ ] **Pasos claros**: Implementación paso a paso
- [ ] **Validaciones ejecutables**: Comandos que se pueden ejecutar
- [ ] **Referencias correctas**: Archivos y patrones existentes
- [ ] **Criterios medibles**: Éxito definido claramente

### Puntuación
**Evalúa el PRP en una escala de 1-10** basado en:
- Completitud del contexto (1-3 puntos)
- Claridad de implementación (1-3 puntos)
- Calidad de validaciones (1-2 puntos)
- Referencias y documentación (1-2 puntos)

## 📤 Salida

### Archivo a Crear
Guarda el PRP en `PRPs/[nombre-caracteristica].md`

### Contenido
- **PRP completo** siguiendo la plantilla
- **Puntuación de confianza** (1-10)
- **Justificación** de la puntuación 