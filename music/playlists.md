# 🎵 Gestión de Playlists - Dark-Bot

## 🎯 Sistema de Playlists Avanzado

Dark-Bot incluye un sistema completo de gestión de playlists que te permite crear, organizar y compartir colecciones de música con tu servidor. Desde playlists personales hasta playlists del servidor, tenemos todo lo que necesitas.

## 🚀 Comandos Básicos de Playlists

### Crear Playlist
```
/playlist create <nombre> [descripción]
```

**Ejemplos**:
```
/playlist create "Música Relajante" "Para estudiar y concentrarse"
/playlist create "Rock Clásico" "Los mejores hits del rock"
/playlist create "Fiesta" "Música para animar el ambiente"
```

**Opciones**:
- **Nombre**: Hasta 50 caracteres
- **Descripción**: Hasta 200 caracteres (opcional)
- **Privacidad**: Pública/Privada/Solo servidor
- **Colaborativa**: Permitir que otros añadan canciones

### Listar Playlists
```
/playlist list [usuario]
```

**Filtros Disponibles**:
- **Mis Playlists**: Solo tus playlists
- **Playlists del Servidor**: Playlists públicas del servidor
- **Playlists Favoritas**: Playlists que has marcado como favoritas
- **Playlists Recientes**: Últimas playlists reproducidas

### Información de Playlist
```
/playlist info <nombre>
```

**Información Mostrada**:
- Nombre y descripción
- Creador y fecha de creación
- Número total de canciones
- Duración total
- Última actualización
- Configuración de privacidad
- Estadísticas de reproducción

## 🎶 Gestión de Canciones

### Añadir Canciones
```
/playlist add <playlist> <canción/url>
```

**Métodos de Añadir**:
- **URL Directa**: YouTube, Spotify, SoundCloud
- **Búsqueda**: Buscar por nombre y artista
- **Canción Actual**: Añadir lo que se está reproduciendo
- **Desde Otra Playlist**: Copiar canciones entre playlists

**Ejemplos**:
```
/playlist add "Rock Clásico" "Bohemian Rhapsody Queen"
/playlist add "Fiesta" https://youtu.be/dQw4w9WgXcQ
/playlist add "Favoritas" --current
```

### Remover Canciones
```
/playlist remove <playlist> <posición/nombre>
```

**Métodos de Remoción**:
- **Por Posición**: Número en la playlist
- **Por Nombre**: Nombre exacto de la canción
- **Por Rango**: Remover múltiples canciones
- **Por Artista**: Remover todas las canciones de un artista

**Ejemplos**:
```
/playlist remove "Rock Clásico" 5
/playlist remove "Fiesta" "Never Gonna Give You Up"
/playlist remove "Favoritas" 1-5
```

### Mover Canciones
```
/playlist move <playlist> <posición_actual> <nueva_posición>
```

**Funciones de Organización**:
- Cambiar orden de canciones
- Mover al inicio/final
- Intercambiar posiciones
- Ordenar alfabéticamente
- Ordenar por duración
- Mezclar aleatoriamente

## 📋 Tipos de Playlists

### Playlists Personales
```
/playlist create <nombre> --private
```

**Características**:
- Solo visibles para el creador
- Control total sobre contenido
- Pueden hacerse públicas después
- Límite de 50 playlists por usuario
- Hasta 500 canciones por playlist

### Playlists del Servidor
```
/playlist create <nombre> --server
```

**Características**:
- Visibles para todos en el servidor
- Pueden ser editadas por moderadores
- Aparecen en la lista pública
- Límite de 20 playlists por servidor
- Hasta 1000 canciones por playlist

### Playlists Colaborativas
```
/playlist create <nombre> --collaborative
```

**Funciones**:
- Múltiples usuarios pueden añadir canciones
- Sistema de votación para remover canciones
- Moderación automática de contenido
- Logs de cambios
- Límites por usuario

### Playlists Automáticas
```
/playlist auto create <tipo> <criterios>
```

**Tipos Disponibles**:
- **Top Reproducidas**: Canciones más reproducidas del servidor
- **Recientes**: Últimas canciones reproducidas
- **Por Género**: Canciones de un género específico
- **Por Artista**: Todas las canciones de artistas favoritos
- **Por Época**: Música de una década específica

## 🎵 Reproducción de Playlists

### Reproducir Playlist
```
/play playlist <nombre>
```

**Opciones de Reproducción**:
- **Orden Normal**: Reproducir en orden
- **Aleatorio**: Mezclar canciones
- **Repetir**: Repetir toda la playlist
- **Repetir Una**: Repetir canción actual
- **Continuar**: Continuar donde se dejó

### Modos de Reproducción
```
/playlist mode <playlist> <modo>
```

**Modos Disponibles**:
- **Sequential**: Orden original
- **Shuffle**: Orden aleatorio
- **Smart Shuffle**: Aleatorio inteligente (evita repeticiones)
- **Radio**: Modo radio (añade canciones similares)
- **Discovery**: Descubrimiento (mezcla conocidas y nuevas)

### Cola de Playlists
```
/queue playlist <nombre> [posición]
```

**Funciones**:
- Añadir playlist completa a la cola
- Insertar en posición específica
- Añadir al final de la cola actual
- Reemplazar cola actual
- Mezclar con cola existente

## 🔧 Configuración Avanzada

### Configuración de Playlist
```
/playlist config <nombre>
```

**Opciones Configurables**:
- **Privacidad**: Pública/Privada/Solo servidor
- **Colaboración**: Permitir edición por otros
- **Auto-actualización**: Actualizar automáticamente
- **Filtros**: Filtrar contenido explícito
- **Límites**: Límites de duración y cantidad

### Permisos de Playlist
```
/playlist permissions <nombre>
```

**Niveles de Permisos**:
- **Propietario**: Control total
- **Editor**: Añadir/remover canciones
- **Colaborador**: Solo añadir canciones
- **Visualizador**: Solo ver y reproducir
- **Bloqueado**: Sin acceso

### Moderación de Playlists
```
/playlist moderate <nombre>
```

**Herramientas de Moderación**:
- Revisar canciones reportadas
- Remover contenido inapropiado
- Aplicar filtros automáticos
- Gestionar reportes de usuarios
- Configurar auto-moderación

## 📊 Estadísticas y Análisis

### Estadísticas de Playlist
```
/playlist stats <nombre>
```

**Métricas Incluidas**:
- Total de reproducciones
- Canciones más populares
- Tiempo total reproducido
- Usuarios únicos que la han reproducido
- Tendencias de reproducción
- Comparación con otras playlists

### Análisis de Contenido
```
/playlist analyze <nombre>
```

**Análisis Disponibles**:
- **Géneros**: Distribución por géneros
- **Artistas**: Artistas más frecuentes
- **Décadas**: Distribución temporal
- **Duración**: Análisis de duración de canciones
- **Popularidad**: Nivel de popularidad promedio
- **Energía**: Nivel de energía de las canciones

### Recomendaciones
```
/playlist recommend <nombre>
```

**Tipos de Recomendaciones**:
- Canciones similares para añadir
- Playlists relacionadas
- Artistas que podrían gustar
- Géneros para explorar
- Canciones trending relacionadas

## 🔄 Importación y Exportación

### Importar Playlists
```
/playlist import <plataforma> <url/archivo>
```

**Plataformas Soportadas**:
- **Spotify**: Playlists públicas y propias
- **YouTube**: Playlists y videos guardados
- **Apple Music**: Con archivo de exportación
- **SoundCloud**: Playlists públicas
- **Archivo M3U**: Formato estándar
- **Archivo JSON**: Formato de Dark-Bot

**Proceso de Importación**:
1. Proporcionar URL o archivo
2. Verificar canciones disponibles
3. Resolver canciones no encontradas
4. Crear playlist importada
5. Revisar y ajustar

### Exportar Playlists
```
/playlist export <nombre> <formato>
```

**Formatos de Exportación**:
- **M3U**: Compatible con reproductores
- **JSON**: Formato completo con metadatos
- **TXT**: Lista simple de canciones
- **CSV**: Para análisis en hojas de cálculo
- **Spotify**: Crear playlist en Spotify

### Sincronización
```
/playlist sync <nombre> <plataforma>
```

**Funciones de Sincronización**:
- Mantener playlist actualizada con original
- Sincronización bidireccional
- Resolución de conflictos
- Programar sincronización automática
- Notificaciones de cambios

## 🎨 Personalización

### Temas de Playlist
```
/playlist theme <nombre> <tema>
```

**Temas Disponibles**:
- **Clásico**: Diseño tradicional
- **Moderno**: Diseño minimalista
- **Colorido**: Con colores vibrantes
- **Oscuro**: Tema oscuro
- **Personalizado**: Colores personalizados

### Portadas de Playlist
```
/playlist cover <nombre> <imagen/url>
```

**Opciones de Portada**:
- Subir imagen personalizada
- Usar portada de canción
- Generar automáticamente
- Seleccionar de galería
- Crear collage de portadas

### Descripciones Enriquecidas
```
/playlist description <nombre> <descripción>
```

**Funciones de Descripción**:
- Texto enriquecido con markdown
- Enlaces a redes sociales
- Información del creador
- Historia de la playlist
- Créditos y colaboradores

## 🔍 Búsqueda y Descubrimiento

### Búsqueda de Playlists
```
/playlist search <términos>
```

**Filtros de Búsqueda**:
- **Por Nombre**: Buscar en nombres de playlists
- **Por Descripción**: Buscar en descripciones
- **Por Creador**: Playlists de usuario específico
- **Por Género**: Playlists de género musical
- **Por Popularidad**: Ordenar por reproducciones

### Explorar Playlists
```
/playlist explore [categoría]
```

**Categorías de Exploración**:
- **Trending**: Playlists más populares
- **Nuevas**: Playlists recién creadas
- **Recomendadas**: Basadas en tu historial
- **Por Género**: Explorar por género musical
- **Colaborativas**: Playlists abiertas a colaboración

### Playlists Destacadas
```
/playlist featured
```

**Criterios para Destacar**:
- Alta calidad de contenido
- Buena organización
- Popularidad en el servidor
- Originalidad y creatividad
- Actualizaciones regulares

## 🏆 Sistema de Logros

### Logros de Playlists
```
/playlist achievements
```

**Logros Disponibles**:
- **Curador**: Crear 10 playlists
- **Popular**: Playlist con 100+ reproducciones
- **Colaborativo**: Participar en 5 playlists colaborativas
- **Diverso**: Playlist con 10+ géneros diferentes
- **Maratonista**: Playlist de 24+ horas
- **Descubridor**: Añadir 50+ canciones únicas

### Insignias Especiales
```
/playlist badges
```

**Tipos de Insignias**:
- **Playlist del Mes**: Mejor playlist mensual
- **Innovador**: Uso creativo de funciones
- **Mentor**: Ayudar a otros con playlists
- **Veterano**: Usuario de larga data
- **Especialista**: Experto en género específico

## 🔧 Herramientas de Gestión

### Limpieza de Playlists
```
/playlist cleanup <nombre>
```

**Funciones de Limpieza**:
- Remover canciones no disponibles
- Eliminar duplicados
- Corregir metadatos
- Reorganizar automáticamente
- Optimizar para reproducción

### Backup de Playlists
```
/playlist backup [nombre]
```

**Opciones de Backup**:
- Backup individual
- Backup de todas las playlists
- Backup automático programado
- Restaurar desde backup
- Historial de versiones

### Fusión de Playlists
```
/playlist merge <playlist1> <playlist2> <nombre_nueva>
```

**Opciones de Fusión**:
- Combinar manteniendo orden
- Mezclar aleatoriamente
- Eliminar duplicados
- Mantener metadatos
- Crear nueva o sobrescribir

## 📱 Integración con Plataformas

### Spotify Integration
```
/playlist spotify connect
```

**Funciones con Spotify**:
- Importar playlists de Spotify
- Exportar a Spotify
- Sincronización automática
- Buscar en catálogo de Spotify
- Recomendaciones de Spotify

### YouTube Integration
```
/playlist youtube connect
```

**Funciones con YouTube**:
- Importar playlists de YouTube
- Buscar videos en YouTube
- Crear playlists de YouTube
- Sincronizar con YouTube Music
- Acceso a YouTube Premium

### SoundCloud Integration
```
/playlist soundcloud connect
```

**Funciones con SoundCloud**:
- Importar playlists públicas
- Descubrir música independiente
- Seguir artistas en SoundCloud
- Acceder a tracks exclusivos
- Integración con SoundCloud Go+

## 🆘 Solución de Problemas

### Problemas Comunes

#### "No puedo reproducir mi playlist"
**Soluciones**:
1. Verificar que la playlist existe: `/playlist info <nombre>`
2. Comprobar permisos: `/playlist permissions <nombre>`
3. Revisar si hay canciones disponibles
4. Intentar reproducir canciones individuales

#### "Canciones desaparecen de la playlist"
**Posibles Causas**:
- Videos eliminados de YouTube
- Canciones removidas de Spotify
- Problemas de derechos de autor
- Limpieza automática activada

**Soluciones**:
1. Activar notificaciones de cambios
2. Hacer backups regulares
3. Usar múltiples fuentes para canciones
4. Revisar configuración de auto-limpieza

#### "No puedo importar playlist"
**Verificaciones**:
1. URL correcta y accesible
2. Playlist pública (si es externa)
3. Formato de archivo correcto
4. Límites de importación no excedidos

### Limitaciones Conocidas

#### Límites de Playlists
- **Usuarios Gratuitos**: 10 playlists, 100 canciones cada una
- **Usuarios Premium**: 50 playlists, 500 canciones cada una
- **Servidores**: 20 playlists públicas, 1000 canciones cada una

#### Restricciones de Contenido
- Algunas canciones pueden no estar disponibles por región
- Contenido con derechos de autor puede ser limitado
- Canciones explícitas filtradas según configuración del servidor

## 📞 Soporte y Recursos

### Recursos de Ayuda
- **[Guía de Música Básica](/music/)** - Introducción al sistema
- **[Comandos de Música](/music/commands)** - Lista completa de comandos
- **[Configuración de Música](/music/setup)** - Configuración inicial
- **[Solución de Problemas](/music/troubleshooting)** - Problemas comunes
- **[Servidor de Soporte](/support)** - Ayuda personalizada

### Consejos para Mejores Playlists

#### Organización
- Usa nombres descriptivos y únicos
- Añade descripciones detalladas
- Organiza canciones por flujo o tema
- Mantén un equilibrio en géneros y energía

#### Colaboración
- Establece reglas claras para playlists colaborativas
- Modera contenido regularmente
- Fomenta la participación de la comunidad
- Reconoce contribuciones valiosas

#### Mantenimiento
- Revisa playlists regularmente
- Actualiza con nueva música
- Remueve canciones que ya no funcionan
- Haz backups de playlists importantes

---

**¿Quieres crear la playlist perfecta?** Nuestro equipo puede ayudarte a organizar y optimizar tus playlists. Únete a nuestro [servidor de soporte](/support) para obtener consejos personalizados y acceso a funciones exclusivas.

**¿Tienes ideas para nuevas funciones de playlists?** ¡Nos encanta escuchar sugerencias de la comunidad! Comparte tus ideas y podrían aparecer en futuras actualizaciones del sistema de playlists.