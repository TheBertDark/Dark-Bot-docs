# 🔐 Sistema de Permisos - Dark-Bot

## 🎯 Gestión Avanzada de Permisos

Dark-Bot incluye un sistema de permisos granular que te permite controlar exactamente qué usuarios pueden usar qué comandos y funciones en tu servidor.

## 🚀 Configuración Inicial

### Comando Principal
```
/permissions_setup
```
Este comando inicia el asistente de configuración de permisos que te guiará paso a paso.

### Verificar Permisos Actuales
```
/permissions_check [usuario/rol]
```
Muestra los permisos actuales de un usuario o rol específico.

## 📋 Tipos de Permisos

### Permisos por Comando
```
/permissions_command <comando> <rol/usuario> <permitir/denegar>
```

**Ejemplos**:
```
/permissions_command music @DJ permitir
/permissions_command ban @Moderador permitir
/permissions_command kqmc @everyone denegar
```

**Comandos Configurables**:
- **Música**: `/play`, `/skip`, `/queue`, `/playlist`
- **Moderación**: `/ban`, `/kick`, `/mute`, `/warn`
- **Configuración**: `/config`, `/setup`, `/permissions`
- **KQMC**: `/tc`, `/kqmc_config`
- **Utilidades**: `/weather`, `/translate`, `/remind`
- **Entretenimiento**: `/meme`, `/joke`, `/8ball`

### Permisos por Categoría
```
/permissions_category <categoría> <rol/usuario> <nivel>
```

**Categorías Disponibles**:
- **music**: Sistema de música completo
- **moderation**: Herramientas de moderación
- **config**: Configuración del bot
- **kqmc**: Verificador KQMC
- **utility**: Comandos de utilidad
- **entertainment**: Entretenimiento
- **admin**: Administración del servidor

**Niveles de Permiso**:
- **none**: Sin acceso
- **basic**: Funciones básicas
- **advanced**: Funciones avanzadas
- **full**: Acceso completo

### Permisos por Canal
```
/permissions_channel <canal> <comando/categoría> <rol/usuario> <permitir/denegar>
```

**Casos de Uso**:
- Restringir música a canales específicos
- Limitar comandos de moderación a canales de staff
- Permitir KQMC solo en canales de builds
- Configurar canales de entretenimiento

## 🔧 Configuración Avanzada

### Jerarquía de Permisos
```
/permissions_hierarchy
```

**Orden de Prioridad** (de mayor a menor):
1. **Permisos de Usuario Específico**: Configuración individual
2. **Permisos de Rol Más Alto**: Rol con mayor jerarquía
3. **Permisos de Canal**: Configuración por canal
4. **Permisos por Defecto**: Configuración global
5. **Permisos de Discord**: Permisos nativos de Discord

### Grupos de Permisos
```
/permissions_group_create <nombre>
```

**Funciones de Grupos**:
- Crear conjuntos de permisos reutilizables
- Aplicar a múltiples roles/usuarios
- Facilitar gestión de permisos complejos
- Plantillas para diferentes tipos de servidores

**Grupos Predefinidos**:
- **Moderador Básico**: Warn, mute temporal, gestión de mensajes
- **Moderador Avanzado**: Kick, ban temporal, configuración básica
- **Administrador**: Acceso completo excepto configuración crítica
- **DJ**: Control completo del sistema de música
- **Helper**: Comandos de ayuda y utilidades básicas

### Permisos Temporales
```
/permissions_temp <usuario> <permiso> <duración>
```

**Casos de Uso**:
- Permisos de moderación temporal
- Acceso especial durante eventos
- Pruebas de nuevos moderadores
- Permisos de emergencia

**Ejemplos**:
```
/permissions_temp @Usuario moderation 24h
/permissions_temp @EventStaff music 3d
/permissions_temp @TrialMod basic_mod 7d
```

## 🛡️ Permisos de Seguridad

### Permisos Críticos
```
/permissions_critical
```

**Permisos que Requieren Autorización Especial**:
- **Configuración del Bot**: Cambios en configuración principal
- **Gestión de Permisos**: Modificar sistema de permisos
- **Comandos de Administración**: Reiniciar, actualizar, debug
- **Acceso a Logs**: Ver logs completos del sistema
- **Gestión de Base de Datos**: Backup, restore, migrate

### Protección contra Escalada
```
/permissions_protection
```

**Medidas de Seguridad**:
- **Límite de Jerarquía**: No otorgar permisos superiores a los propios
- **Confirmación Doble**: Requerir confirmación para cambios críticos
- **Logs de Cambios**: Registrar todos los cambios de permisos
- **Reversión Automática**: Deshacer cambios problemáticos
- **Alertas de Seguridad**: Notificar cambios sospechosos

### Auditoría de Permisos
```
/permissions_audit
```

**Información de Auditoría**:
- **Historial de Cambios**: Quién cambió qué y cuándo
- **Permisos Inusuales**: Configuraciones fuera de lo normal
- **Usuarios con Muchos Permisos**: Posibles riesgos de seguridad
- **Permisos Sin Usar**: Optimización de configuración
- **Conflictos**: Permisos contradictorios

## 📊 Gestión de Roles

### Roles de Moderación
```
/permissions_mod_roles
```

**Configuración de Roles de Staff**:

#### Helper/Ayudante
```yaml
Permisos:
  - Comandos básicos de moderación
  - Ver logs básicos
  - Responder tickets
  - Usar comandos de utilidad
  - Acceso a canales de staff básicos

Restricciones:
  - No puede banear o kickear
  - Mute máximo de 1 hora
  - No puede modificar configuración
```

#### Moderador
```yaml
Permisos:
  - Todos los permisos de Helper
  - Kick usuarios
  - Ban temporal (máx. 7 días)
  - Mute hasta 24 horas
  - Gestión completa de mensajes
  - Configuración básica del bot

Restricciones:
  - No puede modificar permisos
  - No puede banear permanentemente
  - No puede acceder a configuración crítica
```

#### Moderador Senior
```yaml
Permisos:
  - Todos los permisos de Moderador
  - Ban permanente
  - Configuración avanzada
  - Gestión de otros moderadores
  - Acceso a logs completos
  - Modificar algunos permisos

Restricciones:
  - No puede modificar administradores
  - No puede cambiar configuración crítica
```

#### Administrador
```yaml
Permisos:
  - Acceso completo al bot
  - Modificar cualquier configuración
  - Gestionar todos los permisos
  - Acceso a funciones de debug
  - Gestión de base de datos

Restricciones:
  - Algunas acciones requieren confirmación
  - Logs de todas las acciones críticas
```

### Roles Especializados
```
/permissions_special_roles
```

#### DJ/Música
```yaml
Permisos de Música:
  - Control completo de reproducción
  - Gestión de playlists del servidor
  - Configuración de música
  - Moderación de contenido musical
  - Estadísticas de música
```

#### Event Manager
```yaml
Permisos de Eventos:
  - Crear y gestionar eventos
  - Configurar notificaciones
  - Gestionar inscripciones
  - Acceso a herramientas de evento
  - Permisos temporales durante eventos
```

#### KQMC Expert
```yaml
Permisos KQMC:
  - Configuración del verificador
  - Acceso a estadísticas avanzadas
  - Moderación de resultados
  - Ayuda especializada a usuarios
  - Gestión de base de datos KQMC
```

## 🔍 Monitoreo y Logs

### Logs de Permisos
```
/permissions_logs
```

**Eventos Registrados**:
- Cambios de permisos
- Intentos de acceso denegado
- Uso de permisos críticos
- Escaladas de permisos
- Errores de configuración

### Alertas de Seguridad
```
/permissions_alerts
```

**Tipos de Alertas**:
- **Cambios Críticos**: Modificaciones importantes
- **Accesos Sospechosos**: Intentos inusuales
- **Escaladas**: Otorgamiento de permisos altos
- **Errores**: Problemas de configuración
- **Violaciones**: Intentos de bypass

### Reportes de Uso
```
/permissions_reports
```

**Información de Reportes**:
- Comandos más usados por rol
- Usuarios más activos
- Permisos más solicitados
- Tendencias de uso
- Recomendaciones de optimización

## 🛠️ Herramientas de Gestión

### Backup de Permisos
```
/permissions_backup
```

**Funciones de Backup**:
- Crear respaldo completo de permisos
- Programar backups automáticos
- Restaurar desde backup
- Comparar configuraciones
- Exportar/importar configuraciones

### Plantillas de Permisos
```
/permissions_template
```

**Plantillas Disponibles**:
- **Servidor Gaming**: Configuración para gaming
- **Servidor Comunitario**: Enfoque en comunidad
- **Servidor Educativo**: Permisos educativos
- **Servidor de Música**: Centrado en música
- **Servidor de Roleplay**: Para roleplay

### Migración de Permisos
```
/permissions_migrate
```

**Opciones de Migración**:
- Migrar desde otro bot
- Importar desde archivo
- Copiar de otro servidor
- Fusionar configuraciones
- Actualizar estructura antigua

## 🔧 Configuración por Servidor

### Configuración Multi-Servidor
```
/permissions_multi_server
```

**Funciones**:
- Sincronizar permisos entre servidores
- Configuración global para múltiples servidores
- Roles compartidos
- Gestión centralizada
- Estadísticas combinadas

### Permisos por Región
```
/permissions_region
```

**Configuraciones Regionales**:
- Diferentes permisos por zona horaria
- Restricciones por ubicación
- Configuración cultural específica
- Cumplimiento de regulaciones locales

## 🆘 Solución de Problemas

### Problemas Comunes

#### "Usuario no puede usar comando"
**Diagnóstico**:
1. Verificar permisos del usuario: `/permissions_check @usuario`
2. Comprobar permisos del rol: `/permissions_check @rol`
3. Revisar restricciones de canal
4. Verificar jerarquía de roles
5. Comprobar permisos de Discord

#### "Permisos no se aplican correctamente"
**Soluciones**:
1. Reiniciar sistema de permisos: `/permissions_reload`
2. Verificar conflictos: `/permissions_conflicts`
3. Revisar jerarquía: `/permissions_hierarchy`
4. Comprobar cache: `/permissions_cache_clear`

#### "Cambios de permisos no se guardan"
**Verificaciones**:
1. Comprobar permisos del bot
2. Verificar espacio de almacenamiento
3. Revisar logs de errores
4. Contactar soporte si persiste

### Herramientas de Diagnóstico
```
/permissions_diagnose
```

**Verificaciones Automáticas**:
- Configuración de permisos
- Conflictos y contradicciones
- Permisos faltantes o excesivos
- Problemas de jerarquía
- Errores de configuración

## 📞 Soporte y Recursos

### Recursos de Ayuda
- **[Guía de Configuración Básica](/setup)** - Primeros pasos
- **[Preguntas Frecuentes](/faq)** - Problemas comunes
- **[Servidor de Soporte](/support)** - Ayuda personalizada

### Mejores Prácticas

#### Principio de Menor Privilegio
- Otorgar solo los permisos necesarios
- Revisar permisos regularmente
- Remover permisos no utilizados
- Usar roles en lugar de permisos individuales

#### Gestión de Roles
- Crear jerarquía clara de roles
- Usar nombres descriptivos
- Documentar responsabilidades
- Revisar membresía de roles regularmente

#### Seguridad
- Hacer backups regulares
- Monitorear cambios críticos
- Usar confirmación doble para cambios importantes
- Mantener logs de auditoría

---

**¿Necesitas ayuda configurando permisos complejos?** Nuestro equipo puede ayudarte a diseñar un sistema de permisos seguro y eficiente. Únete a nuestro [servidor de soporte](/support) para obtener asistencia especializada.

**¿Tienes sugerencias para mejorar el sistema de permisos?** ¡Nos encanta recibir feedback! Tus ideas podrían convertirse en nuevas funciones en futuras actualizaciones.