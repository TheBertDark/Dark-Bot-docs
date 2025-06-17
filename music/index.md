# 🎵 Sistema de Música - Dark-Bot

## Descripción General

El sistema de música de Dark-Bot te permite reproducir música de alta calidad en tu servidor de Discord. Compatible con múltiples plataformas y diseñado para ofrecer la mejor experiencia de audio.

## 🚀 Características Principales

### Plataformas Soportadas
- **YouTube** - Videos y playlists
- **Spotify** - Canciones y playlists (requiere Premium)
- **SoundCloud** - Tracks y sets
- **Bandcamp** - Álbumes y canciones
- **Twitch** - Streams de audio
- **Archivos Directos** - MP3, FLAC, WAV

### Funcionalidades Avanzadas
- **Cola de Reproducción** - Hasta 100 canciones
- **Playlists Personalizadas** - Guarda tus favoritas
- **Controles de Audio** - Volumen, ecualizador, filtros
- **Modo DJ** - Controles exclusivos para DJs
- **Auto-Play** - Reproducción continua inteligente
- **Letras en Tiempo Real** - Sincronizadas con la música

## 📋 Comandos Básicos

### Reproducción
```
/play <canción/URL>     - Reproduce una canción
/pause                  - Pausa la reproducción
/resume                 - Reanuda la reproducción
/stop                   - Detiene y limpia la cola
/skip                   - Salta a la siguiente canción
/previous               - Vuelve a la canción anterior
```

### Control de Cola
```
/queue                  - Muestra la cola actual
/queue_clear            - Limpia toda la cola
/queue_shuffle          - Mezcla la cola aleatoriamente
/queue_remove <número>  - Elimina una canción específica
/queue_move <de> <a>    - Mueve una canción en la cola
```

### Playlists
```
/playlist_create <nombre>       - Crea una nueva playlist
/playlist_add <nombre> <canción> - Añade canción a playlist
/playlist_play <nombre>         - Reproduce una playlist
/playlist_list                  - Lista tus playlists
/playlist_delete <nombre>       - Elimina una playlist
```

### Controles de Audio
```
/volume <0-100>         - Ajusta el volumen
/bass <-10 a 10>        - Ajusta los graves
/treble <-10 a 10>      - Ajusta los agudos
/equalizer <preset>     - Aplica preset de ecualizador
/filters                - Muestra filtros disponibles
```

## 🎛️ Configuración Avanzada

### Configuración del Servidor
```
/music_setup            - Configuración inicial
/dj_role <@rol>         - Establece rol de DJ
/music_channel <#canal> - Canal dedicado para música
/auto_disconnect <tiempo> - Desconexión automática
```

### Permisos y Roles
- **Administrador**: Control total del sistema
- **DJ**: Controles avanzados (skip, volume, filters)
- **Usuario**: Comandos básicos (play, queue)
- **Invitado**: Solo visualización

## 🎵 Guías de Uso

### Cómo Empezar
1. **Únete a un canal de voz**
2. **Usa `/play <canción>`** para empezar
3. **Añade más canciones** con `/play` adicionales
4. **Controla la reproducción** con los comandos básicos

### Crear tu Primera Playlist
1. **Crea la playlist**: `/playlist_create MiPlaylist`
2. **Añade canciones**: `/playlist_add MiPlaylist Bohemian Rhapsody`
3. **Reproduce**: `/playlist_play MiPlaylist`

### Configurar Modo DJ
1. **Crea un rol DJ**: En configuración del servidor
2. **Configura el rol**: `/dj_role @DJ`
3. **Asigna permisos**: Los DJs pueden controlar la música

## 🔧 Solución de Problemas

### Problemas Comunes

#### El bot no se conecta al canal de voz
- **Verifica permisos**: El bot necesita "Conectar" y "Hablar"
- **Revisa el canal**: Asegúrate de que no esté lleno
- **Reinicia conexión**: `/disconnect` y luego `/play`

#### La música se corta o tiene lag
- **Verifica tu conexión**: Velocidad de internet estable
- **Cambia región**: `/region` para cambiar servidor de voz
- **Reduce calidad**: `/quality low` temporalmente

#### No encuentra la canción
- **Usa términos específicos**: "Artista - Canción"
- **Prueba con URL directa**: Copia el enlace de YouTube/Spotify
- **Verifica disponibilidad**: Algunas canciones tienen restricciones regionales

#### Comandos no responden
- **Verifica permisos**: El bot necesita permisos de slash commands
- **Revisa el rol**: Tu rol debe tener permisos de música
- **Contacta soporte**: Si persiste el problema

### Códigos de Error

| Código | Descripción | Solución |
|--------|-------------|----------|
| MUS001 | No conectado a canal de voz | Únete a un canal primero |
| MUS002 | Sin permisos en el canal | Verifica permisos del bot |
| MUS003 | Canción no encontrada | Usa términos más específicos |
| MUS004 | Playlist no existe | Verifica el nombre de la playlist |
| MUS005 | Cola llena | Elimina canciones o espera |
| MUS006 | Formato no soportado | Usa formatos compatibles |

## 🎼 Características Premium

### Spotify Integration
- **Playlists completas** de Spotify
- **Recomendaciones personalizadas**
- **Sincronización de favoritos**
- **Calidad de audio mejorada**

### Funciones Avanzadas
- **Ecualizador de 10 bandas**
- **Efectos de audio profesionales**
- **Grabación de sesiones**
- **Estadísticas detalladas de uso**

### Límites Aumentados
- **Cola de 500 canciones**
- **50 playlists personalizadas**
- **Historial de 1000 canciones**
- **Prioridad en servidores**

## 📊 Estadísticas y Métricas

### Comandos de Estadísticas
```
/music_stats            - Estadísticas del servidor
/my_stats               - Tus estadísticas personales
/top_songs              - Canciones más reproducidas
/listening_time         - Tiempo total de escucha
```

### Métricas Disponibles
- **Canciones reproducidas**
- **Tiempo total de escucha**
- **Géneros favoritos**
- **Artistas más escuchados**
- **Horarios de mayor actividad**

## 🔗 Integraciones

### Discord Rich Presence
- **Muestra la canción actual** en tu estado
- **Información del artista y álbum**
- **Tiempo de reproducción**
- **Botones de control rápido**

### Webhooks y API
- **Notificaciones de nuevas canciones**
- **Integración con bots de terceros**
- **Exportación de playlists**
- **Sincronización con servicios externos**

## 🎯 Consejos y Trucos

### Optimización de Rendimiento
- **Usa playlists** en lugar de añadir canciones una por una
- **Configura auto-disconnect** para ahorrar recursos
- **Limpia la cola regularmente** para mejor rendimiento

### Mejores Prácticas
- **Crea roles específicos** para diferentes niveles de control
- **Usa canales dedicados** para comandos de música
- **Configura filtros de contenido** apropiados para tu servidor

### Comandos Útiles para Administradores
```
/music_logs             - Logs de actividad musical
/music_backup           - Respalda configuración
/music_restore          - Restaura configuración
/music_reset            - Reinicia configuración
```

## 🆕 Actualizaciones Recientes

### Versión 3.2.1
- **Nuevo algoritmo de búsqueda** más preciso
- **Soporte para YouTube Shorts**
- **Mejoras en calidad de audio**
- **Corrección de bugs en playlists**

### Próximas Características
- **Karaoke Mode** con letras sincronizadas
- **Collaborative Playlists** para múltiples usuarios
- **AI Music Recommendations** basadas en preferencias
- **Live Concert Streaming** para eventos especiales

## 📞 Soporte

¿Necesitas ayuda con el sistema de música? Tenemos varias opciones:

- **[Guía de Comandos](/music/commands)** - Lista completa de comandos
- **[Configuración Avanzada](/music/setup)** - Guía de configuración detallada
- **[Solución de Problemas](/music/troubleshooting)** - Problemas comunes y soluciones
- **[Servidor de Soporte](/support)** - Ayuda en tiempo real

---

*¿Quieres contribuir al desarrollo del sistema de música? Únete a nuestro [servidor de desarrollo](https://discord.gg/tu-servidor) y comparte tus ideas.*