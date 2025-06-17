# 🖼️ Comandos de Imagen

Esta sección detalla todos los comandos de procesamiento y mejora de imágenes, incluyendo ampliación con IA, eliminación de marcas de agua y herramientas avanzadas de edición.

---

## /imglarge

**Descripción:** Amplía y mejora la resolución de imágenes usando inteligencia artificial.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/imglarge imagen:<archivo o URL> [escala:<factor>] [modelo:<tipo>]
```

**Parámetros:**
- `imagen` (Archivo/URL, requerido): Imagen a procesar (archivo adjunto o URL)
- `escala` (Entero, opcional): Factor de ampliación (2x, 4x, 8x - por defecto: 4x)
- `modelo` (String, opcional): Tipo de modelo de IA a usar
  - `general` - Para imágenes generales (por defecto)
  - `anime` - Optimizado para arte anime/manga
  - `photo` - Optimizado para fotografías
  - `art` - Optimizado para arte digital

### Tipos de Imágenes Soportadas

**Formatos aceptados:**
- JPG/JPEG
- PNG
- WEBP
- BMP
- GIF (solo primer frame)

**Limitaciones:**
- Tamaño máximo: 10MB
- Resolución máxima de entrada: 2048x2048
- Resolución máxima de salida: 8192x8192

### Ejemplos por Tipo de Imagen

**Fotografías:**
```
# Foto de perfil de baja resolución
/imglarge imagen:[adjuntar foto] escala:4 modelo:photo

# Foto antigua o escaneada
/imglarge imagen:https://ejemplo.com/foto-antigua.jpg escala:2 modelo:photo

# Selfie pixelada
/imglarge imagen:[adjuntar selfie] escala:4 modelo:photo
```

**Arte Anime/Manga:**
```
# Avatar de anime de baja resolución
/imglarge imagen:[adjuntar avatar] escala:4 modelo:anime

# Fanart pixelado
/imglarge imagen:https://ejemplo.com/fanart.png escala:8 modelo:anime

# Imagen de perfil de personaje
/imglarge imagen:[adjuntar imagen] escala:2 modelo:anime
```

**Arte Digital:**
```
# Ilustración de baja calidad
/imglarge imagen:[adjuntar arte] escala:4 modelo:art

# Logo o icono pequeño
/imglarge imagen:https://ejemplo.com/logo.png escala:8 modelo:art

# Concept art pixelado
/imglarge imagen:[adjuntar concept] escala:2 modelo:art
```

**Imágenes Generales:**
```
# Meme de baja resolución
/imglarge imagen:[adjuntar meme] escala:4 modelo:general

# Captura de pantalla pixelada
/imglarge imagen:https://ejemplo.com/screenshot.jpg escala:2 modelo:general

# Imagen de juego retro
/imglarge imagen:[adjuntar retro] escala:8 modelo:general
```

### Casos de Uso Específicos

**Mejora de avatares:**
```
# Avatar de Discord pixelado
/imglarge imagen:[adjuntar avatar] escala:4 modelo:anime
# Resultado: Avatar nítido para usar como perfil

# Foto de perfil antigua
/imglarge imagen:[adjuntar foto] escala:2 modelo:photo
# Resultado: Foto mejorada para redes sociales
```

**Restauración de imágenes:**
```
# Foto familiar antigua
/imglarge imagen:[adjuntar foto-antigua] escala:2 modelo:photo
# Resultado: Foto restaurada con mejor calidad

# Artwork vintage
/imglarge imagen:[adjuntar artwork] escala:4 modelo:art
# Resultado: Arte digitalizado mejorado
```

**Preparación para impresión:**
```
# Imagen para poster
/imglarge imagen:[adjuntar imagen] escala:8 modelo:general
# Resultado: Resolución suficiente para impresión grande

# Logo para merchandising
/imglarge imagen:[adjuntar logo] escala:4 modelo:art
# Resultado: Logo vectorizado de alta calidad
```

**Gaming y entretenimiento:**
```
# Sprite de juego retro
/imglarge imagen:[adjuntar sprite] escala:8 modelo:general
# Resultado: Sprite HD para modding

# Fanart de personaje
/imglarge imagen:[adjuntar fanart] escala:4 modelo:anime
# Resultado: Fanart mejorado para wallpaper
```

### Comparación de Modelos

**Modelo General:**
- **Mejor para:** Memes, capturas, imágenes mixtas
- **Características:** Balanceado, preserva detalles generales
- **Tiempo de procesamiento:** Rápido (30-60 segundos)

**Modelo Anime:**
- **Mejor para:** Arte anime, manga, personajes 2D
- **Características:** Preserva líneas limpias, colores vibrantes
- **Tiempo de procesamiento:** Medio (45-90 segundos)

**Modelo Photo:**
- **Mejor para:** Fotografías reales, retratos, paisajes
- **Características:** Mejora texturas naturales, reduce ruido
- **Tiempo de procesamiento:** Lento (60-120 segundos)

**Modelo Art:**
- **Mejor para:** Arte digital, ilustraciones, logos
- **Características:** Preserva detalles artísticos, mejora gradientes
- **Tiempo de procesamiento:** Medio (45-90 segundos)

### Factores de Escala

**2x (Conservador):**
```
/imglarge imagen:[imagen] escala:2
# Mejora sutil, procesamiento rápido
# Ideal para: Imágenes ya decentes que necesitan pequeña mejora
```

**4x (Estándar):**
```
/imglarge imagen:[imagen] escala:4
# Mejora significativa, balance calidad/tiempo
# Ideal para: La mayoría de casos de uso
```

**8x (Máximo):**
```
/imglarge imagen:[imagen] escala:8
# Mejora dramática, procesamiento lento
# Ideal para: Imágenes muy pequeñas o para impresión
```

---

## /watermark

**Descripción:** Elimina marcas de agua de imágenes usando IA avanzada.
**Permisos requeridos:** Ninguno
**Canales permitidos:** Configurables por administrador

**Sintaxis:**
```
/watermark imagen:<archivo o URL> [intensidad:<nivel>]
```

**Parámetros:**
- `imagen` (Archivo/URL, requerido): Imagen con marca de agua
- `intensidad` (String, opcional): Nivel de procesamiento
  - `suave` - Eliminación conservadora
  - `normal` - Eliminación estándar (por defecto)
  - `agresiva` - Eliminación intensiva

### Tipos de Marcas de Agua

**Marcas de agua de texto:**
```
# Texto semitransparente
/watermark imagen:[adjuntar imagen] intensidad:normal

# Texto en esquinas
/watermark imagen:https://ejemplo.com/imagen-texto.jpg intensidad:suave

# Texto repetido
/watermark imagen:[adjuntar imagen] intensidad:agresiva
```

**Marcas de agua de logo:**
```
# Logo en esquina
/watermark imagen:[adjuntar imagen] intensidad:normal

# Logo centrado
/watermark imagen:https://ejemplo.com/logo-centro.png intensidad:agresiva

# Logo semitransparente
/watermark imagen:[adjuntar imagen] intensidad:suave
```

**Marcas de agua complejas:**
```
# Múltiples elementos
/watermark imagen:[adjuntar imagen] intensidad:agresiva

# Patrones repetitivos
/watermark imagen:https://ejemplo.com/patron.jpg intensidad:normal

# Marcas integradas
/watermark imagen:[adjuntar imagen] intensidad:normal
```

### Niveles de Intensidad

**Suave:**
```
/watermark imagen:[imagen] intensidad:suave
# Características:
# - Eliminación conservadora
# - Preserva máximo detalle de la imagen original
# - Mejor para marcas de agua sutiles
# - Menor riesgo de artefactos
# - Tiempo de procesamiento: 30-45 segundos
```

**Normal:**
```
/watermark imagen:[imagen] intensidad:normal
# Características:
# - Balance entre eliminación y preservación
# - Efectivo para la mayoría de marcas de agua
# - Resultado natural en la mayoría de casos
# - Tiempo de procesamiento: 45-60 segundos
```

**Agresiva:**
```
/watermark imagen:[imagen] intensidad:agresiva
# Características:
# - Eliminación intensiva
# - Efectivo para marcas de agua persistentes
# - Mayor riesgo de artefactos
# - Puede afectar detalles de la imagen
# - Tiempo de procesamiento: 60-90 segundos
```

### Casos de Uso Específicos

**Imágenes de stock:**
```
# Imagen de stock con marca de agua
/watermark imagen:https://stock-site.com/imagen-watermark.jpg intensidad:normal
# Resultado: Imagen limpia para uso personal
```

**Capturas de pantalla:**
```
# Screenshot con logo de app
/watermark imagen:[adjuntar screenshot] intensidad:suave
# Resultado: Captura limpia para tutorial
```

**Memes y contenido social:**
```
# Meme con marca de agua
/watermark imagen:[adjuntar meme] intensidad:normal
# Resultado: Meme limpio para compartir
```

**Imágenes de productos:**
```
# Foto de producto con marca
/watermark imagen:https://tienda.com/producto-marca.jpg intensidad:agresiva
# Resultado: Imagen limpia para referencia
```

### Limitaciones y Consideraciones

**Limitaciones técnicas:**
- Tamaño máximo: 15MB
- Resolución máxima: 4096x4096
- Formatos: JPG, PNG, WEBP
- No funciona con GIFs animados

**Consideraciones éticas:**
- ⚠️ **Uso responsable:** Solo para uso personal o educativo
- ⚠️ **Respeto de derechos:** No violar derechos de autor
- ⚠️ **Términos de servicio:** Respetar términos de las plataformas

**Calidad del resultado:**
- Depende de la complejidad de la marca de agua
- Marcas simples = mejores resultados
- Marcas integradas = resultados variables
- Múltiples marcas = mayor dificultad

---

## /avatar-enhance

**Descripción:** Mejora específicamente avatares y fotos de perfil.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/avatar-enhance imagen:<archivo o URL> [estilo:<tipo>]
```

**Parámetros:**
- `imagen` (Archivo/URL, requerido): Avatar o foto de perfil
- `estilo` (String, opcional): Estilo de mejora
  - `natural` - Mejora realista (por defecto)
  - `anime` - Estilo anime/cartoon
  - `artistic` - Estilo artístico
  - `professional` - Estilo profesional

### Estilos de Mejora

**Natural:**
```
# Foto de perfil real
/avatar-enhance imagen:[adjuntar foto] estilo:natural
# Resultado: Foto mejorada manteniendo realismo

# Selfie de baja calidad
/avatar-enhance imagen:https://ejemplo.com/selfie.jpg estilo:natural
# Resultado: Selfie nítido y natural
```

**Anime:**
```
# Avatar de anime pixelado
/avatar-enhance imagen:[adjuntar avatar] estilo:anime
# Resultado: Avatar anime de alta calidad

# Fanart de personaje
/avatar-enhance imagen:https://ejemplo.com/personaje.png estilo:anime
# Resultado: Personaje mejorado estilo anime
```

**Artistic:**
```
# Retrato artístico
/avatar-enhance imagen:[adjuntar retrato] estilo:artistic
# Resultado: Retrato con mejoras artísticas

# Ilustración de perfil
/avatar-enhance imagen:https://ejemplo.com/ilustracion.jpg estilo:artistic
# Resultado: Ilustración refinada
```

**Professional:**
```
# Foto de LinkedIn
/avatar-enhance imagen:[adjuntar foto-profesional] estilo:professional
# Resultado: Foto profesional mejorada

# Headshot corporativo
/avatar-enhance imagen:https://ejemplo.com/headshot.jpg estilo:professional
# Resultado: Imagen corporativa de calidad
```

### Casos de Uso por Plataforma

**Discord:**
```
# Avatar de Discord de 128x128
/avatar-enhance imagen:[adjuntar avatar] estilo:anime
# Resultado: Avatar 512x512 o superior
```

**Redes sociales:**
```
# Foto de perfil de Instagram
/avatar-enhance imagen:[adjuntar foto] estilo:natural
# Resultado: Foto optimizada para redes
```

**Plataformas profesionales:**
```
# Foto de LinkedIn
/avatar-enhance imagen:[adjuntar foto] estilo:professional
# Resultado: Imagen profesional de alta calidad
```

**Gaming:**
```
# Avatar de juego
/avatar-enhance imagen:[adjuntar avatar-juego] estilo:artistic
# Resultado: Avatar gaming mejorado
```

---

## Flujos de Trabajo Completos

### Mejora Completa de Avatar

```
# Paso 1: Ampliar resolución
/imglarge imagen:[avatar-pequeño] escala:4 modelo:anime

# Paso 2: Mejorar calidad específica
/avatar-enhance imagen:[resultado-paso1] estilo:anime

# Resultado: Avatar de máxima calidad
```

### Restauración de Imagen Vintage

```
# Paso 1: Eliminar marcas de agua si las hay
/watermark imagen:[imagen-vintage] intensidad:suave

# Paso 2: Ampliar y mejorar
/imglarge imagen:[resultado-paso1] escala:2 modelo:photo

# Resultado: Imagen vintage restaurada
```

### Preparación para Impresión

```
# Paso 1: Limpiar imagen
/watermark imagen:[imagen-original] intensidad:normal

# Paso 2: Ampliar para impresión
/imglarge imagen:[resultado-paso1] escala:8 modelo:art

# Resultado: Imagen lista para impresión de alta calidad
```

### Optimización para Redes Sociales

```
# Paso 1: Mejorar avatar
/avatar-enhance imagen:[foto-perfil] estilo:natural

# Paso 2: Ajustar si es necesario
/imglarge imagen:[resultado-paso1] escala:2 modelo:photo

# Resultado: Perfil optimizado para redes
```

---

## Configuración y Administración

### Configuración de Canales

**Para `/watermark`:**
```
# Los administradores pueden configurar:
# - Canales permitidos para uso
# - Límites de uso por usuario
# - Restricciones de tamaño
# - Logs de uso para moderación
```

**Configuración AWS (para administradores):**
```
# Configuración de almacenamiento:
# - Bucket de S3 para imágenes temporales
# - Credenciales de acceso
# - Región de procesamiento
# - Políticas de retención
```

### Límites y Restricciones

**Por usuario:**
- Máximo 10 imágenes por hora
- Máximo 50 imágenes por día
- Cooldown de 30 segundos entre comandos

**Por servidor:**
- Máximo 100 procesamiento simultáneos
- Prioridad por roles (boosters, VIP, etc.)
- Logs de uso para moderación

**Técnicos:**
- Timeout de procesamiento: 5 minutos
- Almacenamiento temporal: 24 horas
- Formatos de salida: PNG (alta calidad)

---

## Consejos y Mejores Prácticas

### Optimización de Resultados

**Selección de modelo correcto:**
```
# Para fotos reales
/imglarge imagen:[foto] modelo:photo

# Para arte anime
/imglarge imagen:[anime] modelo:anime

# Para logos/arte digital
/imglarge imagen:[logo] modelo:art

# Para contenido mixto
/imglarge imagen:[mixto] modelo:general
```

**Selección de escala apropiada:**
```
# Imagen muy pequeña (menos de 200px)
/imglarge imagen:[muy-pequeña] escala:8

# Imagen pequeña (200-500px)
/imglarge imagen:[pequeña] escala:4

# Imagen mediana (500-1000px)
/imglarge imagen:[mediana] escala:2
```

### Calidad de Entrada

**Mejores resultados:**
- Imágenes sin compresión excesiva
- Formato PNG cuando sea posible
- Buena iluminación en fotos
- Imágenes sin ruido excesivo

**Evitar:**
- Imágenes muy comprimidas (JPEG de baja calidad)
- Imágenes con mucho ruido
- Capturas de pantalla de baja resolución
- Imágenes con múltiples marcas de agua

### Uso Eficiente

**Planificación:**
```
# 1. Evaluar la imagen original
# 2. Elegir el comando apropiado
# 3. Seleccionar parámetros óptimos
# 4. Procesar en orden lógico
```

**Ahorro de tiempo:**
```
# Usar parámetros por defecto cuando sea apropiado
# No sobre-procesar imágenes ya buenas
# Combinar comandos estratégicamente
```

---

## Solución de Problemas

### Errores Comunes

**"Imagen demasiado grande":**
```
# Solución: Reducir tamaño antes de procesar
# O usar un servicio de compresión online
```

**"Formato no soportado":**
```
# Solución: Convertir a JPG o PNG
# Evitar formatos exóticos
```

**"Procesamiento fallido":**
```
# Solución: Intentar con intensidad menor
# O usar modelo diferente
```

**"Resultado con artefactos":**
```
# Solución: Usar escala menor
# O cambiar modelo de IA
# O usar intensidad suave
```

### Optimización de Calidad

**Si el resultado no es satisfactorio:**
1. Verificar calidad de imagen original
2. Probar modelo diferente
3. Ajustar parámetros de intensidad
4. Considerar pre-procesamiento manual

**Para mejores resultados:**
1. Usar imágenes de la mejor calidad disponible
2. Elegir parámetros apropiados para el tipo de imagen
3. Ser paciente con el procesamiento
4. Experimentar con diferentes configuraciones

---

> **Nota:** Los comandos de imagen utilizan IA avanzada y pueden tomar tiempo en procesar. La calidad del resultado depende significativamente de la calidad de la imagen original y la selección apropiada de parámetros. Usa estas herramientas de manera responsable y respeta los derechos de autor.