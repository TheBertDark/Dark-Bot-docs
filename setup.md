# Configuración Inicial

¡Perfecto! Ya tienes **Dark-Bot** en tu servidor. Ahora vamos a configurarlo para que funcione perfectamente según las necesidades de tu comunidad.

## 🚀 Configuración Rápida (5 minutos)

Sigue estos pasos esenciales para tener el bot funcionando:

### 1. Verificar Instalación

```
/setup verificar
```

Este comando revisa que todos los permisos estén correctos y el bot funcione adecuadamente.

### 2. Configurar Idioma

```
/config idioma español
```

Establece el idioma principal del bot para tu servidor.

### 3. Configurar Canal de Logs

```
/config logs canal #mod-logs
```

Crea un canal llamado `#mod-logs` y configúralo para recibir registros de moderación.

### 4. Probar Funcionalidad Básica

```
/ping
```

Verifica que el bot responda correctamente.

¡Listo! Tu bot ya está funcionando. Para configuraciones avanzadas, continúa leyendo.

## ⚙️ Configuración Completa

### 🏠 Configuración del Servidor

#### Información Básica

```
/config servidor nombre:"Mi Servidor Genial"
/config servidor descripción:"Servidor dedicado a Genshin Impact"
/config servidor zona_horaria:America/Mexico_City
```

#### Prefijo de Comandos (Opcional)

```
/config prefijo !
```

::: info Nota
Los slash commands (`/`) siempre funcionan independientemente del prefijo configurado.
:::

### 👋 Sistema de Bienvenidas

#### Configuración Básica

```
/config welcome canal #bienvenidas
/config welcome mensaje "¡Bienvenido {user} a {server}! 🎉"
/config welcome activar true
```

#### Mensaje Personalizado

```
/config welcome mensaje "¡Hola {user}! 👋

🌟 Bienvenido a **{server}**
📖 Lee las reglas en #reglas
🎮 Comparte tu UID en #genshin-uids
🔧 Prueba el verificador con `/tc`

¡Disfruta tu estadía!"
```

#### Variables Disponibles

- `{user}` - Mención del usuario
- `{username}` - Nombre del usuario
- `{server}` - Nombre del servidor
- `{membercount}` - Número de miembros
- `{date}` - Fecha actual

### 🎵 Sistema de Música

#### Configuración Básica

```
/config musica canal #música
/config musica volumen_default 50
/config musica auto_disconnect 300
```

#### Configuración Avanzada

```
/config musica calidad alta
/config musica filtros_permitidos true
/config musica playlist_max 100
/config musica duracion_max 600
```

### 🛡️ Sistema de Moderación

#### Anti-Spam

```
/config antispam activar true
/config antispam limite_mensajes 5
/config antispam tiempo_limite 10
/config antispam accion mute
```

#### Auto-Moderación

```
/config automod palabras_prohibidas true
/config automod enlaces_spam true
/config automod menciones_masivas true
/config automod limite_menciones 5
```

#### Sistema de Advertencias

```
/config warns limite 3
/config warns accion_limite ban
/config warns tiempo_expiracion 30d
```

### 🎫 Sistema de Tickets

#### Configuración Inicial

```
/ticket setup canal:#tickets categoría:"Soporte"
```

#### Personalización

```
/ticket config mensaje_bienvenida "¡Hola! Un moderador te atenderá pronto."
/ticket config roles_soporte @Moderador @Admin
/ticket config auto_cerrar 24h
```

### 🔧 Verificador KQMC

#### Configuración del Canal

```
/config kqmc canal #verificaciones
/config kqmc idioma_reportes español
/config kqmc mostrar_detalles true
```

#### Configuración Avanzada

```
/config kqmc cache_tiempo 30m
/config kqmc formato_reporte completo
/config kqmc notificaciones_error true
```

## 🎯 Roles y Permisos

### Crear Roles Recomendados

#### Roles de Staff

```
/role crear nombre:"🔧 Bot Manager" color:#5865f2
/role crear nombre:"🛡️ Moderador" color:#e74c3c
/role crear nombre:"👑 Admin" color:#f1c40f
```

#### Roles de Comunidad

```
/role crear nombre:"🎵 DJ" color:#9b59b6
/role crear nombre:"🎮 Gamer" color:#2ecc71
/role crear nombre:"📊 Theorycrafter" color:#3498db
```

### Configurar Auto-Roles

```
/config autorole agregar @Miembro
/config autorole activar true
```

### Permisos por Comando

```
/permisos comando:ban roles:@Moderador,@Admin
/permisos comando:kick roles:@Moderador,@Admin
/permisos comando:config roles:@Bot Manager,@Admin
```

## 📊 Canales Recomendados

### Estructura Básica

```
📋 INFORMACIÓN
├── 📜 reglas
├── 📢 anuncios
└── 🆔 genshin-uids

💬 CHAT GENERAL
├── 💬 general
├── 🎮 genshin-chat
└── 🔧 verificaciones

🎵 ENTRETENIMIENTO
├── 🎵 música
├── 🎮 juegos
└── 🖼️ memes

🛡️ MODERACIÓN
├── 🛡️ mod-logs
├── 🎫 tickets
└── 🚨 reportes
```

### Configurar Canales Específicos

```
/config canal #verificaciones tipo:kqmc
/config canal #música tipo:musica
/config canal #mod-logs tipo:logs
/config canal #tickets tipo:tickets
```

## 🔔 Notificaciones

### YouTube/Twitch

```
/config notificaciones youtube canal:#anuncios
/config notificaciones youtube agregar "@GenshinImpactOfficial"
/config notificaciones twitch canal:#streams
```

### Eventos del Servidor

```
/config eventos member_join true
/config eventos member_leave true
/config eventos message_delete true
/config eventos role_update true
```

## 🎨 Personalización Visual

### Colores del Bot

```
/config colores principal:#5865f2
/config colores exito:#00ff00
/config colores error:#ff0000
/config colores advertencia:#ffff00
```

### Emojis Personalizados

```
/config emojis exito:✅
/config emojis error:❌
/config emojis cargando:⏳
/config emojis musica:🎵
```

## 📋 Lista de Verificación

Marca cada elemento cuando lo hayas configurado:

- [ ] ✅ Verificar instalación del bot
- [ ] 🌐 Configurar idioma
- [ ] 📝 Configurar canal de logs
- [ ] 👋 Sistema de bienvenidas
- [ ] 🛡️ Configuración de moderación
- [ ] 🎵 Sistema de música
- [ ] 🎫 Sistema de tickets
- [ ] 🔧 Verificador KQMC
- [ ] 👥 Roles y permisos
- [ ] 📊 Estructura de canales
- [ ] 🔔 Notificaciones
- [ ] 🎨 Personalización visual

## 🔧 Comandos de Configuración Útiles

### Ver Configuración Actual

```
/config mostrar
```

### Exportar Configuración

```
/config exportar
```

### Importar Configuración

```
/config importar archivo:config.json
```

### Restablecer Configuración

```
/config reset categoria:musica
/config reset todo  # ⚠️ Cuidado: borra toda la configuración
```

## 🆘 Solución de Problemas

### El bot no responde a comandos

1. Verifica permisos de "Usar comandos de barra"
2. Asegúrate de que el bot pueda leer mensajes
3. Revisa que esté online

### Los logs no aparecen

1. Verifica que el canal de logs exista
2. Asegúrate de que el bot pueda escribir en el canal
3. Revisa la configuración con `/config mostrar`

### La música no funciona

1. Únete a un canal de voz primero
2. Verifica permisos de voz del bot
3. Asegúrate de que el canal de música esté configurado

### El verificador KQMC falla

1. Verifica que el UID sea correcto
2. Asegúrate de que el showcase esté público
3. Revisa la configuración del canal KQMC

## 📚 Próximos Pasos

¡Felicidades! Tu bot está completamente configurado. Ahora puedes:

- 📖 Explorar todos los [comandos disponibles](/commands/)
- 🔧 Aprender más sobre el [verificador KQMC](/kqmc/)
- 🎵 Configurar [playlists de música](/music/playlists)
- 🛡️ Configurar [moderación avanzada](/config/moderation)
- ❓ Consultar las [preguntas frecuentes](/faq)

---

::: tip Consejo Pro
¡Guarda tu configuración regularmente con `/config exportar`! Esto te permitirá restaurar rápidamente la configuración si algo sale mal.
:::

¿Necesitas ayuda adicional? Únete a nuestro [servidor de soporte](/support) donde la comunidad y el equipo de desarrollo estarán encantados de ayudarte.
