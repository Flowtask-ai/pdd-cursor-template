# Ejemplo: Sistema de Notificaciones - PDD

## 🎯 CARACTERÍSTICA

Crear un sistema de notificaciones que permita enviar notificaciones por email y Slack con templates personalizables, rate limiting, y retry automático. El sistema debe integrarse con PostgreSQL para persistir el estado.

### Funcionalidades específicas:
- Envío de notificaciones por email usando SMTP
- Integración con Slack API para mensajes
- Sistema de templates con variables dinámicas
- Rate limiting por destinatario
- Retry automático con backoff exponencial
- API REST para envío programático

## 📚 EJEMPLOS

### Ejemplos de referencia:
- `examples/notification_service/` - Patrón para servicios de notificación
- `examples/api_endpoints/` - Patrón para endpoints REST
- `examples/database_models/` - Patrón para modelos con SQLAlchemy

### Cómo usar los ejemplos:
- **Sigue la estructura** del servicio de notificaciones existente
- **Adapta los patrones** de validación de API endpoints
- **Reutiliza la configuración** de base de datos

## 📖 DOCUMENTACIÓN

### Documentación técnica:
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [SQLAlchemy Documentation](https://docs.sqlalchemy.org/)
- [Slack API Documentation](https://api.slack.com/)

## ⚠️ OTRAS CONSIDERACIONES

### Requisitos técnicos:
- **Rate limiting**: Máximo 100 notificaciones por minuto por destinatario
- **Retry automático**: 3 intentos con backoff exponencial
- **Templates**: Soporte para variables {{variable}}

### Consideraciones de seguridad:
- **Autenticación**: API key requerida para envío programático
- **Validación**: Sanitización de templates para prevenir inyección
- **Logs**: No registrar información sensible

## 🎯 CRITERIOS DE ÉXITO

### Funcionalidad:
- [ ] Envío exitoso de emails a través de SMTP
- [ ] Integración funcional con Slack API
- [ ] Sistema de templates con variables dinámicas
- [ ] Rate limiting implementado y funcionando
- [ ] API REST funcional con autenticación

### Calidad:
- [ ] Todos los tests pasan (cobertura >90%)
- [ ] Código cumple estándares de estilo
- [ ] Documentación de API generada automáticamente

## 🔧 CONFIGURACIÓN REQUERIDA

### Variables de entorno:
```
# Base de datos
DATABASE_URL=postgresql://user:pass@localhost/notifications

# SMTP para emails
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASSWORD=your_app_password

# Slack
SLACK_BOT_TOKEN=xoxb-your-bot-token

# API
API_SECRET_KEY=your-secret-key-here
```

### Dependencias adicionales:
```
fastapi>=0.104.0
sqlalchemy>=2.0.0
slack-sdk>=3.21.0
aiosmtplib>=2.0.0
``` 