# Preguntas Frecuentes (FAQ)

Aquí encontrarás respuestas a las preguntas más comunes sobre **Dark-Bot**.

## 🤖 General

### ¿Qué es Dark-Bot?

**Dark-Bot** es un bot multifuncional de Discord diseñado específicamente para comunidades de Genshin Impact, aunque es versátil para cualquier servidor. Incluye un verificador KQMC avanzado, sistema de música, moderación y más de 100 comandos.

### ¿Es gratis?

¡Sí! **Dark-Bot** es completamente gratuito. No hay costos ocultos ni funciones premium.

### ¿En qué idiomas está disponible?

Actualmente soporta:

- 🇪🇸 Español (principal)
- 🇺🇸 Inglés
- 🇨🇳 Chino
- 🇯🇵 Japonés
- 🇰🇷 Coreano

### ¿Cómo invito el bot a mi servidor?

Usa nuestro [enlace de invitación oficial](/invite) y sigue la [guía de configuración](/setup).

## 🔧 Verificador KQMC

### ¿Qué es el verificador KQMC?

Es un sistema avanzado que analiza tus builds de Genshin Impact, verifica la autenticidad de tus artefactos y proporciona análisis detallados de optimización.

### ¿Cómo uso el verificador?

```
/tc uid:123456789
```

Asegúrate de que tu showcase de personajes esté público en Genshin Impact.

### ¿Por qué dice "UID no encontrado"?

- Verifica que tu UID sea correcto (9 dígitos)
- Asegúrate de que tu showcase esté público
- Los servidores de Genshin pueden estar ocupados, intenta más tarde

### ¿Qué significa "Cannot find integer subs"?

Este error ocurre con artefactos mixtos (5★ en sets 4★). El sistema lo maneja automáticamente en la mayoría de casos.

### ¿El verificador funciona en todos los servidores?

Sí, funciona en:

- 🇺🇸 América
- 🇪🇺 Europa
- 🇦🇸 Asia
- 🇹🇼 TW/HK/MO

### ¿Qué tan preciso es el verificador?

Tiene una precisión del **99.2%** en la detección de artefactos válidos y procesa más de 1000 análisis diarios.

## 🎵 Sistema de Música

### ¿Qué plataformas soporta?

- YouTube
- Spotify (enlaces)
- SoundCloud
- Bandcamp
- Twitch
- Y más...

### ¿Por qué la música no se reproduce?

1. Únete a un canal de voz primero
2. Verifica que el bot tenga permisos de voz
3. Asegúrate de que el bot pueda conectar al canal
4. Prueba con una canción diferente

### ¿Puedo crear playlists?

¡Sí! Usa:

```
/playlist crear nombre:"Mi Playlist"
/playlist agregar playlist:"Mi Playlist" canción:"nombre"
```

### ¿Hay límite de duración?

Por defecto, las canciones están limitadas a 10 minutos, pero puedes configurarlo:

```
/config musica duracion_max 600
```

## 🛡️ Moderación

### ¿Qué comandos de moderación tiene?

- `/ban` - Banear usuarios
- `/kick` - Expulsar usuarios
- `/warn` - Advertir usuarios
- `/mute` - Silenciar usuarios
- `/clear` - Limpiar mensajes
- Y muchos más...

### ¿Cómo configuro el anti-spam?

```
/config antispam activar true
/config antispam limite_mensajes 5
/config antispam tiempo_limite 10
```

### ¿Puedo configurar auto-moderación?

¡Sí! El bot puede detectar automáticamente:

- Spam de mensajes
- Enlaces maliciosos
- Palabras prohibidas
- Menciones masivas

## ⚙️ Configuración

### ¿Cómo cambio el idioma del bot?

```
/config idioma español
```

### ¿Puedo personalizar los comandos?

Puedes configurar permisos específicos:

```
/permisos comando:ban roles:@Moderador
```

### ¿Cómo hago backup de mi configuración?

```
/config exportar
```

Esto te dará un archivo que puedes guardar y restaurar después.

### ¿Puedo usar el bot en múltiples servidores?

¡Sí! Cada servidor tiene su configuración independiente.

## 🎮 Comandos y Funciones

### ¿Cuántos comandos tiene el bot?

Más de **100 comandos** organizados en categorías:

- Verificador KQMC
- Música
- Moderación
- Utilidades
- Juegos
- Imágenes
- Configuración

### ¿Cómo veo todos los comandos?

```
/help
```

O visita nuestra [documentación de comandos](/commands/).

### ¿Los comandos funcionan en DM?

Algunos comandos básicos sí, pero la mayoría requieren estar en un servidor.

## 🔒 Permisos y Seguridad

### ¿Qué permisos necesita el bot?

Para funcionalidad completa:

- Leer/enviar mensajes
- Gestionar mensajes
- Conectar/hablar en voz
- Gestionar roles (para auto-roles)
- Banear/expulsar miembros (para moderación)

### ¿Es seguro el bot?

¡Absolutamente! El bot:

- No almacena información personal
- Solo accede a datos públicos de Genshin
- Cumple con las políticas de Discord
- Código auditado regularmente

### ¿Puedo limitar el bot a ciertos canales?

Sí, puedes configurar permisos por canal en la configuración del servidor de Discord.

## 🐛 Problemas Técnicos

### El bot está offline

- Puede estar en mantenimiento temporal
- Verifica el [estado del servicio](/status)
- Contacta [soporte](/support) si persiste

### Los comandos no aparecen

- Asegúrate de que el bot tenga permisos de "Usar comandos de barra"
- Reinicia Discord
- Verifica que el bot esté en el servidor

### Error "Falta acceso"

- Verifica permisos del bot
- Asegúrate de que pueda leer/escribir en el canal
- Revisa la configuración de roles

### El bot responde lento

- Los servidores pueden estar ocupados
- Comandos complejos (como KQMC) pueden tardar más
- Verifica tu conexión a internet

## 📊 Estadísticas y Límites

### ¿Hay límites de uso?

- Verificador KQMC: 10 usos por hora por usuario
- Música: Sin límites específicos
- Comandos generales: Sin límites

### ¿Cuántos servidores usa el bot?

Actualmente en **+1000 servidores** con **+50,000 usuarios** únicos.

### ¿Qué tan rápido es el bot?

Latencia promedio: **<100ms**
Tiempo de actividad: **99.9%**

## 🆕 Actualizaciones

### ¿Con qué frecuencia se actualiza?

Actualizaciones regulares cada 2-4 semanas con:

- Nuevas funciones
- Corrección de errores
- Mejoras de rendimiento
- Soporte para nuevos personajes de Genshin

### ¿Cómo me entero de las actualizaciones?

- Únete a nuestro [servidor de soporte](/support)
- Sigue nuestro [changelog](/changelog)
- Configura notificaciones en tu servidor

## 💡 Consejos y Trucos

### ¿Cómo optimizo el rendimiento?

1. Configura canales específicos para cada función
2. Usa roles para organizar permisos
3. Configura auto-moderación para reducir carga
4. Mantén la configuración actualizada

### ¿Cómo mejoro la experiencia de usuario?

1. Configura mensajes de bienvenida personalizados
2. Crea canales temáticos
3. Usa el sistema de tickets para soporte
4. Configura roles automáticos

## 🆘 Obtener Ayuda

### ¿Dónde puedo obtener soporte?

- 📖 Consulta esta documentación
- 💬 Únete a nuestro [servidor de soporte](/support)
- 📧 Contacta al equipo de desarrollo
- 🐛 Reporta bugs en GitHub

### ¿Cómo reporto un error?

1. Describe el problema detalladamente
2. Incluye capturas de pantalla si es posible
3. Menciona los pasos para reproducir el error
4. Proporciona tu ID de servidor si es relevante

### ¿Puedo sugerir nuevas funciones?

¡Por supuesto! Únete a nuestro servidor de soporte y comparte tus ideas en el canal de sugerencias.

---

::: tip ¿No encuentras tu respuesta?
Si tu pregunta no está aquí, únete a nuestro [servidor de soporte](/support) donde la comunidad y el equipo de desarrollo estarán encantados de ayudarte.
:::

¿Quieres contribuir a esta FAQ? ¡Las sugerencias son bienvenidas en nuestro servidor de Discord!
