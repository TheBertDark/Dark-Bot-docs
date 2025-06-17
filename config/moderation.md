# 🛡️ Configuración de Moderación - Dark-Bot

## 🎯 Sistema de Moderación Avanzado

Dark-Bot incluye un sistema de moderación completo y automatizado que te ayuda a mantener tu servidor seguro y organizado. Esta guía te mostrará cómo configurar cada aspecto del sistema de moderación.

## 🚀 Configuración Inicial

### Comando Principal
```
/moderation_setup
```
Este comando inicia el asistente de configuración de moderación que te guiará paso a paso.

### Configuración Rápida
```
/moderation_quicksetup
```
Configura la moderación básica en menos de 2 minutos con valores recomendados.

## 🔧 Auto-Moderación

### Configuración de Anti-Spam
```
/automod_spam
```

**Opciones Configurables**:
- **Límite de Mensajes**: Máximo de mensajes por minuto (1-20)
- **Tiempo de Cooldown**: Segundos entre mensajes (1-60)
- **Mensajes Duplicados**: Máximo de mensajes idénticos (1-5)
- **Acción**: Warn/Mute/Kick/Ban
- **Duración del Mute**: Tiempo de silenciamiento (1m-24h)

**Configuración Recomendada**:
```yaml
Límite de Mensajes: 8 por minuto
Cooldown: 3 segundos
Mensajes Duplicados: 3 máximo
Acción: Mute por 10 minutos
```

### Filtro de Palabras
```
/automod_words
```

**Funciones**:
- **Lista Negra**: Palabras completamente prohibidas
- **Lista de Advertencia**: Palabras que generan warnings
- **Excepciones**: Roles/canales exentos del filtro
- **Sensibilidad**: Nivel de detección (bajo/medio/alto)
- **Acción Automática**: Respuesta a palabras prohibidas

**Configuración por Severidad**:

#### Nivel Bajo (Advertencias)
- Palabras levemente inapropiadas
- Acción: Warning automático
- Sin eliminación de mensaje

#### Nivel Medio (Moderado)
- Insultos y lenguaje ofensivo
- Acción: Eliminación + Warning
- Mute temporal opcional

#### Nivel Alto (Severo)
- Contenido extremadamente ofensivo
- Acción: Ban temporal/permanente
- Eliminación inmediata

### Anti-Raid Protection
```
/automod_raid
```

**Configuraciones**:
- **Límite de Joins**: Usuarios por minuto (5-50)
- **Tiempo de Ventana**: Período de análisis (1-10 minutos)
- **Acción de Raid**: Lockdown/Kick nuevos/Ban temporal
- **Duración del Lockdown**: Tiempo de bloqueo (5m-24h)
- **Whitelist de Roles**: Roles exentos de restricciones

**Configuración Anti-Raid Recomendada**:
```yaml
Límite de Joins: 15 por minuto
Ventana de Tiempo: 2 minutos
Acción: Lockdown por 30 minutos
Kick automático: Usuarios sin verificar
```

### Control de Menciones
```
/automod_mentions
```

**Límites Configurables**:
- **Menciones de Usuario**: Máximo por mensaje (1-20)
- **Menciones de Rol**: Máximo por mensaje (1-5)
- **Menciones @everyone/@here**: Permitir/Prohibir
- **Acción**: Warning/Mute/Eliminación
- **Excepciones**: Roles con permisos especiales

### Filtro de Enlaces
```
/automod_links
```

**Configuraciones**:
- **Enlaces Permitidos**: Whitelist de dominios
- **Enlaces Prohibidos**: Blacklist de dominios
- **Invitaciones de Discord**: Permitir/Prohibir/Solo del servidor
- **Acortadores de URL**: Permitir/Prohibir
- **Acción**: Eliminación/Warning/Mute

**Categorías de Enlaces**:

#### Enlaces Seguros (Siempre Permitidos)
- YouTube, Spotify, Twitch
- GitHub, Stack Overflow
- Sitios educativos reconocidos
- Documentación oficial

#### Enlaces Sospechosos (Revisión Manual)
- Acortadores de URL
- Sitios de descarga
- Enlaces con muchos redirects
- Dominios nuevos o desconocidos

#### Enlaces Prohibidos (Bloqueados)
- Sitios maliciosos conocidos
- Contenido para adultos
- Sitios de phishing
- Invitaciones de servidores competidores

## 📋 Logs de Moderación

### Configuración de Logs
```
/modlogs_setup
```

**Canales de Logs Recomendados**:
- **#mod-logs**: Acciones de moderación
- **#message-logs**: Mensajes editados/eliminados
- **#join-leave-logs**: Entradas y salidas
- **#voice-logs**: Actividad de canales de voz
- **#role-logs**: Cambios de roles

### Tipos de Eventos Registrados

#### Logs de Mensajes
```
/modlogs_messages
```
- Mensajes eliminados (con contenido)
- Mensajes editados (antes/después)
- Mensajes en masa eliminados
- Reacciones añadidas/removidas

#### Logs de Usuarios
```
/modlogs_users
```
- Usuarios que se unen/salen
- Cambios de nickname
- Cambios de avatar
- Actualizaciones de perfil

#### Logs de Moderación
```
/modlogs_moderation
```
- Warnings dados
- Mutes aplicados/removidos
- Kicks y bans
- Timeouts aplicados
- Acciones de auto-moderación

#### Logs de Servidor
```
/modlogs_server
```
- Cambios en canales
- Modificaciones de roles
- Actualizaciones del servidor
- Cambios en permisos

## ⚡ Acciones de Moderación

### Sistema de Warnings
```
/warnings_config
```

**Configuración de Warnings**:
- **Límite de Warnings**: Máximo antes de acción (3-10)
- **Expiración**: Tiempo antes de que expiren (1d-never)
- **Acciones Escaladas**: Qué hacer al alcanzar límites
- **Notificaciones**: Avisar al usuario por DM

**Escalación de Acciones**:
```yaml
3 Warnings: Mute por 1 hora
5 Warnings: Mute por 24 horas
7 Warnings: Kick del servidor
10 Warnings: Ban temporal (7 días)
```

### Sistema de Mutes
```
/mute_config
```

**Configuraciones**:
- **Rol de Mute**: Rol aplicado a usuarios silenciados
- **Duración Máxima**: Tiempo máximo de mute (1h-30d)
- **Canales Afectados**: Dónde aplica el mute
- **Auto-Unmute**: Remoción automática al expirar
- **Logs de Mute**: Registro de mutes aplicados

### Configuración de Bans
```
/ban_config
```

**Opciones**:
- **Eliminación de Mensajes**: Días de mensajes a eliminar (0-7)
- **Ban Appeals**: Sistema de apelaciones
- **Bans Temporales**: Duración máxima (1d-365d)
- **Notificación de Ban**: Mensaje al usuario baneado
- **Logs de Bans**: Registro detallado

## 🎭 Roles de Moderación

### Configuración de Roles
```
/mod_roles_setup
```

**Jerarquía de Moderación**:

#### Helper/Ayudante
- Dar warnings
- Mute temporal (máx. 1 hora)
- Ver logs básicos
- Responder tickets

#### Moderador
- Todas las funciones de Helper
- Kick usuarios
- Mute hasta 24 horas
- Gestionar mensajes
- Configurar auto-moderación básica

#### Moderador Senior
- Todas las funciones de Moderador
- Ban temporal (máx. 30 días)
- Configurar filtros avanzados
- Gestionar otros moderadores
- Acceso a logs completos

#### Administrador
- Todas las funciones anteriores
- Ban permanente
- Configuración completa del bot
- Gestión de roles de moderación
- Acceso a configuración del servidor

### Permisos por Rol
```
/mod_permissions
```

**Configuración Granular**:
- **Por Comando**: Qué comandos puede usar cada rol
- **Por Canal**: Restricciones por canal
- **Por Acción**: Límites en acciones de moderación
- **Excepciones**: Usuarios con permisos especiales

## 🔍 Herramientas de Moderación

### Panel de Moderación
```
/mod_panel
```

**Funciones del Panel**:
- Vista general de infracciones recientes
- Usuarios con más warnings
- Estadísticas de moderación
- Acciones rápidas
- Estado de auto-moderación

### Búsqueda de Infracciones
```
/mod_search <usuario/tipo/fecha>
```

**Filtros Disponibles**:
- **Por Usuario**: Historial específico
- **Por Tipo**: Warnings, mutes, bans, etc.
- **Por Fecha**: Rango de fechas
- **Por Moderador**: Quién aplicó la acción
- **Por Razón**: Búsqueda en razones

### Estadísticas de Moderación
```
/mod_stats
```

**Métricas Incluidas**:
- Infracciones por día/semana/mes
- Tipos de infracciones más comunes
- Moderadores más activos
- Efectividad de auto-moderación
- Tendencias de comportamiento

## 🛠️ Configuraciones Avanzadas

### Auto-Moderación Inteligente
```
/automod_ai
```

**Funciones de IA**:
- **Detección de Contexto**: Análisis del contexto del mensaje
- **Detección de Sarcasmo**: Identificar sarcasmo vs. insultos reales
- **Análisis de Sentimiento**: Evaluar tono del mensaje
- **Detección de Spam Sofisticado**: Spam que evade filtros básicos

### Configuración de Excepciones
```
/automod_exceptions
```

**Tipos de Excepciones**:
- **Roles Exentos**: Roles que ignoran ciertas reglas
- **Canales Especiales**: Canales con reglas diferentes
- **Horarios**: Reglas diferentes según la hora
- **Eventos**: Excepciones durante eventos especiales

### Sistema de Apelaciones
```
/appeals_setup
```

**Configuración**:
- **Canal de Apelaciones**: Donde se envían las apelaciones
- **Formulario**: Preguntas para la apelación
- **Tiempo Límite**: Cuándo se pueden hacer apelaciones
- **Revisores**: Quién puede revisar apelaciones
- **Proceso**: Pasos del proceso de apelación

## 📊 Reportes y Análisis

### Reportes Automáticos
```
/mod_reports_config
```

**Tipos de Reportes**:
- **Reporte Diario**: Resumen de actividad diaria
- **Reporte Semanal**: Análisis semanal detallado
- **Reporte de Incidentes**: Alertas de problemas graves
- **Reporte de Tendencias**: Cambios en patrones de comportamiento

### Análisis de Comportamiento
```
/behavior_analysis
```

**Métricas Analizadas**:
- Patrones de infracciones
- Horarios de mayor actividad problemática
- Correlación entre eventos y comportamiento
- Efectividad de diferentes acciones de moderación

## 🔄 Integración con Otros Sistemas

### Integración con Tickets
```
/mod_ticket_integration
```

**Funciones**:
- Crear tickets automáticamente para infracciones graves
- Historial de moderación en tickets
- Escalación automática a staff senior
- Seguimiento de resolución de problemas

### Integración con Niveles
```
/mod_level_integration
```

**Configuraciones**:
- Pérdida de XP por infracciones
- Restricciones de nivel por comportamiento
- Recompensas por buen comportamiento
- Sistema de rehabilitación

## 🆘 Solución de Problemas

### Problemas Comunes

#### "Auto-moderación muy estricta"
**Soluciones**:
1. Ajustar sensibilidad de filtros
2. Añadir excepciones para roles de confianza
3. Revisar configuración de límites
4. Implementar sistema de warnings graduales

#### "Muchos falsos positivos"
**Verificaciones**:
1. Revisar lista de palabras filtradas
2. Ajustar configuración de contexto
3. Añadir excepciones específicas
4. Entrenar filtros con ejemplos del servidor

#### "Logs muy saturados"
**Optimizaciones**:
1. Filtrar eventos menos importantes
2. Usar canales separados por tipo
3. Configurar rotación de logs
4. Implementar sistema de archivado

### Configuración de Emergencia
```
/mod_emergency
```

**Funciones de Emergencia**:
- **Lockdown Total**: Bloquear todo el servidor
- **Mute Masivo**: Silenciar múltiples usuarios
- **Purge Rápido**: Eliminar mensajes en masa
- **Ban de Emergencia**: Ban rápido con confirmación mínima

## 📞 Soporte y Recursos

### Recursos de Ayuda
- **[Guía de Moderación Básica](/setup#moderacion)** - Primeros pasos
- **[Comandos de Moderación](/commands/)** - Lista completa
- **[Preguntas Frecuentes](/faq#moderacion)** - Problemas comunes
- **[Servidor de Soporte](/support)** - Ayuda personalizada

### Mejores Prácticas

#### Para Servidores Pequeños (< 100 miembros)
- Auto-moderación básica
- Logs simplificados
- Moderación manual principalmente
- Enfoque en comunidad

#### Para Servidores Medianos (100-1000 miembros)
- Auto-moderación moderada
- Sistema de warnings activo
- Múltiples moderadores
- Logs detallados

#### Para Servidores Grandes (> 1000 miembros)
- Auto-moderación estricta
- Múltiples niveles de moderación
- Sistemas automatizados
- Análisis de comportamiento

---

**¿Necesitas ayuda configurando la moderación?** Nuestro equipo puede ayudarte a crear un sistema de moderación personalizado para tu servidor. Únete a nuestro [servidor de soporte](/support) para obtener asistencia especializada.

**¿Tienes sugerencias para mejorar el sistema de moderación?** ¡Nos encanta recibir feedback! Tus ideas pueden convertirse en nuevas funciones en futuras actualizaciones.