# 🔧 Solución de Problemas - Sistema de Música

## 🚨 Problemas Más Comunes

### 🔇 El Bot No Reproduce Audio

#### **Síntoma**: El bot se conecta pero no se escucha nada

**Causas Posibles y Soluciones**:

1. **Permisos Insuficientes**
   ```
   Verificar: Configuración del Servidor → Roles → @Dark-Bot
   Permisos necesarios:
   ✅ Conectar
   ✅ Hablar
   ✅ Usar Actividad de Voz
   ```

2. **Problemas de Región del Servidor**
   ```
   /voice_region auto
   /reconnect
   ```

3. **Canal de Voz Lleno o Restringido**
   - Verifica que el canal no tenga límite de usuarios
   - Asegúrate de que el bot tenga permisos en ese canal específico

4. **Problemas de Codec de Audio**
   ```
   /audio_quality medium
   /reconnect
   ```

**Solución Rápida**:
```
/disconnect
/join
/play test song
```

### 🔌 El Bot No Se Conecta al Canal de Voz

#### **Síntoma**: Error "No se puede conectar al canal de voz"

**Diagnóstico Paso a Paso**:

1. **Verificar Estado del Bot**
   ```
   /music_diagnostics
   ```

2. **Comprobar Permisos**
   ```
   /check_permissions #canal-de-voz
   ```

3. **Forzar Reconexión**
   ```
   /force_disconnect
   /join #canal-de-voz
   ```

**Códigos de Error Comunes**:

| Código | Descripción | Solución |
|--------|-------------|----------|
| `VOICE_CONNECTION_TIMEOUT` | Timeout de conexión | Cambiar región del servidor |
| `VOICE_CHANNEL_FULL` | Canal lleno | Aumentar límite o usar otro canal |
| `INSUFFICIENT_PERMISSIONS` | Sin permisos | Verificar permisos del bot |
| `VOICE_SERVER_CRASHED` | Servidor de voz caído | Esperar o cambiar región |

### 🎵 Problemas de Reproducción

#### **Síntoma**: Las canciones se cortan o tienen lag

**Soluciones por Prioridad**:

1. **Optimizar Calidad de Audio**
   ```
   /audio_quality low     # Temporal
   /buffer_size large     # Aumenta estabilidad
   ```

2. **Verificar Conexión**
   ```
   /connection_test
   /ping                  # Verifica latencia
   ```

3. **Limpiar Cola**
   ```
   /queue_clear
   /cache_clear          # Limpia cache de canciones
   ```

4. **Reiniciar Sistema de Audio**
   ```
   /audio_restart
   ```

#### **Síntoma**: "No se puede encontrar la canción"

**Estrategias de Búsqueda**:

1. **Usar Términos Específicos**
   ```
   ❌ /play queen
   ✅ /play Queen - Bohemian Rhapsody
   ✅ /play https://youtube.com/watch?v=...
   ```

2. **Probar Diferentes Plataformas**
   ```
   /play youtube:Bohemian Rhapsody
   /play spotify:Bohemian Rhapsody
   /play soundcloud:Bohemian Rhapsody
   ```

3. **Verificar Restricciones Regionales**
   ```
   /region_check <canción>
   /vpn_mode enable       # Solo Premium
   ```

### ⚡ Problemas de Rendimiento

#### **Síntoma**: El bot responde lentamente

**Optimizaciones**:

1. **Reducir Carga del Sistema**
   ```
   /queue_limits 50       # Reduce tamaño máximo de cola
   /auto_disconnect 5     # Desconexión más rápida
   /cache_optimize        # Optimiza cache
   ```

2. **Verificar Recursos del Servidor**
   ```
   /server_stats
   /bot_performance
   ```

3. **Configurar Prioridades**
   ```
   /priority_mode music   # Prioriza sistema de música
   /background_tasks off  # Desactiva tareas no esenciales
   ```

## 🔍 Diagnóstico Avanzado

### Herramientas de Diagnóstico

#### `/music_diagnostics`
**Información Proporcionada**:
- Estado de conexión de voz
- Latencia de audio
- Uso de memoria
- Errores recientes
- Configuración actual
- Recomendaciones automáticas

#### `/connection_test`
**Pruebas Realizadas**:
- Velocidad de conexión
- Estabilidad de la conexión
- Calidad de audio
- Compatibilidad de codec
- Latencia de red

#### `/audio_analysis`
**Análisis Incluido**:
- Calidad de audio actual
- Pérdida de paquetes
- Jitter de red
- Recomendaciones de optimización

### Logs Detallados

#### Habilitar Logs Avanzados
```
/debug_mode enable
/log_level verbose
/music_logs #canal-logs
```

#### Interpretar Logs

**Tipos de Mensajes**:
- `[INFO]` - Información general
- `[WARN]` - Advertencias (no críticas)
- `[ERROR]` - Errores que requieren atención
- `[DEBUG]` - Información técnica detallada

**Ejemplos de Logs Importantes**:
```
[ERROR] Voice connection lost: VOICE_SERVER_CRASHED
[WARN] High latency detected: 250ms
[INFO] Successfully connected to voice channel
[DEBUG] Audio packet sent: seq=1234, timestamp=5678
```

## 🛠️ Soluciones por Categoría

### Problemas de Configuración

#### **Comandos No Funcionan**

1. **Verificar Permisos de Slash Commands**
   ```
   Configuración del Servidor → Integraciones → Dark-Bot
   ✅ Usar Comandos de Aplicación
   ```

2. **Reconfigurar Comandos**
   ```
   /commands_refresh
   /permissions_reset
   ```

3. **Verificar Restricciones de Canal**
   ```
   /music_channel_check
   /channel_permissions #canal
   ```

#### **Configuración Perdida**

1. **Restaurar desde Backup**
   ```
   /config_restore latest
   ```

2. **Reconfiguración Rápida**
   ```
   /quick_setup
   ```

3. **Configuración Manual**
   ```
   /music_setup
   /dj_role @DJ
   /music_channel #música
   ```

### Problemas de Red

#### **Alta Latencia**

**Soluciones Inmediatas**:
```
/voice_region closest     # Región más cercana
/buffer_size large        # Aumenta buffer
/quality_adaptive enable  # Calidad adaptativa
```

**Optimizaciones a Largo Plazo**:
- Contactar al proveedor de hosting
- Considerar servidor Premium
- Configurar CDN personalizado

#### **Desconexiones Frecuentes**

**Configuración de Estabilidad**:
```
/reconnect_auto enable
/connection_timeout 30
/retry_attempts 5
/fallback_servers enable
```

### Problemas de Plataforma

#### **YouTube**

**Errores Comunes**:
- `Video unavailable` - Video eliminado o privado
- `Age restricted` - Contenido con restricción de edad
- `Region blocked` - Bloqueado en tu región
- `Rate limited` - Demasiadas solicitudes

**Soluciones**:
```
/youtube_fallback enable
/age_bypass enable        # Solo con permisos
/proxy_mode enable        # Premium
/alternative_source auto
```

#### **Spotify**

**Problemas de Autenticación**:
```
/spotify_reauth
/spotify_credentials_check
/spotify_premium_verify
```

**Limitaciones de API**:
```
/spotify_quota_check
/api_usage_stats
/rate_limit_status
```

#### **SoundCloud**

**Problemas de Acceso**:
```
/soundcloud_status
/soundcloud_fallback enable
/direct_stream_mode enable
```

## 🚨 Problemas Críticos

### El Bot Está Completamente Inactivo

**Pasos de Emergencia**:

1. **Verificar Estado del Bot**
   - ¿Aparece online en Discord?
   - ¿Responde a comandos básicos como `/ping`?

2. **Reinicio de Emergencia**
   ```
   /emergency_restart
   ```

3. **Contactar Soporte Inmediato**
   - Discord: [Servidor de Soporte](/support)
   - Email: support@dark-bot.com
   - Status Page: status.dark-bot.com

### Pérdida de Datos

**Recuperación de Playlists**:
```
/playlist_recovery
/backup_restore emergency
/data_recovery_scan
```

**Recuperación de Configuración**:
```
/config_recovery
/settings_restore default
/emergency_config_load
```

## 📊 Monitoreo Preventivo

### Configurar Alertas

```
/alerts_setup
/monitor_enable performance
/threshold_set latency 200ms
/notification_channel #admin-alerts
```

**Tipos de Alertas**:
- Alta latencia (>200ms)
- Errores frecuentes (>5 por minuto)
- Desconexiones repetidas
- Uso excesivo de memoria
- Fallos de API externa

### Mantenimiento Regular

**Tareas Semanales**:
```
/cache_cleanup
/log_rotation
/performance_report
/backup_verify
```

**Tareas Mensuales**:
```
/full_diagnostics
/database_optimize
/config_audit
/security_check
```

## 🔧 Herramientas de Reparación

### Reparación Automática

```
/auto_repair enable
```

**Funciones Incluidas**:
- Detección automática de problemas
- Reparación de configuración corrupta
- Limpieza de cache automática
- Reconexión automática en fallos
- Restauración de backups en emergencias

### Reparación Manual

#### Reparar Base de Datos
```
/database_repair
/index_rebuild
/corruption_check
```

#### Reparar Configuración
```
/config_repair
/permissions_rebuild
/settings_validate
```

#### Reparar Cache
```
/cache_rebuild
/temp_files_clean
/memory_optimize
```

## 📞 Cuándo Contactar Soporte

### Problemas que Requieren Soporte Inmediato

- ✅ Bot completamente inactivo por más de 5 minutos
- ✅ Pérdida de datos importantes (playlists, configuración)
- ✅ Errores de seguridad o acceso no autorizado
- ✅ Problemas que afectan a múltiples servidores
- ✅ Errores críticos no documentados

### Información a Proporcionar al Soporte

**Información Básica**:
- ID del servidor de Discord
- Descripción detallada del problema
- Pasos para reproducir el error
- Capturas de pantalla de errores

**Información Técnica**:
```
/support_info_generate
```
Este comando genera un reporte técnico que incluye:
- Configuración actual
- Logs recientes
- Estado del sistema
- Información de diagnóstico

### Canales de Soporte

1. **Discord** - [Servidor de Soporte](/support)
   - Respuesta: 5-30 minutos
   - Disponible: 24/7
   - Idiomas: Español, Inglés

2. **Email** - support@dark-bot.com
   - Respuesta: 2-24 horas
   - Para problemas complejos
   - Incluye archivos adjuntos

3. **Documentación** - docs.dark-bot.com
   - Disponible: 24/7
   - Búsqueda avanzada
   - Guías paso a paso

4. **Status Page** - status.dark-bot.com
   - Estado de servicios en tiempo real
   - Mantenimientos programados
   - Historial de incidentes

## 🎯 Prevención de Problemas

### Mejores Prácticas

1. **Configuración Inicial Correcta**
   - Usar `/music_setup` para configuración automática
   - Verificar todos los permisos necesarios
   - Crear backup inmediatamente después de configurar

2. **Mantenimiento Regular**
   - Ejecutar `/music_diagnostics` semanalmente
   - Limpiar cache mensualmente
   - Actualizar configuración según necesidades

3. **Monitoreo Proactivo**
   - Configurar alertas para problemas comunes
   - Revisar logs regularmente
   - Mantener backups actualizados

4. **Educación del Equipo**
   - Entrenar a moderadores en comandos básicos
   - Documentar configuración específica del servidor
   - Establecer procedimientos para problemas comunes

### Lista de Verificación de Salud

**Verificación Diaria** (Automática):
- [ ] Bot responde a comandos
- [ ] Audio funciona correctamente
- [ ] No hay errores críticos en logs
- [ ] Latencia dentro de rangos normales

**Verificación Semanal** (Manual):
- [ ] Ejecutar diagnósticos completos
- [ ] Revisar estadísticas de uso
- [ ] Verificar integridad de backups
- [ ] Comprobar actualizaciones disponibles

**Verificación Mensual** (Manual):
- [ ] Auditoría completa de configuración
- [ ] Optimización de rendimiento
- [ ] Revisión de permisos y seguridad
- [ ] Planificación de mejoras

---

## 🆘 Contacto de Emergencia

Para problemas críticos que requieren atención inmediata:

- **Discord**: Menciona `@Support Team` en [nuestro servidor](/support)
- **Email Urgente**: emergency@dark-bot.com
- **Status Updates**: Síguenos en Twitter @DarkBotStatus

**Recuerda**: La mayoría de problemas se pueden resolver con las herramientas de diagnóstico integradas. Siempre intenta `/music_diagnostics` y `/auto_repair` antes de contactar soporte.

---

*¿Este problema no está cubierto en la guía? Ayúdanos a mejorar la documentación reportándolo en nuestro [servidor de soporte](/support).*