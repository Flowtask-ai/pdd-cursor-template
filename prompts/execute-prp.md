# Prompt para Ejecutar PRP

## 🎯 Instrucciones

Actúa como un desarrollador experto en PDD (Prompt Driven Design). Ejecuta el PRP en `[RUTA_DEL_PRP]` siguiendo estas instrucciones:

## 📋 Proceso

### 1. Análisis
- **Lee completamente** el PRP especificado
- **Entiende el contexto** y objetivos
- **Identifica todos los requisitos** técnicos y funcionales

### 2. Planificación
- **Crea un plan detallado** basado en los pasos del PRP
- **Identifica dependencias** entre componentes
- **Planifica el orden** de implementación

### 3. Implementación
- **Implementa cada componente** paso a paso
- **Ejecuta validaciones** después de cada paso
- **Corrige errores** automáticamente cuando sea posible

### 4. Validación
- **Ejecuta todas las validaciones** especificadas
- **Verifica criterios de éxito** definidos
- **Corrige problemas** encontrados

## 🔧 Estrategia

### Enfoque Modular
- **Implementa componentes** de forma independiente
- **Valida cada componente** antes de continuar
- **Mantén compatibilidad** con código existente

### Manejo de Errores
- **Captura errores** específicos y proporciona soluciones
- **Implementa logging** detallado para debugging
- **Proporciona mensajes de error** claros

### Validación Automática
- **Ejecuta tests** después de cada cambio significativo
- **Verifica sintaxis** y estilo del código
- **Comprueba integración** con componentes existentes

## 🧪 Testing

### Estrategia
- **Crea tests unitarios** para cada componente
- **Implementa tests de integración** para componentes complejos
- **Incluye tests de edge cases** y manejo de errores

### Validaciones
```bash
# Sintaxis y estilo
ruff check --fix && mypy .

# Tests unitarios
pytest tests/ -v

# Cobertura
pytest --cov=src --cov-report=html
```

### Criterios de Aceptación
- **Funcionalidad cumple** requisitos especificados
- **Código pasa** todas las validaciones automáticas
- **Documentación está** actualizada
- **No hay regresiones** en funcionalidad existente

## 🔄 Iteración

### Proceso de Refinamiento
- **Identifica problemas** durante la implementación
- **Propone mejoras** basadas en hallazgos
- **Itera sobre la implementación** hasta que sea correcta

### Corrección de Errores
- **Analiza errores** de validación automática
- **Implementa correcciones** específicas
- **Verifica que las correcciones** resuelven el problema

## 📊 Monitoreo

### Seguimiento
- **Marca pasos completados** según el PRP
- **Registra problemas** encontrados y soluciones
- **Actualiza estado** del proyecto

### Métricas
- **Cobertura de código** alcanzada
- **Tests pasando** exitosamente
- **Validaciones automáticas** exitosas

## 🎯 Mejores Prácticas

### Implementación
- **Sigue el plan** del PRP estrictamente
- **Mantén consistencia** con patrones del proyecto
- **Implementa de forma incremental** y valida cada paso

### Comunicación
- **Proporciona actualizaciones** regulares del progreso
- **Explica decisiones** de implementación
- **Solicita aclaraciones** cuando sea necesario

### Calidad
- **Mantén estándares** de código del proyecto
- **Implementa manejo de errores** robusto
- **Incluye logging** apropiado

## 🔍 Validación Final

### Verificación
- **Ejecuta todas las validaciones** del PRP
- **Verifica criterios de éxito** uno por uno
- **Confirma funcionalidad** según especificaciones

### Documentación
- **Actualiza README.md** si es necesario
- **Completa docstrings** de funciones
- **Actualiza documentación** de API si aplica

## 📤 Reporte

### Resumen
- **Componentes implementados** exitosamente
- **Problemas encontrados** y soluciones aplicadas
- **Mejoras realizadas** durante la implementación

### Estado Final
- **Todos los criterios de éxito** cumplidos
- **Validaciones automáticas** pasando
- **Código listo** para producción 