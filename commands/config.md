# ⚙️ Comandos de Configuración

Esta sección detalla todos los comandos de configuración disponibles, con ejemplos completos y casos de uso específicos.

---

## /config-antiscam

**Descripción:** Configura el sistema anti-scam y anti-raid del servidor.
**Permisos requeridos:** Administrador

### Subcomandos

#### staff-role
Configura los roles de staff que pueden gestionar el sistema anti-scam.

**Sintaxis:**
```
/config-antiscam staff-role rol:<@rol> añadir:<true/false>
```

**Parámetros:**
- `rol` (Rol, requerido): El rol a añadir o remover del sistema
- `añadir` (Boolean, requerido): `true` para añadir, `false` para remover

**Ejemplos:**
```
# Añadir rol de moderador al sistema
/config-antiscam staff-role rol:@Moderador añadir:true

# Remover rol de helper del sistema
/config-antiscam staff-role rol:@Helper añadir:false
```

#### notify-channel
Configura el canal de notificaciones y los roles del sistema.

**Sintaxis:**
```
/config-antiscam notify-channel canal:<#canal> staff-roles:<IDs> muted-role:<ID> [english-role:<ID>]
```

**Parámetros:**
- `canal` (Canal, requerido): Canal donde se enviarán las alertas
- `staff-roles` (String, requerido): IDs de roles de staff separados por comas
- `muted-role` (String, requerido): ID del rol de silenciado
- `english-role` (String, opcional): ID del rol de inglés

**Ejemplos:**
```
# Configuración básica
/config-antiscam notify-channel canal:#alertas-antiscam staff-roles:123456789,987654321 muted-role:555666777

# Configuración con rol de inglés
/config-antiscam notify-channel canal:#security-alerts staff-roles:123456789 muted-role:555666777 english-role:111222333
```

### Casos de Uso

**Configuración inicial del servidor:**
1. Primero configura el canal de notificaciones:
   ```
   /config-antiscam notify-channel canal:#mod-alerts staff-roles:123456789 muted-role:987654321
   ```

2. Luego añade los roles de staff uno por uno:
   ```
   /config-antiscam staff-role rol:@Administrador añadir:true
   /config-antiscam staff-role rol:@Moderador añadir:true
   /config-antiscam staff-role rol:@Helper añadir:true
   ```

**Actualización de roles:**
```
# Remover un rol que ya no es staff
/config-antiscam staff-role rol:@Ex-Moderador añadir:false

# Añadir nuevo rol de staff
/config-antiscam staff-role rol:@Nuevo-Moderador añadir:true
```

---

## /config-codes

**Descripción:** Configura el sistema de códigos de juegos de HoYoverse.
**Permisos requeridos:** Gestionar Mensajes

### Funcionalidad
Este comando abre un panel interactivo para configurar:
- Canales donde se pueden enviar códigos
- Roles que pueden usar el comando `/codes`
- Configuración de juegos soportados

**Sintaxis:**
```
/config-codes
```

**Ejemplo de uso:**
```
/config-codes
```

Al ejecutar este comando, aparecerá un menú interactivo donde podrás:
1. Seleccionar canales permitidos para códigos
2. Configurar roles con permisos
3. Activar/desactivar juegos específicos (Genshin Impact, Honkai: Star Rail, Zenless Zone Zero)

### Casos de Uso

**Configuración para servidor de Genshin Impact:**
1. Ejecuta `/config-codes`
2. Selecciona el canal `#genshin-codes`
3. Permite solo al rol `@Moderador` usar códigos
4. Activa únicamente Genshin Impact

**Configuración para servidor multi-juego:**
1. Ejecuta `/config-codes`
2. Selecciona múltiples canales: `#genshin-codes`, `#hsr-codes`, `#zzz-codes`
3. Permite a roles `@Moderador` y `@Game-Helper`
4. Activa todos los juegos de HoYoverse

---

## /level-config

**Descripción:** Configura el sistema de niveles y experiencia del servidor.
**Permisos requeridos:** Gestionar Servidor

### Funcionalidad
Este comando abre un panel de configuración completo para:
- Canal de anuncios de nivel
- Multiplicadores de XP
- Roles con bonus de experiencia
- Canales excluidos del sistema

**Sintaxis:**
```
/level-config
```

**Ejemplo:**
```
/level-config
```

### Configuraciones Disponibles

**Canal de Anuncios:**
- Configura dónde se envían las notificaciones de subida de nivel
- Personaliza el mensaje de felicitación
- Activa/desactiva menciones

**Multiplicadores de XP:**
- Configura diferentes multiplicadores por rol
- Establece bonus para boosters del servidor
- Define XP base por mensaje

**Canales Excluidos:**
- Excluye canales específicos del sistema de XP
- Útil para canales de spam o bots

### Casos de Uso

**Servidor gaming básico:**
1. Ejecuta `/level-config`
2. Establece canal de anuncios: `#level-ups`
3. Configura multiplicador x1.5 para `@Booster`
4. Excluye canales: `#bot-commands`, `#spam`

**Servidor con sistema de roles complejo:**
1. Ejecuta `/level-config`
2. Configura múltiples multiplicadores:
   - `@VIP`: x2.0
   - `@Donador`: x1.5
   - `@Activo`: x1.2
3. Establece XP base: 15-25 por mensaje
4. Activa menciones solo para niveles múltiplos de 10

---

## /welcome-config

**Descripción:** Configura el sistema de mensajes de bienvenida del servidor.
**Permisos requeridos:** Gestionar Servidor

### Subcomandos

#### channel
Establece el canal donde se enviarán los mensajes de bienvenida.

**Sintaxis:**
```
/welcome-config channel canal:<#canal>
```

**Parámetros:**
- `canal` (Canal, requerido): Canal de bienvenidas

**Ejemplo:**
```
/welcome-config channel canal:#bienvenidas
```

#### message
Configura el mensaje personalizado de bienvenida.

**Sintaxis:**
```
/welcome-config message mensaje:<texto>
```

**Parámetros:**
- `mensaje` (String, opcional): Mensaje personalizado con variables

**Variables disponibles:**
- `{mention}` - Menciona al usuario
- `{username}` - Nombre del usuario
- `{guildName}` - Nombre del servidor
- `{memberCount}` - Número total de miembros

**Ejemplos:**
```
# Mensaje básico
/welcome-config message mensaje:¡Bienvenido {mention} al servidor {guildName}!

# Mensaje completo
/welcome-config message mensaje:🎉 ¡Hola {mention}! Bienvenido a **{guildName}**. Ahora somos {memberCount} miembros. ¡Esperamos que disfrutes tu estadía!

# Mensaje temático para Genshin
/welcome-config message mensaje:⚡ ¡Un nuevo Viajero ha llegado a Teyvat! Bienvenido {mention} a {guildName}. ¡Que tengas suerte en tus deseos! 🌟
```

### Casos de Uso

**Configuración básica:**
```
# Paso 1: Configurar canal
/welcome-config channel canal:#general

# Paso 2: Configurar mensaje
/welcome-config message mensaje:¡Bienvenido {mention} a {guildName}!
```

**Servidor de Genshin Impact:**
```
/welcome-config channel canal:#bienvenidas-teyvat
/welcome-config message mensaje:🌟 ¡Un nuevo Viajero se une a nuestra aventura! Bienvenido {mention} a **{guildName}**. Somos {memberCount} exploradores de Teyvat. ¡Que la suerte te acompañe en tus invocaciones! ⚡
```

**Servidor profesional:**
```
/welcome-config channel canal:#nuevos-miembros
/welcome-config message mensaje:👋 Hola {username}, bienvenido a {guildName}. Por favor lee las reglas en #reglas y preséntate en #presentaciones. ¡Esperamos tu participación!
```

**Servidor gaming:**
```
/welcome-config channel canal:#lobby
/welcome-config message mensaje:🎮 ¡Player {mention} has joined the game! Bienvenido a {guildName}, ahora somos {memberCount} gamers. ¡Prepárate para la diversión!
```

---

## /youtube-notifications

**Descripción:** Configura el sistema de notificaciones de YouTube.
**Permisos requeridos:** Gestionar Servidor

### Funcionalidad
Este comando abre un panel interactivo para:
- Añadir canales de YouTube a monitorear
- Configurar canal de Discord para notificaciones
- Personalizar mensajes de notificación
- Configurar roles a mencionar

**Sintaxis:**
```
/youtube-notifications
```

**Ejemplo:**
```
/youtube-notifications
```

### Configuraciones Disponibles

**Canales de YouTube:**
- Añadir/remover canales por URL o ID
- Verificar estado de monitoreo
- Ver lista de canales configurados

**Canal de Notificaciones:**
- Seleccionar canal de Discord
- Configurar formato de mensaje
- Activar/desactivar embeds

**Menciones:**
- Configurar roles a mencionar
- Activar/desactivar @everyone
- Personalizar por canal de YouTube

### Casos de Uso

**Servidor de Genshin Impact:**
1. Ejecuta `/youtube-notifications`
2. Añade canales oficiales:
   - Genshin Impact Official
   - HoYoverse
   - Genshin Impact ES
3. Configura canal: `#noticias-genshin`
4. Menciona rol: `@Genshin News`

**Servidor de contenido:**
1. Ejecuta `/youtube-notifications`
2. Añade canales de creadores de contenido
3. Configura canal: `#nuevos-videos`
4. Personaliza mensaje: "🎥 ¡Nuevo video de {channel}! {title}"

---

## Comandos Adicionales de Configuración

### /modmail-config
**Descripción:** Configura el sistema de modmail.
**Uso:** Panel interactivo para configurar categorías, roles de staff y mensajes automáticos.

### /rank-rol-config
**Descripción:** Configura roles automáticos por nivel.
**Uso:** Define qué roles se otorgan automáticamente al alcanzar ciertos niveles.

### /self-roles
**Descripción:** Configura roles auto-asignables.
**Uso:** Permite a los usuarios asignarse roles específicos mediante reacciones o comandos.

### /set-boost-channel
**Descripción:** Configura el canal de anuncios de boost.
**Uso:** Define dónde se anuncian los nuevos boosts del servidor.

### /set-lvl-channel
**Descripción:** Configura el canal de anuncios de nivel.
**Uso:** Alternativa rápida para configurar solo el canal de niveles.

### /test-boost
**Descripción:** Prueba el sistema de notificaciones de boost.
**Uso:** Envía un mensaje de prueba para verificar la configuración.

---

## Consejos de Configuración

### Orden Recomendado de Configuración

1. **Configuración básica:**
   - `/welcome-config` - Mensajes de bienvenida
   - `/level-config` - Sistema de niveles
   - `/set-boost-channel` - Anuncios de boost

2. **Seguridad:**
   - `/config-antiscam` - Sistema anti-scam
   - `/modmail-config` - Sistema de tickets

3. **Entretenimiento:**
   - `/config-codes` - Códigos de juegos
   - `/youtube-notifications` - Notificaciones

4. **Roles avanzados:**
   - `/rank-rol-config` - Roles por nivel
   - `/self-roles` - Roles auto-asignables

### Mejores Prácticas

**Seguridad:**
- Siempre configura el sistema anti-scam antes de hacer público el servidor
- Usa roles específicos para cada función
- Mantén logs de todas las configuraciones

**Experiencia de Usuario:**
- Personaliza mensajes de bienvenida según la temática del servidor
- Configura canales específicos para cada tipo de notificación
- Usa variables dinámicas para hacer mensajes más personales

**Mantenimiento:**
- Revisa configuraciones regularmente
- Prueba sistemas después de cambios importantes
- Mantén respaldos de configuraciones críticas

---

> **Nota:** Todos los comandos de configuración requieren permisos específicos. Asegúrate de tener los permisos necesarios antes de intentar configurar cualquier sistema.