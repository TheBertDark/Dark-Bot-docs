# 👋 Sistema de Bienvenidas - Dark-Bot

## 🎯 Bienvenidas Personalizadas

Dark-Bot ofrece un sistema de bienvenidas completo y personalizable que te permite dar la mejor primera impresión a los nuevos miembros de tu servidor.

## 🚀 Configuración Inicial

### Comando Principal
```
/welcome_setup
```
Este comando inicia el asistente de configuración de bienvenidas que te guiará paso a paso.

### Configuración Rápida
```
/welcome_quicksetup
```
Configura las bienvenidas básicas en menos de 2 minutos con valores recomendados.

## 📋 Tipos de Bienvenidas

### Bienvenidas en Canal
```
/welcome_channel <canal>
```

**Opciones Configurables**:
- **Canal de Bienvenidas**: Donde se enviarán los mensajes
- **Formato del Mensaje**: Texto, embed o imagen
- **Contenido**: Mensaje personalizado con variables
- **Menciones**: Mencionar al usuario o no
- **Imágenes**: Añadir imágenes o banners

**Variables Disponibles**:
- `{user}` - Mención del usuario (@Usuario)
- `{username}` - Nombre del usuario sin discriminador
- `{server}` - Nombre del servidor
- `{membercount}` - Número total de miembros
- `{position}` - Posición del miembro (ej: #100)
- `{date}` - Fecha actual
- `{time}` - Hora actual

### Mensajes Privados de Bienvenida
```
/welcome_dm
```

**Configuraciones**:
- **Activar/Desactivar**: Enviar DM o no
- **Contenido**: Mensaje personalizado
- **Formato**: Texto simple o embed
- **Imágenes**: Incluir imágenes o no
- **Timing**: Cuándo enviar el DM

**Ejemplo de Mensaje DM**:
```
¡Bienvenido/a a {server}, {username}!

Gracias por unirte a nuestra comunidad. Aquí tienes algunos recursos para empezar:

• #bienvenida - Información general
• #reglas - Normas del servidor
• #roles - Obtén roles personalizados

Si tienes alguna pregunta, no dudes en contactar al staff.
¡Esperamos que disfrutes tu estancia!
```

### Imágenes de Bienvenida
```
/welcome_image
```

**Opciones de Personalización**:
- **Plantilla**: Diferentes diseños predefinidos
- **Colores**: Esquema de colores personalizado
- **Fondo**: Imagen de fondo personalizada
- **Texto**: Posición y estilo del texto
- **Avatar**: Tamaño y forma del avatar

**Estilos Disponibles**:
1. **Minimalista**: Diseño limpio y simple
2. **Moderno**: Estilo contemporáneo con efectos
3. **Temático**: Basado en el tema del servidor
4. **Animado**: Con elementos animados (GIF)
5. **Personalizado**: Diseño totalmente a medida

## 🔧 Configuración Avanzada

### Roles Automáticos
```
/welcome_autorole
```

**Configuraciones**:
- **Roles Iniciales**: Roles asignados al unirse
- **Roles por Verificación**: Tras completar verificación
- **Roles Temporales**: Roles de "nuevo miembro"
- **Roles por Plataforma**: Diferentes según dispositivo
- **Excepciones**: Usuarios que no reciben roles

### Mensajes Temporales
```
/welcome_temp
```

**Opciones**:
- **Duración**: Tiempo antes de eliminar el mensaje
- **Canales**: Dónde aplicar mensajes temporales
- **Tipos**: Qué mensajes son temporales
- **Excepciones**: Mensajes que no se eliminan

### Notificaciones de Salida
```
/goodbye_setup
```

**Configuraciones**:
- **Canal de Despedidas**: Dónde enviar mensajes
- **Formato**: Texto, embed o desactivado
- **Contenido**: Mensaje personalizado
- **Razón**: Mostrar razón de salida (kick, ban, voluntario)
- **Estadísticas**: Incluir tiempo en servidor

**Ejemplo de Mensaje de Despedida**:
```
{username} ha abandonado el servidor.
Estuvo con nosotros durante 45 días.
Ahora somos {membercount} miembros.
```

## 📊 Estadísticas de Miembros

### Contador de Miembros
```
/welcome_counter
```

**Opciones de Contador**:
- **Canal de Voz**: Actualización en tiempo real
- **Canal de Texto**: Actualización en nombre/tema
- **Formato**: Personalización del formato
- **Frecuencia**: Cada cuánto actualizar
- **Categorías**: Diferentes contadores (total, online, bots)

**Formatos Disponibles**:
- `Miembros: 1,234`
- `👥 1,234 miembros`
- `Somos 1,234 en la comunidad`
- `1,234 aventureros`
- Formato personalizado

### Gráficos de Crecimiento
```
/welcome_stats
```

**Estadísticas Disponibles**:
- **Crecimiento Diario**: Nuevos miembros por día
- **Retención**: Tasa de permanencia
- **Horas Pico**: Cuando más usuarios se unen
- **Fuentes**: De dónde vienen las invitaciones
- **Proyecciones**: Crecimiento estimado futuro

## 🎨 Personalización Visual

### Temas de Bienvenida
```
/welcome_theme
```

**Temas Predefinidos**:
- **Clásico**: Diseño tradicional
- **Moderno**: Estilo minimalista
- **Colorido**: Con colores vibrantes
- **Oscuro**: Tema oscuro
- **Temático**: Basado en juegos/anime

### Banners Personalizados
```
/welcome_banner
```

**Opciones de Banner**:
- **Subir Imagen**: Banner personalizado
- **Galería**: Seleccionar de plantillas
- **Dimensiones**: Tamaño recomendado 1600x400px
- **Animación**: Soporte para GIFs
- **Texto Superpuesto**: Personalización de texto

### Embeds Personalizados
```
/welcome_embed
```

**Personalización de Embeds**:
- **Colores**: Color principal del embed
- **Título**: Título personalizado
- **Descripción**: Cuerpo del mensaje
- **Campos**: Información adicional
- **Thumbnail**: Imagen pequeña (avatar)
- **Imagen**: Imagen grande
- **Footer**: Texto de pie de página
- **Timestamp**: Mostrar hora

## 🔄 Integración con Otros Sistemas

### Integración con Verificación
```
/welcome_verify
```

**Funciones**:
- Mensaje de bienvenida tras verificación
- Roles automáticos post-verificación
- Acceso a canales específicos
- Estadísticas de verificación
- Tiempo promedio de verificación

### Integración con Niveles
```
/welcome_level
```

**Configuraciones**:
- XP inicial para nuevos miembros
- Bonificación de bienvenida
- Roles por nivel automáticos
- Anuncios de nivel en canal de bienvenida
- Recompensas por primeros días

## 🛠️ Herramientas Adicionales

### Mensajes de Reglas
```
/welcome_rules
```

**Opciones**:
- Envío automático de reglas
- Confirmación de lectura
- Formato personalizado
- Actualizaciones automáticas
- Recordatorios periódicos

### Guía del Servidor
```
/welcome_guide
```

**Contenido de la Guía**:
- Tour por canales importantes
- Comandos esenciales
- Roles y permisos
- Eventos regulares
- Recursos útiles
- Preguntas frecuentes

## 📈 Análisis y Optimización

### Estadísticas de Efectividad
```
/welcome_analytics
```

**Métricas Disponibles**:
- Tasa de retención de nuevos miembros
- Engagement post-bienvenida
- Efectividad de diferentes mensajes
- Comparación con períodos anteriores
- Recomendaciones de mejora

### A/B Testing
```
/welcome_test
```

**Funciones de Testing**:
- Probar diferentes mensajes
- Comparar efectividad
- Rotación automática
- Informes de resultados
- Implementación automática del ganador

## 🆘 Solución de Problemas

### Problemas Comunes

#### "Los mensajes de bienvenida no aparecen"
**Soluciones**:
1. Verificar permisos del bot en el canal
2. Comprobar que el canal existe y es accesible
3. Revisar configuración de privacidad
4. Reiniciar el sistema: `/welcome_reset`

#### "Las imágenes no se generan correctamente"
**Verificaciones**:
1. Comprobar dimensiones de imágenes subidas
2. Verificar formatos soportados (PNG, JPG, GIF)
3. Revisar permisos de archivos adjuntos
4. Probar con otra plantilla

#### "Los roles automáticos no se aplican"
**Posibles Causas**:
- Jerarquía de roles incorrecta
- Permisos insuficientes del bot
- Conflicto con otro bot
- Límite de roles alcanzado

**Soluciones**:
1. Verificar jerarquía de roles
2. Comprobar permisos del bot
3. Desactivar sistemas similares
4. Revisar logs de errores

## 📋 Plantillas y Ejemplos

### Plantillas Predefinidas

#### Servidor de Gaming
```
¡Bienvenido/a {user} a {server}!

🎮 Eres nuestro miembro #{position}
🔥 Canales principales:
#anuncios - Novedades importantes
#chat-general - Conversación principal
#buscar-grupo - Encuentra compañeros

¡Esperamos que disfrutes tu estancia!
```

#### Servidor Comunitario
```
¡Hola {user}! ¡Bienvenido/a a nuestra comunidad!

🌟 Te has unido a una familia de {membercount} miembros
📜 Por favor, lee nuestras #reglas
🏷️ Obtén tus roles en #roles
💬 Preséntate en #presentaciones

¡Estamos felices de tenerte con nosotros!
```

#### Servidor Educativo
```
¡Bienvenido/a {user} a {server}!

📚 Recursos disponibles:
#material-estudio - Documentos y guías
#dudas - Preguntas y respuestas
#eventos - Talleres y seminarios

🧠 ¡Comienza tu viaje de aprendizaje ahora!
```

### Crear Plantillas Personalizadas
```
/welcome_template_create <nombre>
```

**Proceso**:
1. Diseña tu mensaje de bienvenida
2. Guárdalo como plantilla
3. Compártelo con el servidor
4. Úsalo cuando lo necesites

## 📞 Soporte y Recursos

### Recursos de Ayuda
- **[Guía de Configuración Básica](/setup)** - Primeros pasos
- **[Preguntas Frecuentes](/faq)** - Problemas comunes
- **[Servidor de Soporte](/support)** - Ayuda personalizada

### Mejores Prácticas

#### Para Servidores Pequeños (< 100 miembros)
- Mensajes personalizados y cálidos
- Menciones directas a nuevos miembros
- Presentación manual por moderadores
- Enfoque en integración personal

#### Para Servidores Medianos (100-1000 miembros)
- Sistema automatizado pero personalizado
- Guía del servidor completa
- Roles automáticos básicos
- Imágenes de bienvenida temáticas

#### Para Servidores Grandes (> 1000 miembros)
- Sistema completamente automatizado
- Verificación antes de bienvenida completa
- Múltiples canales de introducción
- Estadísticas y análisis de retención

---

**¿Necesitas ayuda configurando tu sistema de bienvenidas?** Nuestro equipo puede ayudarte a crear un sistema personalizado para tu servidor. Únete a nuestro [servidor de soporte](/support) para obtener asistencia especializada.

**¿Tienes ideas para mejorar el sistema de bienvenidas?** ¡Nos encanta recibir feedback! Tus sugerencias podrían convertirse en nuevas funciones en futuras actualizaciones.