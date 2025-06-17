# 🎁 Comandos de Utilidad

Esta sección detalla todos los comandos de utilidad disponibles, incluyendo el sistema de giveaways, IA integrada, sistema de niveles y herramientas útiles para la gestión del servidor.

---

## /giveaway

**Descripción:** Sistema completo de sorteos con múltiples opciones avanzadas.
**Permisos requeridos:** Gestionar Eventos

### Subcomandos

#### crear
Crea un nuevo giveaway con opciones personalizables.

**Sintaxis:**
```
/giveaway crear canal:<#canal> premio:<texto> duracion:<tiempo> [opciones...]
```

**Parámetros obligatorios:**
- `canal` (Canal, requerido): Canal donde se enviará el sorteo
- `premio` (String, requerido): Premio del sorteo
- `duracion` (String, requerido): Duración (ej: 1d, 2h, 30m)

**Parámetros opcionales:**
- `ganadores` (Entero, opcional): Número de ganadores (1-20, por defecto: 1)
- `host` (Usuario, opcional): Usuario anfitrión del sorteo
- `titulo` (String, opcional): Título personalizado
- `descripcion` (String, opcional): Descripción adicional
- `color` (String, opcional): Color del embed (formato hex)
- `imagen` (String, opcional): URL de imagen
- `thumbnail` (String, opcional): URL de thumbnail

**Ejemplos básicos:**
```
# Giveaway simple
/giveaway crear canal:#sorteos premio:"Discord Nitro" duracion:1d

# Giveaway con múltiples ganadores
/giveaway crear canal:#eventos premio:"Steam Gift Card $10" duracion:3d ganadores:3

# Giveaway con host específico
/giveaway crear canal:#sorteos premio:"Genshin Welkin Moon" duracion:12h host:@Moderador
```

**Ejemplos avanzados:**
```
# Giveaway completamente personalizado
/giveaway crear canal:#mega-sorteos premio:"Gaming Setup Completo" duracion:1w ganadores:1 titulo:"🎮 MEGA SORTEO GAMING" descripcion:"Incluye: Teclado mecánico, mouse gaming, headset y mousepad" color:#FF6B6B imagen:https://ejemplo.com/gaming-setup.jpg

# Giveaway temático de Genshin
/giveaway crear canal:#genshin-sorteos premio:"Blessing of the Welkin Moon x3" duracion:2d ganadores:5 titulo:"⚡ Sorteo Semanal Genshin" descripcion:"¡Que tengas suerte en tus deseos!" color:#7C4DFF thumbnail:https://ejemplo.com/genshin-logo.png

# Giveaway de aniversario
/giveaway crear canal:#aniversario premio:"Paquete Premium Discord" duracion:5d ganadores:10 titulo:"🎉 Aniversario del Servidor" descripcion:"Celebramos 1 año juntos con este mega sorteo" color:#FFD700
```

#### terminar
Termina un giveaway antes de tiempo y selecciona ganadores.

**Sintaxis:**
```
/giveaway terminar mensaje-id:<ID>
```

**Ejemplo:**
```
/giveaway terminar mensaje-id:1234567890123456789
```

#### reroll
Vuelve a sortear ganadores de un giveaway terminado.

**Sintaxis:**
```
/giveaway reroll mensaje-id:<ID> [nuevos-ganadores:<número>]
```

**Ejemplos:**
```
# Reroll con el mismo número de ganadores
/giveaway reroll mensaje-id:1234567890123456789

# Reroll con más ganadores
/giveaway reroll mensaje-id:1234567890123456789 nuevos-ganadores:3
```

#### participantes
Muestra la lista de participantes de un giveaway.

**Sintaxis:**
```
/giveaway participantes mensaje-id:<ID>
```

**Ejemplo:**
```
/giveaway participantes mensaje-id:1234567890123456789
```

#### remover
Remueve a un usuario específico de un giveaway.

**Sintaxis:**
```
/giveaway remover mensaje-id:<ID> usuario:<@usuario>
```

**Ejemplo:**
```
/giveaway remover mensaje-id:1234567890123456789 usuario:@UsuarioProblematico
```

#### configurar-roles
Configura multiplicadores de participación por rol.

**Sintaxis:**
```
/giveaway configurar-roles rol:<@rol> multiplicador:<número>
```

**Ejemplos:**
```
# Doble oportunidad para boosters
/giveaway configurar-roles rol:@Server Booster multiplicador:2.0

# Triple oportunidad para VIP
/giveaway configurar-roles rol:@VIP multiplicador:3.0

# Bonus para miembros activos
/giveaway configurar-roles rol:@Activo multiplicador:1.5
```

#### requisitos
Establece requisitos para participar en un giveaway.

**Sintaxis:**
```
/giveaway requisitos mensaje-id:<ID> [nivel-minimo:<número>] [roles-requeridos:<IDs>] [roles-prohibidos:<IDs>]
```

**Parámetros:**
- `nivel-minimo` (Entero, opcional): Nivel mínimo requerido
- `roles-requeridos` (String, opcional): IDs de roles separados por comas
- `roles-prohibidos` (String, opcional): IDs de roles prohibidos

**Ejemplos:**
```
# Requisito de nivel
/giveaway requisitos mensaje-id:1234567890123456789 nivel-minimo:10

# Requisito de roles específicos
/giveaway requisitos mensaje-id:1234567890123456789 roles-requeridos:123456789,987654321

# Excluir roles específicos
/giveaway requisitos mensaje-id:1234567890123456789 roles-prohibidos:555666777

# Combinación de requisitos
/giveaway requisitos mensaje-id:1234567890123456789 nivel-minimo:5 roles-requeridos:123456789 roles-prohibidos:999888777
```

#### cancelar
Cancela un giveaway activo sin seleccionar ganadores.

**Sintaxis:**
```
/giveaway cancelar mensaje-id:<ID>
```

**Ejemplo:**
```
/giveaway cancelar mensaje-id:1234567890123456789
```

#### lista
Muestra todos los giveaways activos del servidor.

**Sintaxis:**
```
/giveaway lista
```

### Casos de Uso Completos

**Sorteo semanal estándar:**
```
# 1. Crear el sorteo
/giveaway crear canal:#sorteos-semanales premio:"Discord Nitro Classic" duracion:7d ganadores:2 titulo:"🎁 Sorteo Semanal" descripcion:"¡Participa reaccionando con 🎉!"

# 2. Configurar bonus para boosters
/giveaway configurar-roles rol:@Server Booster multiplicador:2.0

# 3. Establecer requisitos mínimos
/giveaway requisitos mensaje-id:1234567890123456789 nivel-minimo:5
```

**Evento especial con múltiples premios:**
```
# Sorteo principal
/giveaway crear canal:#evento-especial premio:"Gaming Chair + Setup" duracion:3d ganadores:1 titulo:"🏆 GRAN PREMIO ESPECIAL" color:#FFD700

# Sorteos secundarios
/giveaway crear canal:#evento-especial premio:"Steam Gift Card $25" duracion:3d ganadores:5 titulo:"🎮 Premio Secundario"

/giveaway crear canal:#evento-especial premio:"Discord Nitro" duracion:3d ganadores:10 titulo:"💎 Premio de Consolación"
```

**Sorteo con requisitos estrictos:**
```
# Crear sorteo VIP
/giveaway crear canal:#sorteos-vip premio:"Paquete Premium Completo" duracion:5d ganadores:3 titulo:"👑 Sorteo Exclusivo VIP"

# Configurar multiplicadores
/giveaway configurar-roles rol:@VIP multiplicador:3.0
/giveaway configurar-roles rol:@Donador multiplicador:2.0

# Establecer requisitos estrictos
/giveaway requisitos mensaje-id:1234567890123456789 nivel-minimo:20 roles-requeridos:123456789,987654321
```

---

## /ask

**Descripción:** Interactúa con la IA integrada (Google Gemini) especializada en Genshin Impact.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/ask pregunta:<texto>
```

**Parámetros:**
- `pregunta` (String, requerido): La pregunta que quieres hacer

### Ejemplos por Categoría

**Preguntas sobre Genshin Impact:**
```
# Builds de personajes
/ask pregunta:¿Cuál es la mejor build para Raiden Shogun DPS?

# Estrategias de combate
/ask pregunta:¿Cómo puedo derrotar al Electro Hypostasis fácilmente?

# Artefactos y estadísticas
/ask pregunta:¿Qué estadísticas principales necesito para Hu Tao?

# Equipos y sinergias
/ask pregunta:¿Qué personajes van bien con Kazuha en un equipo?

# Eventos y actualizaciones
/ask pregunta:¿Cuándo sale la próxima actualización de Genshin Impact?
```

**Preguntas generales:**
```
# Información general
/ask pregunta:¿Cuál es la capital de Francia?

# Matemáticas
/ask pregunta:¿Cuánto es 15% de 2400?

# Tecnología
/ask pregunta:¿Qué es Discord y cómo funciona?

# Consejos
/ask pregunta:¿Cómo puedo mejorar mi productividad estudiando?
```

**Preguntas sobre el servidor:**
```
# Reglas y funcionamiento
/ask pregunta:¿Cómo funciona el sistema de niveles en este servidor?

# Comandos del bot
/ask pregunta:¿Cómo puedo crear un giveaway?

# Moderación
/ask pregunta:¿Qué hago si veo a alguien rompiendo las reglas?
```

### Casos de Uso

**Ayuda para nuevos jugadores:**
```
/ask pregunta:Soy nuevo en Genshin Impact, ¿qué personajes debería usar al principio?
```

**Optimización de builds:**
```
/ask pregunta:Tengo a Diluc con Lobo Gravestone, ¿qué artefactos y estadísticas debería priorizar?
```

**Resolución de dudas:**
```
/ask pregunta:¿Por qué mi Ganyu hace poco daño? Tengo artefactos 5 estrellas pero el daño es bajo
```

---

## /tc

**Descripción:** Verificador KQMC (KeqingMains Character) para análisis detallado de builds de Genshin Impact.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/tc uid:<UID>
```

**Parámetros:**
- `uid` (String, requerido): UID de Genshin Impact (9 dígitos)

**Ejemplos:**
```
# Verificar cuenta propia
/tc uid:123456789

# Verificar cuenta de amigo
/tc uid:987654321

# Verificar para ayudar con build
/tc uid:456789123
```

### Información Proporcionada

**Análisis de Personajes:**
- Nivel y ascensión
- Talentos y niveles
- Artefactos equipados
- Estadísticas calculadas
- Calificación de build

**Análisis de Armas:**
- Arma equipada y nivel
- Refinamiento
- Compatibilidad con el personaje

**Recomendaciones:**
- Mejoras sugeridas
- Prioridades de farming
- Optimizaciones de build

### Casos de Uso

**Verificación de progreso:**
```
# Verificar después de farming
/tc uid:123456789
# "Quiero ver si mis nuevos artefactos mejoraron mi build"
```

**Ayuda a otros jugadores:**
```
# En canal de ayuda
/tc uid:987654321
# "Déjame revisar tu build para ayudarte"
```

**Comparación de builds:**
```
# Verificar múltiples cuentas
/tc uid:123456789
/tc uid:987654321
# "Comparemos nuestras builds de Raiden"
```

---

## /rank y /leaderboard

### /rank
**Descripción:** Muestra tu nivel y progreso en el servidor.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/rank [usuario:<@usuario>]
```

**Ejemplos:**
```
# Ver tu propio rank
/rank

# Ver rank de otro usuario
/rank usuario:@Amigo

# Verificar progreso de moderador
/rank usuario:@Moderador
```

### /leaderboard
**Descripción:** Muestra la tabla de clasificación de niveles del servidor.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/leaderboard [cantidad:<número>]
```

**Parámetros:**
- `cantidad` (Entero, opcional): Número de usuarios a mostrar (máximo 8)

**Ejemplos:**
```
# Ver top 5
/leaderboard cantidad:5

# Ver top 8 (máximo)
/leaderboard cantidad:8

# Ver leaderboard por defecto
/leaderboard
```

### Casos de Uso

**Competencia amistosa:**
```
# Verificar posición en competencia
/leaderboard cantidad:8
/rank usuario:@Competidor
```

**Motivación de comunidad:**
```
# Mostrar progreso personal
/rank
# "¡Subí 3 niveles esta semana!"
```

**Reconocimiento de miembros activos:**
```
# Ver quiénes son los más activos
/leaderboard cantidad:5
```

---

## /avatar

**Descripción:** Muestra el avatar de un usuario en alta resolución.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/avatar [usuario:<@usuario>]
```

**Ejemplos:**
```
# Ver tu propio avatar
/avatar

# Ver avatar de otro usuario
/avatar usuario:@Amigo

# Ver avatar de moderador
/avatar usuario:@Moderador
```

### Casos de Uso

**Obtener imagen de perfil:**
```
# Para usar en otros lugares
/avatar usuario:@Usuario
```

**Verificar cambios:**
```
# Después de cambiar avatar
/avatar
# "¿Se ve bien mi nuevo avatar?"
```

---

## /latex

**Descripción:** Renderiza fórmulas matemáticas en formato LaTeX.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/latex formula:<texto>
```

**Ejemplos básicos:**
```
# Fórmula famosa
/latex formula:E = mc^2

# Ecuación cuadrática
/latex formula:x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}

# Integral
/latex formula:\int_{0}^{\infty} e^{-x} dx = 1

# Sumatoria
/latex formula:\sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}
```

**Ejemplos avanzados:**
```
# Matriz
/latex formula:\begin{pmatrix} a & b \\ c & d \end{pmatrix}

# Sistema de ecuaciones
/latex formula:\begin{cases} x + y = 5 \\ 2x - y = 1 \end{cases}

# Límite
/latex formula:\lim_{x \to \infty} \frac{1}{x} = 0

# Derivada
/latex formula:\frac{d}{dx}(x^n) = nx^{n-1}
```

### Casos de Uso

**Ayuda con tareas:**
```
# Mostrar fórmula para explicar
/latex formula:\frac{d}{dx}(\sin x) = \cos x
```

**Discusiones académicas:**
```
# En canal de matemáticas
/latex formula:\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
```

**Cálculos de daño en juegos:**
```
# Fórmula de daño
/latex formula:Damage = ATK \times (1 + CritRate \times CritDMG) \times Multiplier
```

---

## /ping

**Descripción:** Muestra la latencia del bot y la API de Discord.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/ping
```

**Información mostrada:**
- Latencia del bot (tiempo de respuesta)
- Latencia de la API de Discord
- Estado de conexión
- Tiempo de actividad

### Casos de Uso

**Verificar estado del bot:**
```
/ping
# "¿El bot está funcionando bien?"
```

**Diagnóstico de problemas:**
```
/ping
# "El bot responde lento, veamos la latencia"
```

**Verificación rutinaria:**
```
/ping
# Verificación diaria del estado
```

---

## /embed

**Descripción:** Crea embeds personalizados para anuncios y mensajes especiales.
**Permisos requeridos:** Gestionar Mensajes

**Funcionalidad:**
Este comando abre un constructor interactivo de embeds donde puedes:
- Configurar título y descripción
- Añadir campos personalizados
- Establecer colores
- Añadir imágenes y thumbnails
- Configurar footer y timestamp

**Sintaxis:**
```
/embed
```

### Casos de Uso

**Anuncios oficiales:**
```
# Crear embed para anuncio importante
/embed
# Configurar: Título "📢 Anuncio Importante", color azul, descripción del anuncio
```

**Reglas del servidor:**
```
# Crear embed de reglas
/embed
# Configurar: Título "📋 Reglas del Servidor", campos para cada regla
```

**Información de eventos:**
```
# Crear embed de evento
/embed
# Configurar: Título "🎉 Evento Especial", imagen del evento, campos con detalles
```

---

## /error

**Descripción:** Comando de prueba para el sistema AntiCrash.
**Permisos requeridos:** Desarrollador

**Funcionalidad:**
Este comando está diseñado para:
- Probar el sistema de manejo de errores
- Verificar que el bot no se crashee
- Diagnosticar problemas del sistema

**Sintaxis:**
```
/error
```

**⚠️ Advertencia:** Este comando solo debe ser usado por desarrolladores para pruebas.

---

## Consejos de Uso

### Optimización del Sistema de Giveaways

**Planificación de sorteos:**
1. **Frecuencia:** No más de 2-3 giveaways activos simultáneamente
2. **Duración:** 1-7 días dependiendo del premio
3. **Premios:** Variados para mantener interés

**Configuración de multiplicadores:**
```
# Estructura recomendada
@Server Booster: x2.0
@VIP: x1.8
@Activo: x1.5
@Donador: x1.3
```

**Requisitos balanceados:**
```
# Para premios pequeños
nivel-minimo: 3

# Para premios medianos
nivel-minimo: 10

# Para premios grandes
nivel-minimo: 20 + roles específicos
```

### Uso Efectivo de la IA

**Preguntas específicas obtienen mejores respuestas:**
```
# ❌ Vago
/ask pregunta:¿Cómo jugar Genshin?

# ✅ Específico
/ask pregunta:¿Qué artefactos necesita Ganyu para build de DPS principal?
```

**Contexto ayuda:**
```
# ✅ Con contexto
/ask pregunta:Tengo a Diluc nivel 80 con Lobo Gravestone R1, ¿qué artefactos debería usar para maximizar su daño?
```

### Gestión del Sistema de Niveles

**Monitoreo regular:**
```
# Verificar progreso semanal
/leaderboard cantidad:8

# Reconocer miembros activos
/rank usuario:@MiembroActivo
```

**Motivación de la comunidad:**
- Celebra subidas de nivel importantes
- Reconoce públicamente a miembros del top
- Usa el sistema para eventos especiales

---

> **Nota:** Los comandos de utilidad están diseñados para mejorar la experiencia de la comunidad. Úsalos de manera consistente y estratégica para mantener el engagement y la participación activa de los miembros.