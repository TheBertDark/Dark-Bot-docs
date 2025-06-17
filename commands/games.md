# 🎮 Comandos de Juegos

Esta sección detalla los comandos relacionados con juegos, incluyendo códigos de canje para diversos juegos y mini-juegos interactivos para la comunidad.

---

## /codes

**Descripción:** Sistema de códigos de canje para múltiples juegos populares.
**Permisos requeridos:** Gestionar Mensajes

**Sintaxis:**
```
/codes juego:<nombre> códigos:<lista> [imagen:<URL>]
```

**Parámetros:**
- `juego` (String, requerido): Nombre del juego
- `códigos` (String, requerido): Lista de códigos separados por comas o saltos de línea
- `imagen` (String, opcional): URL de imagen relacionada con los códigos

### Juegos Soportados

**Genshin Impact:**
```
# Códigos de evento
/codes juego:"Genshin Impact" códigos:"GENSHINGIFT, 8ANCKTWYVRD5, NTPVU7JTJYPD" imagen:https://ejemplo.com/genshin-codes.jpg

# Códigos de livestream
/codes juego:"Genshin Impact" códigos:"3TPUKSV8C5X9, DTNUKTWCC6D9, LANVJSFUD6CM"

# Códigos de aniversario
/codes juego:"Genshin Impact" códigos:"ANNIVERSARY2024, CELEBRATION3RD, THANKYOU2024"
```

**Honkai: Star Rail:**
```
# Códigos de actualización
/codes juego:"Honkai Star Rail" códigos:"STARRAILGIFT, TRAILBLAZE2024, MARCH7THGIFT"

# Códigos de evento especial
/codes juego:"Honkai Star Rail" códigos:"HSRGIFT2024, STELLARON123, ASTRALEXPRESS"

# Códigos de colaboración
/codes juego:"Honkai Star Rail" códigos:"COLLAB2024, PARTNERSHIP, SPECIALEVENT"
```

**Zenless Zone Zero:**
```
# Códigos de lanzamiento
/codes juego:"Zenless Zone Zero" códigos:"ZZZLAUNCH, NEWWORLD2024, ZENLAUNCHER"

# Códigos de beta
/codes juego:"Zenless Zone Zero" códigos:"BETATEST2024, EARLYACCESS, ZZZPREVIEW"
```

**Honkai Impact 3rd:**
```
# Códigos regulares
/codes juego:"Honkai Impact 3rd" códigos:"HONKAI2024, VALKYRIE123, CAPTAIN456"

# Códigos de evento
/codes juego:"Honkai Impact 3rd" códigos:"ANNIVERSARY7TH, CELEBRATION, THANKYOU"
```

**Otros juegos populares:**
```
# Roblox
/codes juego:"Roblox" códigos:"ROBUX2024, FREEITEMS, SPECIALGIFT"

# Minecraft
/codes juego:"Minecraft" códigos:"MINECON2024, CREEPER123, DIAMOND456"

# Fortnite
/codes juego:"Fortnite" códigos:"VBUCKS2024, BATTLEPASS, FREESKIN"

# Among Us
/codes juego:"Among Us" códigos:"CREWMATE2024, IMPOSTOR123, SPACESHIP"
```

### Formatos de Códigos

**Lista simple:**
```
/codes juego:"Genshin Impact" códigos:"CODIGO1, CODIGO2, CODIGO3"
```

**Con saltos de línea:**
```
/codes juego:"Genshin Impact" códigos:"CODIGO1
CODIGO2
CODIGO3"
```

**Con descripciones:**
```
/codes juego:"Genshin Impact" códigos:"PRIMOGEMS100 - 100 Primogemas
MORA50000 - 50,000 Mora
EXP10 - 10 Hero's Wit"
```

**Con fechas de expiración:**
```
/codes juego:"Genshin Impact" códigos:"EVENTO2024 (Expira: 31/12/2024)
LIMITADO123 (Expira: 15/01/2025)
TEMPORAL456 (Expira: 01/02/2025)"
```

### Ejemplos con Imágenes

**Códigos de evento con imagen oficial:**
```
/codes juego:"Genshin Impact" códigos:"LANTERNRITE2024, MOONCHASE2024, WINDBLUME2024" imagen:https://genshin.hoyoverse.com/events/lantern-rite.jpg
```

**Códigos de livestream con captura:**
```
/codes juego:"Honkai Star Rail" códigos:"LIVESTREAM2024, PREVIEW456, SNEAK789" imagen:https://ejemplo.com/hsr-livestream.png
```

**Códigos de colaboración con arte promocional:**
```
/codes juego:"Zenless Zone Zero" códigos:"COLLAB2024, CROSSOVER123" imagen:https://ejemplo.com/zzz-collab.jpg
```

### Casos de Uso Completos

**Actualización semanal de códigos:**
```
# Lunes - Genshin Impact
/codes juego:"Genshin Impact" códigos:"WEEKLY2024, MONDAY123, FRESH456"

# Miércoles - Honkai Star Rail
/codes juego:"Honkai Star Rail" códigos:"MIDWEEK789, WEDNESDAY012, UPDATE345"

# Viernes - Zenless Zone Zero
/codes juego:"Zenless Zone Zero" códigos:"FRIDAY678, WEEKEND901, SPECIAL234"
```

**Evento especial multi-juego:**
```
# Aniversario de HoYoverse
/codes juego:"Genshin Impact" códigos:"ANNIVERSARY2024, HOYO4YEARS, CELEBRATION" imagen:https://ejemplo.com/hoyo-anniversary.jpg

/codes juego:"Honkai Star Rail" códigos:"ANNIVERSARY2024, HOYO4YEARS, CELEBRATION" imagen:https://ejemplo.com/hoyo-anniversary.jpg

/codes juego:"Honkai Impact 3rd" códigos:"ANNIVERSARY2024, HOYO4YEARS, CELEBRATION" imagen:https://ejemplo.com/hoyo-anniversary.jpg
```

**Códigos de emergencia/compensación:**
```
# Mantenimiento extendido
/codes juego:"Genshin Impact" códigos:"MAINTENANCE2024 - 300 Primogemas (Compensación por mantenimiento extendido)
SORRY123 - 5 Fragile Resin
APOLOGY456 - 100,000 Mora"

# Problemas del servidor
/codes juego:"Honkai Star Rail" códigos:"SERVERFIX2024 - 300 Stellar Jade
COMPENSATION - 5 Fuel
SORRYGIFT - 50,000 Credits"
```

### Configuración y Gestión

**El comando `/codes` también incluye funciones de configuración:**

**Cargar configuración de juegos:**
- El bot carga automáticamente la lista de juegos soportados
- Se pueden añadir nuevos juegos mediante configuración
- Los administradores pueden personalizar la lista

**Guardar configuración:**
- Los códigos se guardan automáticamente
- Historial de códigos enviados
- Prevención de duplicados

### Mejores Prácticas

**Verificación de códigos:**
```
# Siempre verificar antes de enviar
# Probar códigos en el juego
# Confirmar fechas de expiración
```

**Formato consistente:**
```
# Usar nombres de juegos estándar
# Mantener formato de códigos uniforme
# Incluir información relevante (expiración, recompensas)
```

**Timing apropiado:**
```
# Enviar códigos cuando estén frescos
# Actualizar regularmente
# Avisar sobre expiraciones próximas
```

---

## /puzzle

**Descripción:** Mini-juego de rompecabezas interactivo para la comunidad.
**Permisos requeridos:** Ninguno

**Sintaxis:**
```
/puzzle [dificultad:<nivel>]
```

**Parámetros:**
- `dificultad` (String, opcional): Nivel de dificultad del puzzle
  - `fácil` - Puzzles simples (por defecto)
  - `medio` - Puzzles moderados
  - `difícil` - Puzzles desafiantes
  - `extremo` - Puzzles muy difíciles

### Tipos de Puzzles

**Puzzles de lógica:**
```
# Puzzle fácil
/puzzle dificultad:fácil
# Ejemplo: "¿Qué número sigue en la secuencia: 2, 4, 6, 8, ?"

# Puzzle medio
/puzzle dificultad:medio
# Ejemplo: "Si A=1, B=2, C=3... ¿cuánto vale GATO?"

# Puzzle difícil
/puzzle dificultad:difícil
# Ejemplo: "En una habitación hay 3 interruptores y 3 bombillas en otra habitación..."
```

**Puzzles matemáticos:**
```
# Aritmética básica
/puzzle dificultad:fácil
# Ejemplo: "¿Cuál es el resultado de 15 + 27 × 2?"

# Álgebra simple
/puzzle dificultad:medio
# Ejemplo: "Si x + 5 = 12, ¿cuánto vale 2x?"

# Problemas complejos
/puzzle dificultad:difícil
# Ejemplo: "Un tren sale de A hacia B a 60 km/h..."
```

**Puzzles de palabras:**
```
# Anagramas
/puzzle dificultad:fácil
# Ejemplo: "Reorganiza las letras: AMOR → ?"

# Adivinanzas
/puzzle dificultad:medio
# Ejemplo: "Blanco por dentro, verde por fuera..."

# Acertijos complejos
/puzzle dificultad:difícil
# Ejemplo: "Tengo ciudades pero no casas, bosques pero no árboles..."
```

**Puzzles visuales:**
```
# Patrones simples
/puzzle dificultad:fácil
# Ejemplo: Secuencias de formas geométricas

# Ilusiones ópticas
/puzzle dificultad:medio
# Ejemplo: "¿Cuántos triángulos ves en esta imagen?"

# Puzzles espaciales
/puzzle dificultad:difícil
# Ejemplo: Rotación de objetos 3D
```

### Sistema de Puntuación

**Puntos por dificultad:**
- Fácil: 10 puntos
- Medio: 25 puntos
- Difícil: 50 puntos
- Extremo: 100 puntos

**Bonificaciones:**
- Primera respuesta correcta: +50% puntos
- Respuesta en menos de 30 segundos: +25% puntos
- Racha de 3 puzzles seguidos: +20% puntos
- Racha de 5 puzzles seguidos: +50% puntos

**Sistema de ranking:**
- Los puntos se acumulan por usuario
- Leaderboard semanal y mensual
- Títulos especiales por logros

### Ejemplos de Uso

**Sesión casual:**
```
# Empezar con algo fácil
/puzzle dificultad:fácil
# Responder y ganar confianza

# Subir dificultad gradualmente
/puzzle dificultad:medio
/puzzle dificultad:difícil
```

**Competencia amistosa:**
```
# Desafío entre amigos
/puzzle dificultad:medio
# "A ver quién resuelve este primero"

# Puzzle de desempate
/puzzle dificultad:difícil
# "Este decide el ganador"
```

**Entrenamiento mental:**
```
# Rutina diaria
/puzzle dificultad:fácil    # Calentamiento
/puzzle dificultad:medio    # Ejercicio principal
/puzzle dificultad:difícil  # Desafío
```

**Evento especial:**
```
# Torneo de puzzles
/puzzle dificultad:extremo
# "Solo para los más valientes"
```

### Casos de Uso por Contexto

**Canal de entretenimiento:**
```
/puzzle dificultad:fácil
# "Algo ligero para pasar el rato"
```

**Canal educativo:**
```
/puzzle dificultad:medio
# "Ejercitemos la mente un poco"
```

**Eventos de la comunidad:**
```
/puzzle dificultad:difícil
# "Puzzle especial del evento"
```

**Desafíos nocturnos:**
```
/puzzle dificultad:extremo
# "Para los noctámbulos más inteligentes"
```

### Interacción y Respuestas

**Cómo responder:**
1. El bot presenta el puzzle
2. Los usuarios responden en el chat
3. El bot verifica automáticamente las respuestas
4. Se anuncia al ganador y se otorgan puntos
5. Se muestra la explicación si es necesario

**Comandos relacionados:**
```
# Ver tu puntuación actual
/puzzle-stats

# Ver leaderboard
/puzzle-leaderboard

# Ver historial de puzzles
/puzzle-history

# Pista para puzzle actual
/puzzle-hint
```

### Tipos Especiales de Puzzles

**Puzzles temáticos:**
```
# Relacionados con Genshin Impact
/puzzle dificultad:medio
# "¿Cuántos elementos hay en Teyvat?"

# Relacionados con anime
/puzzle dificultad:difícil
# "¿En qué anime aparece este personaje?"

# Relacionados con gaming
/puzzle dificultad:fácil
# "¿Cuál es el nombre del fontanero más famoso?"
```

**Puzzles colaborativos:**
```
# Requieren múltiples personas
/puzzle dificultad:extremo
# "Este puzzle necesita que trabajen en equipo"
```

**Puzzles de temporada:**
```
# Navidad
/puzzle dificultad:medio
# Puzzles con temática navideña

# Halloween
/puzzle dificultad:difícil
# Puzzles de terror y misterio

# Año Nuevo
/puzzle dificultad:fácil
# Puzzles sobre resoluciones y metas
```

---

## Eventos y Competencias

### Torneos de Puzzles

**Formato semanal:**
```
# Lunes: Calentamiento
/puzzle dificultad:fácil

# Miércoles: Desafío principal
/puzzle dificultad:medio

# Viernes: Gran final
/puzzle dificultad:difícil

# Domingo: Puzzle extremo especial
/puzzle dificultad:extremo
```

**Competencia por equipos:**
```
# Dividir la comunidad en equipos
# Cada equipo resuelve puzzles juntos
# Puntos acumulativos por equipo
# Premio especial para el equipo ganador
```

### Eventos de Códigos

**Maratón de códigos:**
```
# Día 1: Genshin Impact
/codes juego:"Genshin Impact" códigos:"MARATHON1, DAY1GIFT, SPECIAL123"

# Día 2: Honkai Star Rail
/codes juego:"Honkai Star Rail" códigos:"MARATHON2, DAY2GIFT, SPECIAL456"

# Día 3: Zenless Zone Zero
/codes juego:"Zenless Zone Zero" códigos:"MARATHON3, DAY3GIFT, SPECIAL789"
```

**Códigos exclusivos del servidor:**
```
# Códigos especiales para miembros
/codes juego:"Genshin Impact" códigos:"SERVEREXCLUSIVE, MEMBERONLY, SPECIALCOMMUNITY"

# Códigos de aniversario del servidor
/codes juego:"Honkai Star Rail" códigos:"ANNIVERSARY1YEAR, THANKYOU, CELEBRATION"
```

---

## Integración con Otros Sistemas

### Sistema de Niveles

**Experiencia por actividad:**
- Resolver puzzles otorga XP
- Usar códigos otorga XP
- Participar en eventos otorga XP bonus

**Recompensas por nivel:**
- Acceso a puzzles exclusivos
- Códigos especiales para miembros de alto nivel
- Títulos y roles especiales

### Sistema de Giveaways

**Puzzles como requisito:**
```
# Giveaway que requiere resolver puzzle
/giveaway crear canal:#sorteos premio:"Discord Nitro" duracion:1d
# Requisito: Resolver puzzle de dificultad media
```

**Códigos como premio:**
```
# Sortear códigos exclusivos
/giveaway crear canal:#sorteos premio:"Códigos exclusivos Genshin" duracion:2d
```

---

## Consejos y Estrategias

### Para Puzzles

**Estrategias de resolución:**
1. **Leer cuidadosamente:** Entender bien el enunciado
2. **Pensar paso a paso:** No apresurarse
3. **Buscar patrones:** Identificar secuencias o lógica
4. **Eliminar opciones:** Descartar respuestas imposibles
5. **Verificar:** Comprobar la respuesta antes de enviar

**Mejora continua:**
```
# Empezar con dificultad baja
/puzzle dificultad:fácil

# Subir gradualmente
/puzzle dificultad:medio

# Desafiarse regularmente
/puzzle dificultad:difícil
```

### Para Códigos

**Gestión eficiente:**
1. **Verificar regularmente:** Buscar códigos nuevos
2. **Canjear rápido:** Los códigos pueden expirar
3. **Compartir responsablemente:** Solo códigos verificados
4. **Organizar por juego:** Mantener orden en los envíos

**Fuentes confiables:**
- Canales oficiales de los juegos
- Livestreams oficiales
- Redes sociales verificadas
- Comunidades reconocidas

---

## Moderación y Reglas

### Para Puzzles

**Reglas de participación:**
- No hacer spam de respuestas
- Respetar a otros participantes
- No buscar respuestas en internet (honor system)
- Aceptar las decisiones del bot

**Moderación:**
- Los moderadores pueden resetear puzzles
- Pueden otorgar puntos manualmente
- Pueden crear puzzles personalizados

### Para Códigos

**Reglas de envío:**
- Solo códigos verificados
- No códigos falsos o expirados
- Incluir información relevante
- No spam de códigos duplicados

**Verificación:**
- Los moderadores verifican códigos
- Se pueden reportar códigos incorrectos
- Historial de códigos enviados

---

> **Nota:** Los comandos de juegos están diseñados para fomentar la participación activa y el entretenimiento de la comunidad. Úsalos de manera responsable y diviértete mientras aprendes y compartes con otros miembros.