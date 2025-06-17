# 🎵 Comandos de Música

Esta sección detalla el sistema completo de música del bot, incluyendo reproducción, gestión de colas, controles avanzados y funciones especiales para una experiencia musical óptima.

---

## /play

**Descripción:** Reproduce música desde YouTube, Spotify o SoundCloud.
**Permisos requeridos:** Ninguno
**Requisitos:** Estar en un canal de voz

**Sintaxis:**
```
/play consulta:<búsqueda o URL>
```

**Parámetros:**
- `consulta` (String, requerido): Término de búsqueda, URL de YouTube, Spotify o SoundCloud

### Tipos de Búsqueda Soportados

**Búsqueda por texto:**
```
# Búsqueda simple
/play consulta:Imagine Dragons Believer

# Búsqueda específica con artista
/play consulta:The Weeknd Blinding Lights

# Búsqueda de género
/play consulta:lofi hip hop chill

# Búsqueda en otro idioma
/play consulta:BTS Dynamite
```

**URLs de YouTube:**
```
# Video individual
/play consulta:https://www.youtube.com/watch?v=dQw4w9WgXcQ

# Video con timestamp
/play consulta:https://www.youtube.com/watch?v=dQw4w9WgXcQ&t=30s

# Playlist completa
/play consulta:https://www.youtube.com/playlist?list=PLrAl6rYgs4IvGFBDEaVGFXp6_SYiUyuiX

# Video de livestream
/play consulta:https://www.youtube.com/watch?v=jfKfPfyJRdk
```

**URLs de Spotify:**
```
# Canción individual
/play consulta:https://open.spotify.com/track/4iV5W9uYEdYUVa79Axb7Rh

# Álbum completo
/play consulta:https://open.spotify.com/album/1DFixLWuPkv3KT3TnV35m3

# Playlist
/play consulta:https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M

# Artista (top tracks)
/play consulta:https://open.spotify.com/artist/1Xyo4u8uXC1ZmMpatF05PJ
```

**URLs de SoundCloud:**
```
# Track individual
/play consulta:https://soundcloud.com/artist/track-name

# Playlist
/play consulta:https://soundcloud.com/artist/sets/playlist-name

# Usuario (tracks populares)
/play consulta:https://soundcloud.com/username
```

### Casos de Uso Completos

**Sesión de música variada:**
```
# Empezar con un hit popular
/play consulta:Dua Lipa Levitating

# Añadir algo de rock
/play consulta:Queen Bohemian Rhapsody

# Música electrónica
/play consulta:Avicii Wake Me Up

# Algo relajante
/play consulta:Billie Eilish lovely
```

**Sesión temática de gaming:**
```
# Música épica
/play consulta:Two Steps From Hell Heart of Courage

# Soundtracks de juegos
/play consulta:Genshin Impact soundtrack

# Música electrónica energética
/play consulta:TheFatRat Unity

# Lo-fi para concentrarse
/play consulta:lofi hip hop study beats
```

**Fiesta o evento:**
```
# Hits actuales
/play consulta:top hits 2024

# Clásicos de fiesta
/play consulta:party music playlist

# Reggaeton
/play consulta:Bad Bunny Un Verano Sin Ti

# Pop internacional
/play consulta:Dua Lipa Future Nostalgia
```

---

## /queue

**Descripción:** Muestra la cola de reproducción actual con información detallada.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/queue [página:<número>]
```

**Parámetros:**
- `página` (Entero, opcional): Página de la cola a mostrar (por defecto: 1)

**Ejemplos:**
```
# Ver primera página de la cola
/queue

# Ver página específica
/queue página:2

# Navegar por cola larga
/queue página:5
```

### Información Mostrada

**Para cada canción:**
- Posición en la cola
- Título y artista
- Duración
- Usuario que la añadió
- Fuente (YouTube, Spotify, SoundCloud)

**Información general:**
- Canción actual reproduciendo
- Total de canciones en cola
- Tiempo total de reproducción
- Estado del reproductor

### Casos de Uso

**Verificar próximas canciones:**
```
/queue
# "¿Qué viene después?"
```

**Planificar añadir más música:**
```
/queue página:3
# "Veo que la cola está corta, voy a añadir más"
```

**Verificar contribuciones:**
```
/queue
# "¿Quién añadió qué canciones?"
```

---

## /skip

**Descripción:** Salta la canción actual o múltiples canciones.
**Permisos requeridos:** Ninguno (con votación) / Gestionar Canales (directo)

**Sintaxis:**
```
/skip [cantidad:<número>]
```

**Parámetros:**
- `cantidad` (Entero, opcional): Número de canciones a saltar (por defecto: 1)

**Ejemplos:**
```
# Saltar canción actual
/skip

# Saltar 3 canciones
/skip cantidad:3

# Saltar 5 canciones
/skip cantidad:5
```

### Sistema de Votación

**Votación automática:**
- Se requiere 50% + 1 de votos de usuarios en el canal
- Mínimo 2 usuarios para iniciar votación
- Los moderadores pueden saltar directamente

**Proceso de votación:**
```
# Usuario 1 inicia votación
/skip
# Bot: "🗳️ Votación iniciada: 1/3 votos necesarios"

# Usuario 2 vota
/skip
# Bot: "🗳️ Votación: 2/3 votos necesarios"

# Usuario 3 vota
/skip
# Bot: "✅ Votación exitosa! Saltando canción..."
```

### Casos de Uso

**Canción no deseada:**
```
/skip
# "Esta canción no me gusta"
```

**Limpiar cola rápidamente:**
```
/skip cantidad:10
# "Estas canciones ya no van con el ambiente"
```

**Llegar a canción específica:**
```
/queue  # Ver posición de canción deseada
/skip cantidad:5  # Saltar hasta llegar a ella
```

---

## /pause y /resume

### /pause
**Descripción:** Pausa la reproducción actual.
**Permisos requeridos:** Ninguno (con votación) / Gestionar Canales (directo)

**Sintaxis:**
```
/pause
```

### /resume
**Descripción:** Reanuda la reproducción pausada.
**Permisos requeridos:** Ninguno (con votación) / Gestionar Canales (directo)

**Sintaxis:**
```
/resume
```

### Casos de Uso

**Interrupciones temporales:**
```
# Pausa para hablar
/pause
# [conversación]
/resume
```

**Esperar a más gente:**
```
/pause
# "Esperemos a que lleguen más personas"
# [esperando]
/resume
```

**Emergencias:**
```
/pause
# "Momento, tengo que atender algo urgente"
```

---

## /stop

**Descripción:** Detiene completamente la reproducción y limpia la cola.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/stop
```

**Efectos:**
- Detiene la canción actual
- Limpia toda la cola
- Desconecta el bot del canal de voz
- Resetea el estado del reproductor

### Casos de Uso

**Finalizar sesión musical:**
```
/stop
# "Ya terminamos por hoy"
```

**Emergencia o problema:**
```
/stop
# "El bot está bugueado, mejor lo reiniciamos"
```

**Cambio de actividad:**
```
/stop
# "Vamos a hacer otra cosa, paremos la música"
```

---

## /volume

**Descripción:** Ajusta el volumen de reproducción.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/volume nivel:<número>
```

**Parámetros:**
- `nivel` (Entero, requerido): Nivel de volumen (1-100)

**Ejemplos:**
```
# Volumen bajo para conversación
/volume nivel:30

# Volumen medio estándar
/volume nivel:50

# Volumen alto para fiesta
/volume nivel:80

# Volumen máximo
/volume nivel:100

# Volumen mínimo
/volume nivel:1
```

### Niveles Recomendados

**Por situación:**
```
# Música de fondo mientras se habla
/volume nivel:25

# Escucha casual
/volume nivel:50

# Sesión musical dedicada
/volume nivel:70

# Fiesta o evento
/volume nivel:85

# Presentaciones o shows
/volume nivel:95
```

### Casos de Uso

**Ajuste dinámico:**
```
# Al empezar conversación
/volume nivel:30

# Al terminar conversación
/volume nivel:60
```

**Diferentes tipos de música:**
```
# Para música clásica o instrumental
/volume nivel:45

# Para rock o electrónica
/volume nivel:75
```

---

## /shuffle

**Descripción:** Mezcla aleatoriamente el orden de la cola.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/shuffle
```

**Efectos:**
- Reorganiza aleatoriamente todas las canciones en cola
- No afecta la canción actualmente reproduciéndose
- Mantiene la información de quién añadió cada canción

### Casos de Uso

**Variedad en playlist larga:**
```
/shuffle
# "Mezclemos la cola para más variedad"
```

**Sorpresa musical:**
```
/shuffle
# "A ver qué sorpresas nos da el shuffle"
```

**Evitar monotonía:**
```
/shuffle
# "Todas las canciones de rock están juntas, mejor las mezclamos"
```

---

## /loop

**Descripción:** Configura el modo de repetición.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/loop modo:<opción>
```

**Parámetros:**
- `modo` (String, requerido): Opciones disponibles:
  - `off` - Sin repetición
  - `track` - Repetir canción actual
  - `queue` - Repetir toda la cola

**Ejemplos:**
```
# Desactivar repetición
/loop modo:off

# Repetir canción actual
/loop modo:track

# Repetir toda la cola
/loop modo:queue
```

### Casos de Uso por Modo

**Loop de canción (`track`):**
```
/loop modo:track
# "Esta canción está increíble, vamos a repetirla"
# Útil para: canciones favoritas, estudiar con una canción, análisis musical
```

**Loop de cola (`queue`):**
```
/loop modo:queue
# "Esta playlist está perfecta, que se repita"
# Útil para: fiestas, música de fondo continua, playlists curadas
```

**Sin loop (`off`):**
```
/loop modo:off
# "Ya no queremos repetir, sigamos con música nueva"
# Útil para: explorar música nueva, sesiones variadas
```

---

## /nowplaying

**Descripción:** Muestra información detallada de la canción actual.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/nowplaying
```

### Información Mostrada

**Detalles de la canción:**
- Título y artista
- Duración total
- Tiempo transcurrido
- Progreso visual (barra)
- Fuente (YouTube, Spotify, SoundCloud)
- Thumbnail/imagen

**Estado del reproductor:**
- Volumen actual
- Modo de loop activo
- Usuario que añadió la canción
- Posición en cola original

**Controles disponibles:**
- Botones de reacción para:
  - ⏯️ Pausar/Reanudar
  - ⏭️ Saltar
  - 🔀 Shuffle
  - 🔁 Loop
  - ⏹️ Stop

### Casos de Uso

**Identificar canción:**
```
/nowplaying
# "¿Cómo se llama esta canción?"
```

**Verificar progreso:**
```
/nowplaying
# "¿Cuánto falta para que termine?"
```

**Acceso rápido a controles:**
```
/nowplaying
# Usar botones de reacción para controlar
```

---

## /seek

**Descripción:** Salta a un momento específico de la canción actual.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/seek tiempo:<timestamp>
```

**Parámetros:**
- `tiempo` (String, requerido): Tiempo en formato MM:SS o HH:MM:SS

**Ejemplos:**
```
# Saltar al minuto 2:30
/seek tiempo:2:30

# Saltar al inicio
/seek tiempo:0:00

# Saltar a 1 hora 15 minutos 30 segundos
/seek tiempo:1:15:30

# Saltar cerca del final
/seek tiempo:3:45
```

### Casos de Uso

**Saltar intro larga:**
```
/seek tiempo:0:45
# "Esta intro es muy larga"
```

**Ir a la parte favorita:**
```
/seek tiempo:2:15
# "El mejor drop está en 2:15"
```

**Repetir sección específica:**
```
/seek tiempo:1:30
# "Quiero escuchar ese verso otra vez"
```

**Saltar a outro/final:**
```
/seek tiempo:4:20
# "Vamos directo al final épico"
```

---

## /remove

**Descripción:** Remueve canciones específicas de la cola.
**Permisos requeridos:** Gestionar Canales (o ser quien añadió la canción)

**Sintaxis:**
```
/remove posición:<número>
```

**Parámetros:**
- `posición` (Entero, requerido): Posición de la canción en la cola (usar `/queue` para ver)

**Ejemplos:**
```
# Remover canción en posición 3
/remove posición:3

# Remover la siguiente canción
/remove posición:1

# Remover canción específica
/queue  # Ver posiciones
/remove posición:7
```

### Casos de Uso

**Canción duplicada:**
```
/queue  # Ver que hay duplicados
/remove posición:5  # Remover el duplicado
```

**Canción inapropiada:**
```
/remove posición:2
# "Esa canción no va con el ambiente"
```

**Reorganizar cola:**
```
/remove posición:8  # Remover canción
/play consulta:mejor canción  # Añadir reemplazo
```

---

## /clear

**Descripción:** Limpia toda la cola de reproducción.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/clear
```

**Efectos:**
- Remueve todas las canciones de la cola
- No afecta la canción actualmente reproduciéndose
- No desconecta el bot del canal

### Casos de Uso

**Cambio radical de música:**
```
/clear
# "Cambiemos completamente el tipo de música"
/play consulta:nueva playlist
```

**Limpiar cola saturada:**
```
/clear
# "Hay demasiadas canciones, empecemos de nuevo"
```

**Preparar para evento:**
```
/clear
# "Vamos a preparar música específica para el evento"
```

---

## /lyrics

**Descripción:** Busca y muestra las letras de una canción.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/lyrics [canción:<búsqueda>]
```

**Parámetros:**
- `canción` (String, opcional): Búsqueda específica (si no se proporciona, usa la canción actual)

**Ejemplos:**
```
# Letras de la canción actual
/lyrics

# Buscar letras específicas
/lyrics canción:Imagine Dragons Believer

# Buscar con artista específico
/lyrics canción:The Weeknd Blinding Lights

# Buscar canción en español
/lyrics canción:Jesse y Joy Corre
```

### Casos de Uso

**Cantar junto:**
```
/lyrics
# "¿Cuál era la letra de esta parte?"
```

**Entender la canción:**
```
/lyrics canción:Bohemian Rhapsody
# "Quiero entender qué dice esta canción"
```

**Karaoke:**
```
/lyrics
# "Vamos a hacer karaoke con esta canción"
```

**Análisis de letra:**
```
/lyrics canción:Hotel California
# "Analicemos el significado de esta letra"
```

---

## /join y /leave

### /join
**Descripción:** Hace que el bot se una a tu canal de voz.
**Permisos requeridos:** Ninguno
**Requisitos:** Estar en un canal de voz

**Sintaxis:**
```
/join
```

### /leave
**Descripción:** Hace que el bot abandone el canal de voz.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/leave
```

### Casos de Uso

**Preparar para música:**
```
/join
# "Que se una el bot antes de poner música"
```

**Cambiar de canal:**
```
/leave
# [cambiar a otro canal de voz]
/join
```

**Finalizar sesión:**
```
/leave
# "Ya terminamos, que se vaya el bot"
```

---

## /autoplay

**Descripción:** Activa/desactiva la reproducción automática de música relacionada.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/autoplay estado:<on/off>
```

**Parámetros:**
- `estado` (String, requerido): `on` para activar, `off` para desactivar

**Ejemplos:**
```
# Activar autoplay
/autoplay estado:on

# Desactivar autoplay
/autoplay estado:off
```

### Funcionamiento

**Cuando está activado:**
- Al terminar la cola, añade automáticamente música relacionada
- Usa la última canción reproducida como referencia
- Mantiene el flujo musical continuo
- Añade canciones similares en género y estilo

### Casos de Uso

**Música continua:**
```
/autoplay estado:on
# "Que siga sonando música aunque se acabe la cola"
```

**Descubrir música nueva:**
```
/autoplay estado:on
# "A ver qué música nueva nos recomienda"
```

**Control total de la cola:**
```
/autoplay estado:off
# "Solo quiero escuchar lo que está en cola"
```

---

## /filters

**Descripción:** Aplica filtros de audio a la reproducción.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/filters tipo:<filtro>
```

**Filtros disponibles:**
- `clear` - Quitar todos los filtros
- `bassboost` - Realzar graves
- `nightcore` - Acelerar y agudizar
- `vaporwave` - Ralentizar y suavizar
- `8d` - Efecto de audio 8D
- `karaoke` - Reducir voces
- `tremolo` - Efecto de vibración
- `vibrato` - Modulación de frecuencia

**Ejemplos:**
```
# Quitar filtros
/filters tipo:clear

# Realzar graves
/filters tipo:bassboost

# Efecto nightcore
/filters tipo:nightcore

# Efecto vaporwave
/filters tipo:vaporwave

# Audio 8D
/filters tipo:8d

# Modo karaoke
/filters tipo:karaoke
```

### Casos de Uso por Filtro

**Bassboost:**
```
/filters tipo:bassboost
# Para: EDM, hip-hop, música con mucho bajo
# "Esta canción necesita más graves"
```

**Nightcore:**
```
/filters tipo:nightcore
# Para: anime music, energizar canciones lentas
# "Hagamos esta canción más energética"
```

**Vaporwave:**
```
/filters tipo:vaporwave
# Para: música chill, ambiente relajado
# "Pongamos un ambiente más relajado"
```

**8D:**
```
/filters tipo:8d
# Para: experiencia inmersiva
# "Probemos el efecto 8D con audífonos"
```

**Karaoke:**
```
/filters tipo:karaoke
# Para: cantar junto, reducir voces
# "Vamos a hacer karaoke"
```

**Clear:**
```
/filters tipo:clear
# "Ya no queremos filtros, audio original"
```

---

## Flujos de Trabajo Completos

### Sesión Musical Básica

```
# 1. Unirse al canal
/join

# 2. Empezar con música
/play consulta:música relajante

# 3. Ajustar volumen
/volume nivel:50

# 4. Añadir más canciones
/play consulta:Billie Eilish
/play consulta:The Weeknd

# 5. Ver la cola
/queue

# 6. Controlar reproducción según necesidad
/pause  # si necesario
/resume  # cuando esté listo
/skip  # si no gusta una canción
```

### Fiesta o Evento

```
# 1. Preparación
/join
/volume nivel:80
/autoplay estado:on

# 2. Música de fiesta
/play consulta:party hits 2024
/play consulta:reggaeton mix
/play consulta:pop dance music

# 3. Configurar para variedad
/shuffle
/loop modo:queue

# 4. Gestión durante la fiesta
/nowplaying  # verificar qué suena
/skip  # si la canción no funciona
/filters tipo:bassboost  # para más energía
```

### Sesión de Estudio/Trabajo

```
# 1. Configuración tranquila
/join
/volume nivel:30
/autoplay estado:on

# 2. Música apropiada
/play consulta:lofi hip hop study
/play consulta:instrumental focus music
/play consulta:ambient study playlist

# 3. Configurar para continuidad
/loop modo:queue
/filters tipo:clear  # sin filtros que distraigan

# 4. Control mínimo
# Dejar que fluya automáticamente
```

### Karaoke Night

```
# 1. Preparación
/join
/volume nivel:70
/filters tipo:karaoke

# 2. Canciones populares para cantar
/play consulta:Queen Bohemian Rhapsody
/play consulta:Journey Don't Stop Believin
/play consulta:Bon Jovi Livin on a Prayer

# 3. Herramientas útiles
/lyrics  # para cada canción
/seek tiempo:0:30  # saltar intros largas
/pause  # entre participantes
```

### Descubrimiento Musical

```
# 1. Configuración exploratoria
/join
/volume nivel:60
/autoplay estado:on

# 2. Empezar con algo conocido
/play consulta:artista que me gusta

# 3. Dejar que autoplay sugiera
# El bot añadirá música relacionada automáticamente

# 4. Guardar favoritos
/nowplaying  # anotar canciones que gusten
/lyrics  # entender letras interesantes
```

---

## Consejos y Mejores Prácticas

### Gestión de Cola Eficiente

**Planificación:**
```
# Añadir varias canciones de una vez
/play consulta:playlist completa
# En lugar de una por una
```

**Organización:**
```
# Verificar cola regularmente
/queue

# Remover duplicados
/remove posición:X

# Reorganizar si es necesario
/shuffle
```

### Uso de Filtros

**Experimentación:**
```
# Probar filtros con diferentes géneros
/filters tipo:bassboost  # para EDM
/filters tipo:nightcore  # para pop
/filters tipo:vaporwave  # para chill
```

**Combinaciones:**
```
# No combinar filtros conflictivos
# nightcore + vaporwave = cancelación
# Usar /filters tipo:clear entre cambios
```

### Volumen Apropiado

**Por situación:**
```
# Conversación activa: 20-30
/volume nivel:25

# Escucha casual: 40-60
/volume nivel:50

# Fiesta/evento: 70-85
/volume nivel:80

# Nunca usar 100 por períodos largos
```

### Etiqueta Musical

**Votación respetuosa:**
- No spam de `/skip`
- Esperar a que otros voten
- Respetar gustos diversos

**Contribución balanceada:**
- No monopolizar la cola
- Variar géneros y estilos
- Considerar el ambiente del momento

**Uso de permisos:**
- Moderadores: usar poderes responsablemente
- Usuarios: respetar decisiones de moderación

---

> **Nota:** El sistema de música está diseñado para ser colaborativo. La mejor experiencia se logra cuando todos los usuarios participan respetuosamente y consideran las preferencias del grupo.