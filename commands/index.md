# 📋 Comandos

Esta sección documenta todos los comandos slash disponibles, organizados por categoría. Cada comando incluye descripción técnica, permisos requeridos, tabla de opciones y ejemplos de uso basados en el código fuente real del bot.

---

## ⚙️ Configuración

### /config-antiscam
**Descripción:** Configura el sistema anti-scam y anti-raid.
**Permisos requeridos:** Administrador

| Subcomando       | Opción           | Tipo     | Requerido | Descripción                                       |
|------------------|------------------|----------|-----------|---------------------------------------------------|
| staff-role       | rol              | Rol      | Sí        | El rol para añadir o remover                      |
|                  | añadir           | Boolean  | Sí        | True para añadir, False para remover              |
| notify-channel   | canal            | Canal    | Sí        | Canal donde se enviarán las notificaciones        |
|                  | staff-roles      | String   | Sí        | IDs de roles de staff separados por comas         |
|                  | muted-role       | String   | Sí        | ID del rol de silenciado                          |
|                  | english-role     | String   | No        | ID del rol de inglés                              |

**Ejemplo:**
```
/config-antiscam staff-role rol:@Moderador añadir:true
/config-antiscam notify-channel canal:#alertas staff-roles:123456789 muted-role:987654321
```

### /config-codes
**Descripción:** Configura el sistema de códigos de juegos.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/config-codes
```

### /level-config
**Descripción:** Configura el sistema de niveles y XP.
**Permisos requeridos:** Gestionar Servidor

**Ejemplo:**
```
/level-config
```

### /modmail-config
**Descripción:** Configura el sistema de modmail.
**Permisos requeridos:** Administrador

**Ejemplo:**
```
/modmail-config
```

### /rank-rol-config
**Descripción:** Configura roles automáticos por nivel.
**Permisos requeridos:** Gestionar Roles

**Ejemplo:**
```
/rank-rol-config
```

### /self-roles
**Descripción:** Configura roles auto-asignables.
**Permisos requeridos:** Gestionar Roles

**Ejemplo:**
```
/self-roles
```

### /set-boost-channel
**Descripción:** Configura el canal de anuncios de boost.
**Permisos requeridos:** Gestionar Servidor

**Ejemplo:**
```
/set-boost-channel
```

### /set-lvl-channel
**Descripción:** Configura el canal de anuncios de nivel.
**Permisos requeridos:** Gestionar Servidor

**Ejemplo:**
```
/set-lvl-channel
```

### /test-boost
**Descripción:** Prueba el sistema de notificaciones de boost.
**Permisos requeridos:** Administrador

**Ejemplo:**
```
/test-boost
```

### /welcome-config
**Descripción:** Configura el sistema de bienvenidas del servidor.
**Permisos requeridos:** Gestionar Servidor

| Subcomando | Opción  | Tipo   | Requerido | Descripción                                                    |
|------------|---------|--------|-----------|----------------------------------------------------------------|
| channel    | canal   | Canal  | Sí        | El canal donde se enviarán los mensajes de bienvenida         |
| message    | mensaje | String | No        | Mensaje personalizado (usa {mention}, {username}, {guildName}, {memberCount}) |

**Ejemplo:**
```
/welcome-config channel canal:#bienvenidas
/welcome-config message mensaje:¡Bienvenido {mention} al servidor {guildName}!
```

### /youtube-notifications
**Descripción:** Configura notificaciones de YouTube.
**Permisos requeridos:** Gestionar Servidor

**Ejemplo:**
```
/youtube-notifications
```

---

## 🛡️ Moderación

### /ban
**Descripción:** Gestiona los baneos del servidor con historial completo.
**Permisos requeridos:** Banear Miembros

| Subcomando | Opción    | Tipo    | Requerido | Descripción                       |
|------------|-----------|---------|-----------|-----------------------------------|
| add        | usuario   | Usuario | Sí        | Usuario a banear                  |
|            | razón     | String  | No        | Motivo del baneo                  |
|            | duración  | String  | No        | Duración del baneo temporal       |
| list       | usuario   | Usuario | No        | Ver historial de baneos           |
| remove     | usuario   | Usuario | Sí        | Remover baneo del historial       |
|            | index     | Entero  | Sí        | Índice del baneo a remover        |

**Ejemplo:**
```
/ban add usuario:@Usuario razón:Spam duración:7d
/ban list usuario:@Usuario
```

### /kick
**Descripción:** Expulsa a un usuario del servidor.
**Permisos requeridos:** Expulsar Miembros

| Opción  | Tipo    | Requerido | Descripción           |
|---------|---------|-----------|----------------------|
| usuario | Usuario | Sí        | Usuario a expulsar    |
| razón   | String  | No        | Motivo de la expulsión|

**Ejemplo:**
```
/kick usuario:@Usuario razón:Comportamiento inapropiado
```

### /mute
**Descripción:** Gestiona los mutes del servidor.
**Permisos requeridos:** Silenciar Miembros

| Opción    | Tipo    | Requerido | Descripción                       |
|-----------|---------|-----------|-----------------------------------|
| usuario   | Usuario | Sí        | Usuario a silenciar               |
| razón     | String  | No        | Motivo del mute                   |
| duración  | String  | No        | Duración del mute                 |

**Ejemplo:**
```
/mute usuario:@Usuario razón:Spam duración:1h
```

### /warn
**Descripción:** Sistema completo de advertencias.
**Permisos requeridos:** Gestionar Mensajes

| Subcomando | Opción  | Tipo    | Requerido | Descripción                    |
|------------|---------|---------|-----------|--------------------------------|
| add        | usuario | Usuario | Sí        | Usuario a advertir             |
|            | razón   | String  | Sí        | Motivo de la advertencia       |
| list       | usuario | Usuario | Sí        | Ver advertencias de un usuario |
| remove     | usuario | Usuario | Sí        | Remover advertencia            |
|            | index   | Entero  | Sí        | Índice de la advertencia       |
| clear      | usuario | Usuario | Sí        | Limpiar todas las advertencias |

**Ejemplo:**
```
/warn add usuario:@Usuario razón:Lenguaje inapropiado
/warn list usuario:@Usuario
```

### /unban
**Descripción:** Desbanea a un usuario del servidor.
**Permisos requeridos:** Banear Miembros

| Opción    | Tipo   | Requerido | Descripción              |
|-----------|--------|-----------|-------------------------|
| usuario-id| String | Sí        | ID del usuario a desbanear|
| razón     | String | No        | Motivo del desbaneo      |

**Ejemplo:**
```
/unban usuario-id:123456789 razón:Apelación aceptada
```

### /lock
**Descripción:** Bloquea un canal para que los usuarios no puedan escribir.
**Permisos requeridos:** Gestionar Canales

| Opción | Tipo  | Requerido | Descripción                    |
|--------|-------|-----------|--------------------------------|
| canal  | Canal | No        | Canal a bloquear (actual si no se especifica) |
| razón  | String| No        | Motivo del bloqueo             |

**Ejemplo:**
```
/lock canal:#general razón:Mantenimiento
```

### /unlock
**Descripción:** Desbloquea un canal previamente bloqueado.
**Permisos requeridos:** Gestionar Canales

| Opción | Tipo  | Requerido | Descripción                      |
|--------|-------|-----------|----------------------------------|
| canal  | Canal | No        | Canal a desbloquear (actual si no se especifica) |

**Ejemplo:**
```
/unlock canal:#general
```

### /ticket-panel
**Descripción:** Genera un panel de tickets.
**Permisos requeridos:** Gestionar Canales

| Opción    | Tipo      | Requerido | Descripción                           |
|-----------|-----------|-----------|---------------------------------------|
| canal     | Canal     | Sí        | Canal donde se enviará el panel       |
| categoria | Categoría | Sí        | Categoría donde se crearán los tickets|

**Ejemplo:**
```
/ticket-panel canal:#tickets categoria:Soporte
```

### /logs
**Descripción:** Configura el sistema de logs del servidor.
**Permisos requeridos:** Gestionar Servidor

**Ejemplo:**
```
/logs
```

### /modmail-reply
**Descripción:** Responde a un modmail.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/modmail-reply
```

### /modmail-anonreply
**Descripción:** Responde anónimamente a un modmail.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/modmail-anonreply
```

### /modmail-reopen
**Descripción:** Reabre un modmail cerrado.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/modmail-reopen
```

### /modmail-tag
**Descripción:** Añade etiquetas a un modmail.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/modmail-tag
```

### /modmail-block
**Descripción:** Bloquea a un usuario del sistema modmail.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/modmail-block
```

### /verified-send
**Descripción:** Envía un mensaje como usuario verificado.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/verified-send
```

---

## 🎁 Utilidad

### /giveaway
**Descripción:** Sistema completo de giveaways con múltiples opciones.
**Permisos requeridos:** Gestionar Eventos

| Subcomando      | Opción           | Tipo     | Requerido | Descripción                       |
|-----------------|------------------|----------|-----------|-----------------------------------|
| crear           | canal            | Canal    | Sí        | Canal donde se enviará el sorteo   |
|                 | premio           | String   | Sí        | Premio del sorteo                 |
|                 | duracion         | String   | Sí        | Duración (ej: 1d, 2h, 30m)        |
|                 | ganadores        | Entero   | No        | Número de ganadores (mín: 1, máx: 20) |
|                 | host             | Usuario  | No        | Usuario anfitrión                 |
|                 | titulo           | String   | No        | Título personalizado              |
|                 | descripcion      | String   | No        | Descripción adicional             |
|                 | color            | String   | No        | Color del embed (hex)             |
|                 | imagen           | String   | No        | URL de imagen                     |
|                 | thumbnail        | String   | No        | URL de thumbnail                  |
| terminar        | mensaje-id       | String   | Sí        | ID del mensaje del sorteo         |
| reroll          | mensaje-id       | String   | Sí        | ID del mensaje del sorteo         |
|                 | nuevos-ganadores | Entero   | No        | Número de nuevos ganadores        |
| participantes   | mensaje-id       | String   | Sí        | ID del mensaje del sorteo         |
| remover         | mensaje-id       | String   | Sí        | ID del mensaje del sorteo         |
|                 | usuario          | Usuario  | Sí        | Usuario a remover                 |
| configurar-roles| rol              | Rol      | Sí        | Rol a configurar                  |
|                 | multiplicador    | Número   | Sí        | Multiplicador para ese rol        |
| requisitos      | mensaje-id       | String   | Sí        | ID del giveaway                   |
|                 | nivel-minimo     | Entero   | No        | Nivel mínimo requerido            |
|                 | roles-requeridos | String   | No        | IDs de roles separados por comas  |
|                 | roles-prohibidos | String   | No        | IDs de roles prohibidos           |
| cancelar        | mensaje-id       | String   | Sí        | ID del mensaje del sorteo         |
| lista           | (sin opciones)   | -        | -         | Lista de sorteos activos          |

**Ejemplo:**
```
/giveaway crear canal:#sorteos premio:"Discord Nitro" duracion:1d ganadores:2
/giveaway requisitos mensaje-id:123456789 nivel-minimo:5
```

### /ask
**Descripción:** Hazle una pregunta a la IA integrada (Gemini).
**Permisos requeridos:** Ninguno

| Opción   | Tipo   | Requerido | Descripción                    |
|----------|--------|-----------|--------------------------------|
| pregunta | String | Sí        | La pregunta que quieres hacer  |

**Ejemplo:**
```
/ask pregunta:¿Cuál es la capital de Francia?
```

### /avatar
**Descripción:** Muestra el avatar de un usuario.
**Permisos requeridos:** Ninguno

| Opción  | Tipo    | Requerido | Descripción                           |
|---------|---------|-----------|---------------------------------------|
| usuario | Usuario | No        | Usuario del que mostrar el avatar     |

**Ejemplo:**
```
/avatar usuario:@Usuario
```

### /embed
**Descripción:** Crea un embed personalizado.
**Permisos requeridos:** Gestionar Mensajes

**Ejemplo:**
```
/embed
```

### /latex
**Descripción:** Renderiza fórmulas matemáticas en LaTeX.
**Permisos requeridos:** Ninguno

| Opción  | Tipo   | Requerido | Descripción              |
|---------|--------|-----------|-------------------------|
| formula | String | Sí        | Fórmula LaTeX a renderizar|

**Ejemplo:**
```
/latex formula:E = mc^2
```

### /leaderboard
**Descripción:** Muestra la tabla de clasificación de niveles del servidor.
**Permisos requeridos:** Ninguno

| Opción   | Tipo   | Requerido | Descripción                           |
|----------|--------|-----------|---------------------------------------|
| cantidad | Entero | No        | Número de usuarios a mostrar (máx: 8) |

**Ejemplo:**
```
/leaderboard cantidad:5
```

### /ping
**Descripción:** Muestra la latencia del bot y la API de Discord.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/ping
```

### /rank
**Descripción:** Muestra tu nivel y progreso en el servidor.
**Permisos requeridos:** Ninguno

| Opción  | Tipo    | Requerido | Descripción                    |
|---------|---------|-----------|--------------------------------|
| usuario | Usuario | No        | Usuario del que mostrar el rank|

**Ejemplo:**
```
/rank usuario:@Usuario
```

### /tc
**Descripción:** Verificador KQMC para Genshin Impact.
**Permisos requeridos:** Ninguno

| Opción | Tipo   | Requerido | Descripción           |
|--------|--------|-----------|----------------------|
| uid    | String | Sí        | UID de Genshin Impact |

**Ejemplo:**
```
/tc uid:123456789
```

### /error
**Descripción:** Comando de prueba para el sistema AntiCrash.
**Permisos requeridos:** Desarrollador

**Ejemplo:**
```
/error
```

---

## 🎮 Juegos y Entretenimiento

### /codes
**Descripción:** Envía códigos de canje para juegos de HoYoverse.
**Permisos requeridos:** Gestionar Mensajes

| Opción   | Tipo       | Requerido | Descripción                        |
|----------|------------|-----------|------------------------------------|
| juego    | Selección  | Sí        | Juego (Genshin Impact, Honkai: Star Rail, Zenless Zone Zero) |
| códigos  | String     | Sí        | Códigos separados por espacios     |
| imagen   | Archivo    | No        | Imagen personalizada para el embed |

**Ejemplo:**
```
/codes juego:gi códigos:GENSHINGIFT FREEPRIMOGEMS
```

### /puzzle
**Descripción:** Juega un rompecabezas deslizante interactivo.
**Permisos requeridos:** Ninguno

| Opción | Tipo   | Requerido | Descripción                     |
|--------|--------|-----------|--------------------------------|
| imagen | String | No        | URL de imagen personalizada     |

**Ejemplo:**
```
/puzzle imagen:https://ejemplo.com/imagen.jpg
```

---

## 🖼️ Imagen

### /imglarge
**Descripción:** Mejora la resolución de una imagen usando IA.
**Permisos requeridos:** Ninguno

| Opción  | Tipo    | Requerido | Descripción                     |
|---------|---------|-----------|--------------------------------|
| estilo  | String  | Sí        | "photo" o "art"                 |
| archivo | Archivo | Sí        | Imagen a mejorar (PNG, JPG, WEBP)|

**Ejemplo:**
```
/imglarge estilo:photo archivo:imagen.png
```

### /watermark
**Descripción:** Elimina marcas de agua de imágenes usando IA.
**Permisos requeridos:** Ninguno

| Opción  | Tipo    | Requerido | Descripción                     |
|---------|---------|-----------|--------------------------------|
| archivo | Archivo | Sí        | Imagen con marca de agua        |

**Ejemplo:**
```
/watermark archivo:imagen.png
```

### /wm-api
**Descripción:** Actualiza la clave de API de dewatermark.ai.
**Permisos requeridos:** Administrador

| Opción | Tipo   | Requerido | Descripción           |
|--------|--------|-----------|----------------------|
| key    | String | Sí        | Nueva clave de API    |

**Ejemplo:**
```
/wm-api key:tu_nueva_api_key
```

---

## 🎶 Música

### /play
**Descripción:** Reproduce música desde YouTube, Spotify o SoundCloud.
**Permisos requeridos:** Conectarse y Hablar en canal de voz

| Opción  | Tipo   | Requerido | Descripción                        |
|---------|--------|-----------|------------------------------------|
| cancion | String | Sí        | Nombre o URL de la canción         |

**Ejemplo:**
```
/play cancion:Never Gonna Give You Up
/play cancion:https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

### /pause
**Descripción:** Pausa la reproducción actual.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/pause
```

### /resume
**Descripción:** Reanuda la reproducción pausada.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/resume
```

### /skip
**Descripción:** Salta a la siguiente canción en la cola.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/skip
```

### /stop
**Descripción:** Detiene la reproducción y limpia la cola.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/stop
```

### /queue
**Descripción:** Muestra la lista de reproducción actual.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/queue
```

### /nowplaying
**Descripción:** Muestra información de la canción actual.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/nowplaying
```

### /volume
**Descripción:** Ajusta el volumen de reproducción.
**Permisos requeridos:** Ninguno

| Opción  | Tipo   | Requerido | Descripción                    |
|---------|--------|-----------|--------------------------------|
| volumen | Entero | Sí        | Nivel de volumen (0-100)       |

**Ejemplo:**
```
/volume volumen:50
```

### /loop
**Descripción:** Configura el modo de repetición.
**Permisos requeridos:** Ninguno

| Opción | Tipo   | Requerido | Descripción                           |
|--------|--------|-----------|---------------------------------------|
| modo   | String | Sí        | off, song, queue                      |

**Ejemplo:**
```
/loop modo:song
```

### /lyrics
**Descripción:** Muestra las letras de la canción actual.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/lyrics
```

### /search
**Descripción:** Busca canciones en YouTube.
**Permisos requeridos:** Ninguno

| Opción   | Tipo   | Requerido | Descripción              |
|----------|--------|-----------|-------------------------|
| consulta | String | Sí        | Término de búsqueda      |

**Ejemplo:**
```
/search consulta:Imagine Dragons
```

### /playlist
**Descripción:** Gestiona playlists personalizadas.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/playlist
```

### /songinfo
**Descripción:** Información detallada de una canción.
**Permisos requeridos:** Ninguno

| Opción  | Tipo   | Requerido | Descripción              |
|---------|--------|-----------|-------------------------|
| cancion | String | Sí        | Nombre o URL de la canción|

**Ejemplo:**
```
/songinfo cancion:Bohemian Rhapsody
```

### /musicstats
**Descripción:** Estadísticas de uso del sistema de música.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/musicstats
```

### /filter
**Descripción:** Aplica filtros de audio a la reproducción.
**Permisos requeridos:** Ninguno

| Opción | Tipo   | Requerido | Descripción                    |
|--------|--------|-----------|--------------------------------|
| filtro | String | Sí        | Tipo de filtro a aplicar       |

**Ejemplo:**
```
/filter filtro:bassboost
```

### /leave
**Descripción:** Desconecta el bot del canal de voz.
**Permisos requeridos:** Ninguno

**Ejemplo:**
```
/leave
```

---

## 🚀 Comandos Más Populares

### 1. Verificador KQMC

```
/tc uid:123456789
```

Analiza tu cuenta de Genshin Impact y genera un reporte detallado de tus builds con verificación KQMC.

### 2. Reproducir Música

```
/play cancion:Imagine Dragons - Believer
```

Reproducir música desde YouTube, Spotify y otras plataformas con alta calidad.

### 3. Sistema de Giveaways

```
/giveaway crear canal:#sorteos premio:"Discord Nitro" duracion:1d ganadores:2
```

Crea sorteos completos con múltiples opciones de configuración.

### 4. Configurar Bienvenidas

```
/welcome-config channel canal:#bienvenidas
/welcome-config message mensaje:¡Bienvenido {mention} a {guildName}!
```

Configura mensajes de bienvenida personalizados con variables dinámicas.

### 5. Sistema de Moderación

```
/ban add usuario:@usuario razón:Spam duración:7d
/warn add usuario:@usuario razón:Lenguaje inapropiado
```

Herramientas completas de moderación con historial y gestión avanzada.

### 6. IA Integrada

```
/ask pregunta:¿Cuál es la mejor build para Raiden Shogun?
```

Pregunta cualquier cosa a la IA integrada con contexto especializado en Genshin Impact.

---

> **Nota:** Todos los comandos están implementados como slash commands (/). El bot no utiliza comandos de prefijo tradicionales. Esta documentación refleja fielmente las funcionalidades reales implementadas en el código fuente del bot.
