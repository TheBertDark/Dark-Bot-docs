# 🎛️ Configuración del Sistema de Música - Dark-Bot

## 🚀 Configuración Inicial

### Paso 1: Configuración Automática
La forma más rápida de configurar el sistema de música es usar el comando de configuración automática:

```
/music_setup
```

Este comando iniciará un asistente interactivo que te guiará a través de:
- ✅ Verificación de permisos del bot
- ✅ Configuración de canal de música
- ✅ Creación de rol DJ
- ✅ Configuración básica de permisos
- ✅ Prueba de conectividad de audio

### Paso 2: Verificación de Permisos
Asegúrate de que Dark-Bot tenga los siguientes permisos:

#### Permisos de Canal de Voz
- **Conectar** - Para unirse a canales de voz
- **Hablar** - Para reproducir audio
- **Usar Actividad de Voz** - Para detectar comandos de voz
- **Mover Miembros** - Para funciones avanzadas

#### Permisos de Canal de Texto
- **Ver Canal** - Para leer comandos
- **Enviar Mensajes** - Para responder
- **Insertar Enlaces** - Para mostrar información de canciones
- **Usar Comandos de Barra** - Para comandos slash
- **Gestionar Mensajes** - Para limpiar comandos

## 🎯 Configuración Detallada

### Configuración de Roles

#### Crear Rol DJ
1. **Ve a Configuración del Servidor → Roles**
2. **Crea un nuevo rol llamado "DJ"**
3. **Asigna permisos básicos** (no necesita permisos especiales de Discord)
4. **Configura el rol en el bot**:
   ```
   /dj_role @DJ
   ```

#### Configurar Permisos por Rol
```
/music_permissions
```
Esto abrirá un menú interactivo donde puedes:
- **Asignar permisos específicos** a diferentes roles
- **Crear jerarquías de control**
- **Establecer restricciones por canal**

### Configuración de Canales

#### Canal Dedicado para Música
Recomendamos crear un canal específico para comandos de música:

1. **Crea un canal de texto** llamado `#música` o `#music`
2. **Configúralo en el bot**:
   ```
   /music_channel #música
   ```
3. **Beneficios**:
   - Mantiene organizados los comandos
   - Evita spam en otros canales
   - Permite configuraciones específicas

#### Múltiples Canales de Voz
Puedes configurar diferentes canales de voz para diferentes propósitos:

```
/voice_channel_config #General "Música general"
/voice_channel_config #Lounge "Música relajante"
/voice_channel_config #Party "Música de fiesta"
```

### Configuración de Audio

#### Calidad de Audio
```
/audio_quality <nivel>
```
**Niveles disponibles**:
- `low` - 96 kbps (menor uso de ancho de banda)
- `medium` - 128 kbps (equilibrio recomendado)
- `high` - 192 kbps (mejor calidad)
- `ultra` - 320 kbps (máxima calidad, solo Premium)

#### Configuración de Región
```
/voice_region <región>
```
**Regiones disponibles**:
- `auto` - Selección automática
- `us-east` - Estados Unidos Este
- `us-west` - Estados Unidos Oeste
- `europe` - Europa
- `asia` - Asia
- `brazil` - Brasil

## ⚙️ Configuraciones Avanzadas

### Auto-Desconexión
Configura cuándo el bot debe desconectarse automáticamente:

```
/auto_disconnect <minutos>
```

**Opciones recomendadas**:
- **5 minutos** - Para servidores muy activos
- **10 minutos** - Configuración estándar
- **30 minutos** - Para servidores grandes
- **0** - Nunca desconectar (no recomendado)

### Límites de Cola
Configura límites para evitar abuso:

```
/queue_limits
```

**Configuraciones**:
- **Máximo de canciones por usuario**: 5-20
- **Duración máxima por canción**: 10-30 minutos
- **Tamaño máximo de cola**: 50-200 canciones

### Filtros de Contenido
Configura qué tipo de contenido está permitido:

```
/content_filters
```

**Opciones**:
- **Bloquear contenido explícito**: Sí/No
- **Filtrar por duración**: Máximo X minutos
- **Restricciones de edad**: Solo contenido apropiado
- **Blacklist de palabras**: Lista personalizada

### Configuración de Playlists

#### Límites de Playlists
```
/playlist_limits
```
- **Playlists por usuario**: 5-20
- **Canciones por playlist**: 50-500
- **Playlists públicas**: Permitir/Denegar

#### Playlists del Servidor
Crea playlists compartidas para todo el servidor:

```
/server_playlist_create "Rock Clásico"
/server_playlist_create "Música de Trabajo"
/server_playlist_create "Fiesta del Viernes"
```

## 🔧 Configuración por Tipo de Servidor

### Servidor de Gaming
```yaml
Configuración Recomendada:
  - Canal dedicado: #música-gaming
  - Auto-desconexión: 15 minutos
  - Calidad de audio: medium
  - Límite de cola: 100 canciones
  - Filtros: Contenido apropiado
  - Roles: @Gamer-DJ para miembros activos
```

### Servidor de Música/Arte
```yaml
Configuración Recomendada:
  - Canal dedicado: #sala-de-música
  - Auto-desconexión: 30 minutos
  - Calidad de audio: high/ultra
  - Límite de cola: 200 canciones
  - Filtros: Mínimos
  - Roles: Múltiples niveles de DJ
```

### Servidor Comunitario
```yaml
Configuración Recomendada:
  - Canal dedicado: #música-general
  - Auto-desconexión: 10 minutos
  - Calidad de audio: medium
  - Límite de cola: 75 canciones
  - Filtros: Contenido familiar
  - Roles: @DJ para miembros de confianza
```

### Servidor de Estudio/Trabajo
```yaml
Configuración Recomendada:
  - Canal dedicado: #música-ambiente
  - Auto-desconexión: 60 minutos
  - Calidad de audio: medium
  - Límite de cola: 50 canciones
  - Filtros: Solo música instrumental/ambiental
  - Roles: Restringido a moderadores
```

## 📊 Monitoreo y Estadísticas

### Configurar Logs
```
/music_logs_setup #canal-logs
```

**Eventos registrados**:
- Canciones reproducidas
- Comandos utilizados
- Errores de conexión
- Cambios de configuración
- Actividad de usuarios

### Dashboard de Estadísticas
```
/stats_dashboard enable
```

Habilita un dashboard que muestra:
- **Uso en tiempo real**
- **Canciones más populares**
- **Usuarios más activos**
- **Horarios de mayor actividad**
- **Estadísticas de rendimiento**

## 🔐 Configuración de Seguridad

### Prevención de Spam
```
/anti_spam_music
```

**Configuraciones**:
- **Límite de comandos por minuto**: 10-20
- **Cooldown entre canciones**: 3-10 segundos
- **Detección de comportamiento sospechoso**: Activado

### Backup de Configuración
```
/config_backup create
```

Crea un respaldo de:
- Configuraciones del servidor
- Playlists del servidor
- Permisos personalizados
- Filtros y restricciones

### Restaurar Configuración
```
/config_restore <archivo_backup>
```

## 🌐 Integraciones Externas

### Spotify Integration
1. **Obtén credenciales de Spotify Developer**
2. **Configura en el bot**:
   ```
   /spotify_setup <client_id> <client_secret>
   ```
3. **Beneficios**:
   - Reproducir playlists completas de Spotify
   - Sincronización con cuentas de usuarios
   - Recomendaciones personalizadas

### Last.fm Integration
```
/lastfm_setup <api_key>
```

**Funciones**:
- Scrobbling automático
- Estadísticas detalladas
- Recomendaciones basadas en historial

### YouTube Music Premium
```
/youtube_premium_setup
```

**Ventajas**:
- Sin anuncios
- Mejor calidad de audio
- Acceso a YouTube Music exclusives

## 🛠️ Solución de Problemas de Configuración

### Problemas Comunes

#### El bot no puede conectarse a canales de voz
**Solución**:
1. Verifica permisos de "Conectar" y "Hablar"
2. Revisa si el canal tiene límite de usuarios
3. Comprueba la región del servidor de voz
4. Usa `/reconnect` para forzar reconexión

#### Comandos no funcionan en ciertos canales
**Solución**:
1. Verifica permisos del bot en el canal
2. Revisa configuración de `/music_channel`
3. Comprueba restricciones por rol
4. Usa `/music_permissions` para revisar configuración

#### Audio de mala calidad o con cortes
**Solución**:
1. Cambia la calidad de audio: `/audio_quality medium`
2. Cambia región del servidor: `/voice_region auto`
3. Verifica conexión a internet del servidor
4. Reduce la carga del bot con `/queue_limits`

#### Configuración se pierde después de reinicio
**Solución**:
1. Crea backup regular: `/config_backup create`
2. Verifica permisos de escritura del bot
3. Contacta soporte si persiste el problema

### Comandos de Diagnóstico

#### `/music_diagnostics`
Ejecuta una verificación completa del sistema:
- Estado de conexión
- Permisos del bot
- Configuración actual
- Rendimiento del servidor
- Problemas detectados

#### `/connection_test`
Prueba la conectividad de audio:
- Latencia de conexión
- Calidad de audio
- Estabilidad de la conexión
- Recomendaciones de optimización

## 📋 Lista de Verificación Post-Configuración

### ✅ Verificaciones Básicas
- [ ] Bot tiene permisos necesarios
- [ ] Rol DJ configurado y asignado
- [ ] Canal de música establecido
- [ ] Auto-desconexión configurada
- [ ] Límites de cola establecidos

### ✅ Verificaciones de Seguridad
- [ ] Filtros de contenido activados
- [ ] Anti-spam configurado
- [ ] Backup de configuración creado
- [ ] Logs habilitados
- [ ] Permisos por rol verificados

### ✅ Verificaciones de Rendimiento
- [ ] Calidad de audio optimizada
- [ ] Región de voz configurada
- [ ] Límites apropiados establecidos
- [ ] Dashboard de estadísticas habilitado
- [ ] Diagnósticos ejecutados sin errores

### ✅ Verificaciones de Usuario
- [ ] Comandos básicos funcionan
- [ ] Playlists se pueden crear
- [ ] Audio se reproduce correctamente
- [ ] Permisos funcionan como esperado
- [ ] Usuarios pueden acceder a funciones apropiadas

## 🎓 Configuración Avanzada para Expertos

### Configuración de Base de Datos
```
/database_config
```
- **Pool de conexiones**: Optimiza para tu tamaño de servidor
- **Cache de canciones**: Mejora velocidad de carga
- **Limpieza automática**: Mantiene la base de datos optimizada

### Configuración de Red
```
/network_config
```
- **Timeout de conexión**: Ajusta según tu red
- **Reintentos automáticos**: Configura para estabilidad
- **Balanceador de carga**: Para servidores muy grandes

### API Rate Limiting
```
/api_limits
```
- **YouTube API**: Gestiona cuotas diarias
- **Spotify API**: Optimiza llamadas
- **SoundCloud API**: Configura límites

---

## 🆘 Soporte de Configuración

¿Necesitas ayuda con la configuración? Tenemos varias opciones:

- **[Guía de Solución de Problemas](/music/troubleshooting)** - Problemas comunes
- **[Comandos de Música](/music/commands)** - Referencia completa
- **[Servidor de Soporte](/support)** - Ayuda personalizada
- **[Documentación de API](https://docs.dark-bot.com/api)** - Para desarrolladores

### Configuración Personalizada
Si necesitas una configuración específica para tu servidor, nuestro equipo puede ayudarte:

- **Consultoría gratuita** para servidores grandes (1000+ miembros)
- **Configuración personalizada** para casos de uso específicos
- **Integración con bots existentes**
- **Migración desde otros bots de música**

---

*¿Tu servidor tiene necesidades especiales? Contáctanos en nuestro [servidor de soporte](/support) y trabajaremos contigo para crear la configuración perfecta.*