# Guía Rápida

¡Bienvenido a **Dark-Bot**! Esta guía te ayudará a configurar y usar el bot en pocos minutos.

## 🚀 Paso 1: Invitar el Bot

1. Haz clic en el [enlace de invitación](/invite)
2. Selecciona tu servidor de Discord
3. Autoriza los permisos necesarios
4. ¡El bot se unirá automáticamente!

::: tip Permisos Recomendados
Para un funcionamiento óptimo, asegúrate de que el bot tenga permisos de:

- Leer mensajes
- Enviar mensajes
- Gestionar mensajes
- Conectar y hablar en canales de voz
- Usar comandos de barra
  :::

## ⚙️ Paso 2: Configuración Inicial

Una vez que el bot esté en tu servidor, usa estos comandos básicos:

### Configurar el idioma

```
/config idioma español
```

### Configurar canal de bienvenidas

```
/config welcome canal #bienvenidas
```

### Configurar roles automáticos

```
/config autorole add @Miembro
```

## 🔧 Paso 3: Probar el Verificador KQMC

El verificador KQMC es una de las características más populares del bot:

```
/tc uid:123456789
```

Esto analizará tu cuenta de Genshin Impact y generará un reporte detallado de tus builds.

::: warning Nota Importante
Asegúrate de que tu showcase de personajes esté visible en tu perfil de Genshin Impact para obtener los mejores resultados.
:::

## 🎵 Paso 4: Reproducir Música

Para usar el sistema de música:

1. Únete a un canal de voz
2. Usa el comando:
   ```
   /play canción:nombre de la canción
   ```
3. Controla la reproducción con:
   - `/pause` - Pausar
   - `/resume` - Reanudar
   - `/skip` - Saltar canción
   - `/queue` - Ver cola

## 🛡️ Paso 5: Configurar Moderación

### Anti-Spam

```
/config antispam enable
/config antispam limite 5
```

### Sistema de Logs

```
/config logs canal #mod-logs
/config logs eventos all
```

### Sistema de Tickets

```
/ticket setup #tickets
```

## 📖 Comandos Esenciales

| Comando   | Descripción                            |
| --------- | -------------------------------------- |
| `/help`   | Muestra todos los comandos disponibles |
| `/config` | Configuración del servidor             |
| `/tc`     | Verificador KQMC                       |
| `/play`   | Reproducir música                      |
| `/ticket` | Sistema de tickets                     |
| `/warn`   | Advertir usuarios                      |
| `/ban`    | Banear usuarios                        |
| `/kick`   | Expulsar usuarios                      |

## 🎮 Comandos Divertidos

- `/meme` - Genera memes aleatorios
- `/8ball pregunta` - Bola 8 mágica
- `/roll dados` - Lanzar dados
- `/avatar @usuario` - Ver avatar de usuario
- `/serverinfo` - Información del servidor

## 🔍 Solución de Problemas Comunes

### El bot no responde

- Verifica que tenga permisos para leer y enviar mensajes
- Asegúrate de usar `/` antes de los comandos
- Revisa que el bot esté online

### El verificador KQMC no funciona

- Verifica que tu UID sea correcto
- Asegúrate de que tu showcase esté visible
- Espera unos segundos, el análisis puede tardar

### La música no se reproduce

- Únete a un canal de voz primero
- Verifica que el bot tenga permisos de voz
- Prueba con una canción diferente

## 📚 Próximos Pasos

¡Felicidades! Ya tienes lo básico configurado. Ahora puedes:

- 📖 Explorar todos los [comandos disponibles](/commands/)
- ⚙️ Personalizar la [configuración avanzada](/config/)
- 🔧 Aprender más sobre el [verificador KQMC](/kqmc/)
- 🎵 Configurar el [sistema de música](/music/)
- ❓ Consultar las [preguntas frecuentes](/faq)

¿Necesitas más ayuda? Únete a nuestro [servidor de soporte](/support) donde la comunidad y el equipo de desarrollo estarán encantados de ayudarte.

---

::: info ¿Te gusta el bot?
¡Considera dejar una reseña positiva y recomendar **Dark-Bot** a otros servidores!
:::
