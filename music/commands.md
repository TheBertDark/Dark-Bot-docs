# 🎵 Comandos de Música - Dark-Bot

## 📋 Lista Completa de Comandos

### 🎶 Reproducción Básica

#### `/play <búsqueda/URL>`
**Descripción**: Reproduce una canción o la añade a la cola
**Permisos**: Usuario
**Ejemplos**:
```
/play Bohemian Rhapsody
/play https://www.youtube.com/watch?v=fJ9rUzIMcZQ
/play Queen - We Will Rock You
```
**Plataformas soportadas**: YouTube, Spotify, SoundCloud, Bandcamp

#### `/pause`
**Descripción**: Pausa la reproducción actual
**Permisos**: DJ/Usuario que añadió la canción
**Nota**: La canción se puede reanudar con `/resume`

#### `/resume`
**Descripción**: Reanuda la reproducción pausada
**Permisos**: DJ/Usuario que pausó
**Alias**: `/unpause`

#### `/stop`
**Descripción**: Detiene la reproducción y limpia la cola
**Permisos**: DJ/Administrador
**Advertencia**: Esta acción no se puede deshacer

#### `/skip [cantidad]`
**Descripción**: Salta a la siguiente canción o múltiples canciones
**Permisos**: DJ/Usuario (con votación)
**Ejemplos**:
```
/skip           # Salta 1 canción
/skip 3         # Salta 3 canciones
```
**Nota**: Los usuarios normales necesitan votos para saltar

#### `/previous`
**Descripción**: Vuelve a la canción anterior
**Permisos**: DJ
**Limitación**: Solo funciona si hay historial disponible

### 📝 Gestión de Cola

#### `/queue [página]`
**Descripción**: Muestra la cola de reproducción actual
**Permisos**: Usuario
**Ejemplos**:
```
/queue          # Página 1
/queue 2        # Página 2
```
**Información mostrada**: Posición, título, duración, usuario que añadió

#### `/queue_clear`
**Descripción**: Limpia toda la cola de reproducción
**Permisos**: DJ/Administrador
**Confirmación**: Requiere confirmación para evitar accidentes

#### `/queue_shuffle`
**Descripción**: Mezcla aleatoriamente la cola actual
**Permisos**: DJ
**Nota**: La canción actual no se ve afectada

#### `/queue_remove <posición>`
**Descripción**: Elimina una canción específica de la cola
**Permisos**: DJ/Usuario que añadió la canción
**Ejemplos**:
```
/queue_remove 3     # Elimina la canción en posición 3
```

#### `/queue_move <desde> <hacia>`
**Descripción**: Mueve una canción a otra posición en la cola
**Permisos**: DJ
**Ejemplos**:
```
/queue_move 5 2     # Mueve canción de posición 5 a 2
```

#### `/queue_loop [modo]`
**Descripción**: Configura el modo de repetición
**Permisos**: DJ
**Modos disponibles**:
- `off` - Sin repetición
- `song` - Repite canción actual
- `queue` - Repite toda la cola
**Ejemplo**: `/queue_loop song`

### 🎵 Playlists

#### `/playlist_create <nombre>`
**Descripción**: Crea una nueva playlist personal
**Permisos**: Usuario
**Límites**: 10 playlists por usuario (20 con Premium)
**Ejemplo**: `/playlist_create Mi Música Favorita`

#### `/playlist_list [usuario]`
**Descripción**: Lista las playlists disponibles
**Permisos**: Usuario
**Ejemplos**:
```
/playlist_list              # Tus playlists
/playlist_list @usuario     # Playlists públicas de otro usuario
```

#### `/playlist_info <nombre>`
**Descripción**: Muestra información detallada de una playlist
**Permisos**: Usuario
**Información**: Canciones, duración total, creador, fecha de creación

#### `/playlist_play <nombre>`
**Descripción**: Reproduce una playlist completa
**Permisos**: Usuario
**Opciones**: Puede reproducir en orden o aleatorio
**Ejemplo**: `/playlist_play Rock Clásico`

#### `/playlist_add <playlist> <canción/URL>`
**Descripción**: Añade una canción a una playlist
**Permisos**: Propietario de la playlist
**Límites**: 100 canciones por playlist (500 con Premium)
**Ejemplo**: `/playlist_add "Mi Playlist" Stairway to Heaven`

#### `/playlist_remove <playlist> <posición>`
**Descripción**: Elimina una canción de la playlist
**Permisos**: Propietario de la playlist
**Ejemplo**: `/playlist_remove "Mi Playlist" 5`

#### `/playlist_delete <nombre>`
**Descripción**: Elimina una playlist permanentemente
**Permisos**: Propietario de la playlist
**Confirmación**: Requiere confirmación

#### `/playlist_share <nombre> [público]`
**Descripción**: Comparte una playlist o cambia su visibilidad
**Permisos**: Propietario de la playlist
**Opciones**: `true` para público, `false` para privado

### 🔊 Control de Audio

#### `/volume <0-100>`
**Descripción**: Ajusta el volumen de reproducción
**Permisos**: DJ
**Rango**: 0 (silencio) a 100 (máximo)
**Ejemplo**: `/volume 75`

#### `/bass <-10 a 10>`
**Descripción**: Ajusta el nivel de graves
**Permisos**: DJ
**Rango**: -10 (mínimo) a 10 (máximo)
**Ejemplo**: `/bass 3`

#### `/treble <-10 a 10>`
**Descripción**: Ajusta el nivel de agudos
**Permisos**: DJ
**Rango**: -10 (mínimo) a 10 (máximo)
**Ejemplo**: `/treble -2`

#### `/equalizer <preset>`
**Descripción**: Aplica un preset de ecualizador
**Permisos**: DJ
**Presets disponibles**:
- `flat` - Sin modificaciones
- `rock` - Optimizado para rock
- `pop` - Optimizado para pop
- `jazz` - Optimizado para jazz
- `classical` - Optimizado para música clásica
- `electronic` - Optimizado para electrónica
- `bass_boost` - Realza graves
- `vocal` - Realza voces

#### `/filters`
**Descripción**: Muestra y gestiona filtros de audio
**Permisos**: DJ
**Filtros disponibles**:
- `nightcore` - Acelera y agudiza
- `vaporwave` - Ralentiza y suaviza
- `8d` - Efecto de audio 8D
- `karaoke` - Reduce voces principales
- `tremolo` - Efecto de vibrato
- `distortion` - Distorsión controlada

#### `/speed <0.5-2.0>`
**Descripción**: Cambia la velocidad de reproducción
**Permisos**: DJ
**Rango**: 0.5x (lento) a 2.0x (rápido)
**Ejemplo**: `/speed 1.25`

### 🎤 Funciones Especiales

#### `/lyrics [canción]`
**Descripción**: Muestra las letras de la canción
**Permisos**: Usuario
**Ejemplos**:
```
/lyrics                     # Canción actual
/lyrics Bohemian Rhapsody   # Canción específica
```

#### `/nowplaying`
**Descripción**: Muestra información de la canción actual
**Permisos**: Usuario
**Información**: Título, artista, duración, progreso, usuario que la añadió
**Alias**: `/np`

#### `/search <término>`
**Descripción**: Busca canciones sin reproducir inmediatamente
**Permisos**: Usuario
**Resultado**: Lista de opciones para elegir
**Ejemplo**: `/search Queen greatest hits`

#### `/history [cantidad]`
**Descripción**: Muestra el historial de canciones reproducidas
**Permisos**: Usuario
**Límite**: Últimas 50 canciones
**Ejemplo**: `/history 10`

#### `/shuffle_play <término>`
**Descripción**: Busca y reproduce aleatoriamente
**Permisos**: Usuario
**Útil para**: Descubrir música nueva
**Ejemplo**: `/shuffle_play rock 80s`

### 🔧 Configuración y Administración

#### `/music_setup`
**Descripción**: Configuración inicial del sistema de música
**Permisos**: Administrador
**Configura**: Canal de música, rol DJ, permisos básicos

#### `/dj_role <@rol>`
**Descripción**: Establece el rol de DJ del servidor
**Permisos**: Administrador
**Ejemplo**: `/dj_role @DJ`

#### `/music_channel <#canal>`
**Descripción**: Establece canal dedicado para comandos de música
**Permisos**: Administrador
**Efecto**: Solo funciona en el canal especificado

#### `/auto_disconnect <minutos>`
**Descripción**: Configura desconexión automática por inactividad
**Permisos**: Administrador
**Rango**: 1-60 minutos
**Ejemplo**: `/auto_disconnect 10`

#### `/music_permissions`
**Descripción**: Configura permisos detallados de música
**Permisos**: Administrador
**Opciones**: Por rol, por usuario, por canal

### 📊 Estadísticas y Información

#### `/music_stats`
**Descripción**: Estadísticas del servidor
**Permisos**: Usuario
**Información**: Canciones reproducidas, tiempo total, top usuarios

#### `/my_music_stats`
**Descripción**: Tus estadísticas personales
**Permisos**: Usuario
**Información**: Canciones añadidas, tiempo escuchado, géneros favoritos

#### `/top_songs [período]`
**Descripción**: Canciones más reproducidas
**Permisos**: Usuario
**Períodos**: `day`, `week`, `month`, `all`
**Ejemplo**: `/top_songs week`

#### `/top_users [período]`
**Descripción**: Usuarios más activos en música
**Permisos**: Usuario
**Períodos**: `day`, `week`, `month`, `all`

### 🔗 Conexión y Control

#### `/join [canal]`
**Descripción**: Conecta el bot a un canal de voz
**Permisos**: Usuario
**Ejemplos**:
```
/join              # Tu canal actual
/join General      # Canal específico
```

#### `/disconnect`
**Descripción**: Desconecta el bot del canal de voz
**Permisos**: DJ/Administrador
**Efecto**: Limpia la cola y detiene reproducción
**Alias**: `/leave`

#### `/reconnect`
**Descripción**: Reconecta el bot (útil para problemas de audio)
**Permisos**: DJ
**Mantiene**: Cola actual y configuración

#### `/move <#canal>`
**Descripción**: Mueve el bot a otro canal de voz
**Permisos**: DJ
**Ejemplo**: `/move #Música`

### 🎯 Comandos Avanzados (Premium)

#### `/radio <estación>`
**Descripción**: Reproduce estaciones de radio online
**Permisos**: Usuario Premium
**Estaciones**: Rock, Pop, Jazz, Classical, Electronic

#### `/record [duración]`
**Descripción**: Graba la sesión de música actual
**Permisos**: DJ Premium
**Formato**: MP3 de alta calidad
**Límite**: 60 minutos

#### `/crossfade <segundos>`
**Descripción**: Configura transición suave entre canciones
**Permisos**: DJ Premium
**Rango**: 0-10 segundos

#### `/queue_import <archivo>`
**Descripción**: Importa cola desde archivo
**Permisos**: DJ Premium
**Formatos**: JSON, M3U, PLS

#### `/queue_export`
**Descripción**: Exporta cola actual
**Permisos**: Usuario Premium
**Formato**: Archivo descargable

## 🎮 Atajos y Aliases

| Comando Completo | Alias | Descripción |
|------------------|-------|-------------|
| `/play` | `/p` | Reproducir |
| `/skip` | `/s` | Saltar |
| `/queue` | `/q` | Ver cola |
| `/nowplaying` | `/np` | Canción actual |
| `/disconnect` | `/leave`, `/dc` | Desconectar |
| `/volume` | `/vol`, `/v` | Volumen |
| `/playlist_play` | `/pl` | Reproducir playlist |

## 🔐 Niveles de Permisos

### 👤 Usuario Básico
- Reproducir canciones
- Ver cola y estadísticas
- Crear playlists personales
- Votar para saltar canciones

### 🎧 DJ
- Todos los permisos de usuario
- Control total de reproducción
- Gestión de cola
- Configuración de audio
- Saltar sin votación

### 👑 Administrador
- Todos los permisos de DJ
- Configuración del sistema
- Gestión de permisos
- Acceso a logs y estadísticas avanzadas

### 💎 Premium
- Todos los permisos anteriores
- Funciones avanzadas
- Límites aumentados
- Prioridad en servidores

## 📱 Comandos de Contexto

Algunos comandos también están disponibles como **comandos de contexto** (clic derecho):

- **Añadir a Cola**: Clic derecho en mensaje con enlace
- **Información de Usuario**: Ver estadísticas musicales
- **Crear Playlist**: Desde mensaje con múltiples canciones

## 🆘 Comandos de Emergencia

#### `/music_reset`
**Descripción**: Reinicia completamente el sistema de música
**Permisos**: Administrador
**Uso**: Solo en caso de problemas graves
**Advertencia**: Elimina toda la configuración

#### `/force_disconnect`
**Descripción**: Fuerza desconexión del bot
**Permisos**: Administrador
**Uso**: Cuando el bot no responde normalmente

---

## 💡 Consejos de Uso

### Para Usuarios Nuevos
1. **Empieza con `/play`** - Es el comando más básico
2. **Usa `/help music`** - Para ayuda contextual
3. **Crea una playlist** - Para tus canciones favoritas
4. **Aprende los atajos** - Ahorra tiempo escribiendo

### Para DJs
1. **Configura el ecualizador** - Mejora la experiencia de audio
2. **Usa `/queue_shuffle`** - Mantén la música variada
3. **Monitorea `/music_stats`** - Conoce las preferencias del servidor
4. **Aprende los filtros** - Crea ambientes únicos

### Para Administradores
1. **Configura roles apropiados** - Control granular de permisos
2. **Establece un canal dedicado** - Organiza mejor los comandos
3. **Revisa logs regularmente** - Mantén el sistema optimizado
4. **Considera Premium** - Para funciones avanzadas

---

**¿Necesitas ayuda con algún comando específico?** Usa `/help <comando>` para obtener información detallada, o visita nuestro [servidor de soporte](/support) para asistencia personalizada.