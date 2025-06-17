# ⚙️ Configuración Avanzada - Dark-Bot

## 🎯 Panel de Configuración Principal

Dark-Bot ofrece un sistema de configuración completo y flexible que te permite personalizar cada aspecto del bot según las necesidades de tu servidor.

## 🚀 Acceso Rápido

### Comando Principal
```
/config
```
Este comando abre el panel de configuración interactivo donde puedes:
- ✅ Ver configuración actual
- ✅ Modificar ajustes específicos
- ✅ Exportar/importar configuraciones
- ✅ Restaurar valores por defecto

## 📋 Categorías de Configuración

### 🎵 Configuración de Música

#### Configuración Básica
```
/music_setup
```

**Opciones Disponibles**:
- **Canal de Música**: Canal dedicado para comandos
- **Rol DJ**: Rol con permisos avanzados de música
- **Auto-desconexión**: Tiempo antes de desconectar por inactividad
- **Calidad de Audio**: Nivel de calidad (low/medium/high/ultra)
- **Límites de Cola**: Máximo de canciones por usuario/total

#### Configuración Avanzada
```
/music_config_advanced
```

**Configuraciones Técnicas**:
- **Región de Voz**: Servidor de voz preferido
- **Buffer de Audio**: Tamaño del buffer para estabilidad
- **Filtros por Defecto**: Filtros aplicados automáticamente
- **Integración Spotify**: Configuración de API de Spotify
- **Límites de API**: Gestión de cuotas de APIs externas

### 🛡️ Configuración de Moderación

#### Auto-Moderación
```
/automod_setup
```

**Funciones Configurables**:
- **Anti-Spam**: Detección y prevención de spam
- **Filtro de Palabras**: Lista de palabras prohibidas
- **Anti-Raid**: Protección contra raids
- **Límites de Menciones**: Máximo de menciones por mensaje
- **Filtro de Enlaces**: Control de enlaces externos

#### Logs de Moderación
```
/mod_logs_setup
```

**Eventos Registrados**:
- Mensajes eliminados/editados
- Usuarios baneados/expulsados
- Cambios de roles
- Entradas/salidas del servidor
- Acciones de moderación

### 🔧 Configuración del Verificador KQMC

#### Configuración Básica
```
/kqmc_setup
```

**Opciones Principales**:
- **Canal de Verificaciones**: Donde se muestran resultados
- **Formato de Resultados**: Estilo de los embeds
- **Límites de Uso**: Verificaciones por usuario/día
- **Cache de Resultados**: Tiempo de cache para UIDs

#### Configuración Avanzada
```
/kqmc_config_advanced
```

**Configuraciones Técnicas**:
- **Algoritmos de Cálculo**: Versión del algoritmo KQMC
- **Pesos de Stats**: Importancia de cada estadística
- **Umbrales de Calidad**: Límites para clasificaciones
- **Integración con APIs**: Configuración de APIs de Genshin

### 🎫 Sistema de Tickets

#### Configuración de Tickets
```
/ticket_setup
```

**Configuraciones**:
- **Categoría de Tickets**: Donde se crean los tickets
- **Roles de Staff**: Quién puede gestionar tickets
- **Mensaje de Bienvenida**: Mensaje inicial en tickets
- **Auto-cierre**: Tiempo antes de cerrar tickets inactivos
- **Logs de Tickets**: Canal para logs de tickets

### 🎮 Sistema de Niveles y XP

#### Configuración de Niveles
```
/level_config
```

**Opciones**:
- **XP por Mensaje**: Cantidad de XP ganada
- **Cooldown de XP**: Tiempo entre ganancias de XP
- **Canales Excluidos**: Canales sin XP
- **Multiplicadores de XP**: Bonificaciones por rol/canal
- **Recompensas por Nivel**: Roles automáticos por nivel

### 🔔 Sistema de Notificaciones

#### Configuración de Bienvenidas
```
/welcome_setup
```

**Configuraciones**:
- **Canal de Bienvenidas**: Donde se envían mensajes
- **Mensaje Personalizado**: Texto de bienvenida
- **Imagen de Bienvenida**: Banner personalizado
- **Roles Automáticos**: Roles asignados al unirse
- **DM de Bienvenida**: Mensaje privado opcional

#### Configuración de Despedidas
```
/goodbye_setup
```

**Opciones**:
- **Canal de Despedidas**: Donde se envían mensajes
- **Mensaje de Despedida**: Texto personalizado
- **Estadísticas de Salida**: Mostrar razón de salida

## 🔧 Configuraciones por Módulo

### Configuración de Entretenimiento
```
/entertainment_config
```

**Opciones**:
- **Comandos Habilitados**: Qué comandos están activos
- **Cooldowns**: Tiempo entre usos de comandos
- **Canales Permitidos**: Dónde funcionan los comandos
- **Filtros de Contenido**: Restricciones de contenido

### Configuración de Utilidades
```
/utility_config
```

**Configuraciones**:
- **Zona Horaria**: Zona horaria del servidor
- **Idioma**: Idioma de respuestas del bot
- **Formato de Fecha**: Cómo se muestran las fechas
- **Unidades de Medida**: Sistema métrico/imperial

### Configuración de APIs Externas
```
/api_config
```

**APIs Configurables**:
- **OpenWeatherMap**: Para comandos de clima
- **News API**: Para noticias
- **CoinGecko**: Para precios de criptomonedas
- **Alpha Vantage**: Para precios de acciones
- **Custom APIs**: APIs personalizadas

## 📊 Gestión de Configuraciones

### Exportar Configuración
```
/config_export
```

**Formatos Disponibles**:
- **JSON**: Formato técnico completo
- **YAML**: Formato legible por humanos
- **Backup**: Archivo de respaldo completo

### Importar Configuración
```
/config_import <archivo>
```

**Opciones de Importación**:
- **Sobrescribir Todo**: Reemplaza configuración completa
- **Fusionar**: Combina con configuración actual
- **Solo Módulos**: Importa módulos específicos

### Restaurar Configuración
```
/config_restore
```

**Opciones de Restauración**:
- **Valores por Defecto**: Configuración inicial
- **Último Backup**: Último respaldo automático
- **Backup Específico**: Respaldo seleccionado
- **Configuración de Plantilla**: Plantillas predefinidas

## 🔒 Configuración de Seguridad

### Configuración de Permisos
```
/permissions_config
```

**Gestión de Permisos**:
- **Permisos por Rol**: Configuración granular por rol
- **Permisos por Canal**: Restricciones por canal
- **Permisos por Usuario**: Excepciones específicas
- **Jerarquía de Permisos**: Orden de prioridad

### Configuración de Seguridad
```
/security_config
```

**Opciones de Seguridad**:
- **Rate Limiting**: Límites de uso de comandos
- **IP Whitelisting**: IPs permitidas para APIs
- **Encryption**: Cifrado de datos sensibles
- **Audit Logs**: Logs de seguridad detallados

## 🎨 Personalización Visual

### Configuración de Embeds
```
/embed_config
```

**Personalización**:
- **Colores**: Esquema de colores personalizado
- **Thumbnails**: Imágenes en embeds
- **Footers**: Texto de pie de página
- **Timestamps**: Mostrar marcas de tiempo

### Configuración de Emojis
```
/emoji_config
```

**Opciones**:
- **Emojis Personalizados**: Usar emojis del servidor
- **Emojis por Defecto**: Emojis estándar de Discord
- **Reacciones Automáticas**: Emojis en respuestas

## 📈 Configuración de Estadísticas

### Configuración de Métricas
```
/stats_config
```

**Métricas Disponibles**:
- **Uso de Comandos**: Estadísticas de comandos
- **Actividad de Usuarios**: Métricas de participación
- **Rendimiento del Bot**: Estadísticas técnicas
- **Métricas Personalizadas**: Métricas específicas del servidor

### Configuración de Reportes
```
/reports_config
```

**Tipos de Reportes**:
- **Reportes Diarios**: Resumen diario automático
- **Reportes Semanales**: Análisis semanal
- **Reportes Mensuales**: Estadísticas mensuales
- **Reportes Personalizados**: Reportes a medida

## 🔄 Configuración de Automatización

### Tareas Automáticas
```
/automation_config
```

**Automatizaciones**:
- **Limpieza Automática**: Eliminación de mensajes antiguos
- **Backups Automáticos**: Respaldos programados
- **Mantenimiento**: Tareas de mantenimiento automático
- **Notificaciones**: Alertas automáticas

### Configuración de Webhooks
```
/webhook_config
```

**Webhooks Disponibles**:
- **Logs Externos**: Envío de logs a servicios externos
- **Notificaciones**: Alertas a sistemas externos
- **Integraciones**: Conexión con otros bots/servicios

## 🛠️ Herramientas de Configuración

### Asistente de Configuración
```
/config_wizard
```

**Funciones del Asistente**:
- **Configuración Guiada**: Paso a paso
- **Recomendaciones**: Sugerencias basadas en el servidor
- **Validación**: Verificación de configuraciones
- **Pruebas**: Testing de configuraciones

### Diagnóstico de Configuración
```
/config_diagnostics
```

**Verificaciones**:
- **Configuraciones Conflictivas**: Detecta problemas
- **Configuraciones Faltantes**: Identifica vacíos
- **Optimizaciones**: Sugerencias de mejora
- **Compatibilidad**: Verifica compatibilidad

## 📋 Plantillas de Configuración

### Plantillas Predefinidas

#### Servidor de Gaming
```
/config_template gaming
```
- Enfoque en entretenimiento y música
- Moderación equilibrada
- Sistema de niveles activo
- Verificador KQMC optimizado

#### Servidor Comunitario
```
/config_template community
```
- Moderación estricta
- Bienvenidas elaboradas
- Sistema de tickets robusto
- Múltiples canales de logs

#### Servidor de Música
```
/config_template music
```
- Sistema de música avanzado
- Múltiples roles de DJ
- Playlists del servidor
- Estadísticas de música detalladas

#### Servidor Educativo
```
/config_template educational
```
- Moderación estricta
- Filtros de contenido activos
- Sistema de niveles educativo
- Herramientas de estudio

### Crear Plantillas Personalizadas
```
/config_template_create <nombre>
```

**Proceso**:
1. Configura tu servidor como desees
2. Exporta la configuración
3. Guárdala como plantilla
4. Úsala en otros servidores

## 🔍 Monitoreo de Configuración

### Logs de Cambios
```
/config_logs
```

**Información Registrada**:
- **Quién** hizo el cambio
- **Qué** se modificó
- **Cuándo** ocurrió el cambio
- **Valores anteriores** y nuevos

### Alertas de Configuración
```
/config_alerts
```

**Tipos de Alertas**:
- Cambios críticos de configuración
- Configuraciones que causan errores
- Configuraciones subóptimas
- Actualizaciones que requieren reconfiguración

## 🆘 Solución de Problemas de Configuración

### Problemas Comunes

#### "Configuración no se guarda"
**Soluciones**:
1. Verifica permisos del bot
2. Comprueba espacio de almacenamiento
3. Revisa logs de errores
4. Contacta soporte si persiste

#### "Comandos no funcionan después de configurar"
**Verificaciones**:
1. Reinicia el bot: `/restart`
2. Verifica permisos: `/permissions_check`
3. Revisa configuración: `/config_diagnostics`
4. Restaura backup: `/config_restore`

#### "Configuración se resetea sola"
**Posibles Causas**:
- Errores en la configuración
- Problemas de base de datos
- Conflictos de permisos
- Bugs del bot

**Soluciones**:
1. Crea backups frecuentes
2. Valida configuración antes de guardar
3. Reporta el problema a soporte

## 📞 Soporte de Configuración

### Recursos de Ayuda
- **[Guía de Configuración Básica](/setup)** - Primeros pasos
- **[Preguntas Frecuentes](/faq)** - Problemas comunes
- **[Servidor de Soporte](/support)** - Ayuda personalizada

### Configuración Personalizada
Para servidores con necesidades específicas:
- **Consultoría gratuita** para servidores grandes
- **Configuración asistida** por nuestro equipo
- **Plantillas personalizadas** para casos únicos

---

**¿Necesitas ayuda con una configuración específica?** Nuestro equipo está aquí para ayudarte. Únete a nuestro [servidor de soporte](/support) y trabajaremos contigo para crear la configuración perfecta para tu servidor.

**¿Tienes ideas para nuevas opciones de configuración?** ¡Nos encanta escuchar sugerencias! Comparte tus ideas y podrían aparecer en futuras actualizaciones.