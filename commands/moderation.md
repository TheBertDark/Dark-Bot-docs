# 🛡️ Comandos de Moderación

Esta sección detalla todos los comandos de moderación disponibles, con ejemplos completos, casos de uso y mejores prácticas para mantener tu servidor seguro.

---

## /ban

**Descripción:** Sistema completo de gestión de baneos con historial detallado.
**Permisos requeridos:** Banear Miembros

### Subcomandos

#### add
Banea a un usuario del servidor con registro en el historial.

**Sintaxis:**
```
/ban add usuario:<@usuario> [razón:<texto>] [duración:<tiempo>]
```

**Parámetros:**
- `usuario` (Usuario, requerido): Usuario a banear
- `razón` (String, opcional): Motivo del baneo
- `duración` (String, opcional): Duración del baneo temporal

**Formatos de duración:**
- `s` - segundos
- `m` - minutos  
- `h` - horas
- `d` - días
- `w` - semanas

**Ejemplos:**
```
# Baneo permanente con razón
/ban add usuario:@SpammerUser razón:Spam excesivo en múltiples canales

# Baneo temporal
/ban add usuario:@ToxicUser razón:Lenguaje ofensivo duración:7d

# Baneo temporal corto
/ban add usuario:@RuleBreaker razón:Incumplimiento de reglas duración:24h

# Baneo sin razón específica
/ban add usuario:@ProblemUser
```

#### list
Muestra el historial de baneos de un usuario.

**Sintaxis:**
```
/ban list [usuario:<@usuario>]
```

**Parámetros:**
- `usuario` (Usuario, opcional): Usuario específico a consultar

**Ejemplos:**
```
# Ver historial de un usuario específico
/ban list usuario:@ProblematicUser

# Ver todos los baneos recientes del servidor
/ban list
```

#### remove
Elimina un registro de baneo del historial.

**Sintaxis:**
```
/ban remove usuario:<@usuario> index:<número>
```

**Parámetros:**
- `usuario` (Usuario, requerido): Usuario del historial
- `index` (Entero, requerido): Índice del baneo a remover

**Ejemplo:**
```
# Remover el primer baneo del historial
/ban remove usuario:@ReformedUser index:1
```

### Casos de Uso

**Moderación por spam:**
```
# Baneo temporal por spam
/ban add usuario:@Spammer razón:Spam en #general y #off-topic duración:3d

# Verificar historial después
/ban list usuario:@Spammer
```

**Escalación de sanciones:**
```
# Primera ofensa - baneo corto
/ban add usuario:@FirstOffender razón:Primera violación de reglas duración:1d

# Segunda ofensa - baneo más largo
/ban add usuario:@SecondOffender razón:Segunda violación - comportamiento tóxico duración:1w

# Tercera ofensa - baneo permanente
/ban add usuario:@RepeatOffender razón:Tercera violación - baneo permanente
```

**Gestión de historial:**
```
# Ver historial completo
/ban list usuario:@UserInQuestion

# Limpiar registro antiguo (usuario reformado)
/ban remove usuario:@ReformedUser index:1
```

---

## /kick

**Descripción:** Expulsa a un usuario del servidor sin banear.
**Permisos requeridos:** Expulsar Miembros

**Sintaxis:**
```
/kick usuario:<@usuario> [razón:<texto>]
```

**Parámetros:**
- `usuario` (Usuario, requerido): Usuario a expulsar
- `razón` (String, opcional): Motivo de la expulsión

**Ejemplos:**
```
# Kick con razón detallada
/kick usuario:@DisruptiveUser razón:Interrumpir conversaciones y causar drama

# Kick por comportamiento menor
/kick usuario:@MinorOffender razón:Incumplimiento menor de reglas

# Kick de advertencia
/kick usuario:@WarningCase razón:Advertencia final - próxima infracción resultará en ban

# Kick sin razón específica
/kick usuario:@ProblemUser
```

### Casos de Uso

**Advertencia seria:**
```
/kick usuario:@AlmostBanned razón:Última advertencia por comportamiento inapropiado. Próxima infracción resultará en ban permanente.
```

**Resolución de conflictos:**
```
/kick usuario:@ArgumentStarter razón:Iniciar argumentos innecesarios en #general. Tómate un descanso y regresa cuando estés más calmado.
```

**Violación menor:**
```
/kick usuario:@RuleViolator razón:Enviar contenido NSFW en canales generales. Lee las reglas antes de regresar.
```

---

## /mute

**Descripción:** Silencia a un usuario temporalmente.
**Permisos requeridos:** Silenciar Miembros

**Sintaxis:**
```
/mute usuario:<@usuario> [razón:<texto>] [duración:<tiempo>]
```

**Parámetros:**
- `usuario` (Usuario, requerido): Usuario a silenciar
- `razón` (String, opcional): Motivo del mute
- `duración` (String, opcional): Duración del silenciamiento

**Ejemplos:**
```
# Mute temporal por spam
/mute usuario:@Spammer razón:Spam en chat duración:1h

# Mute por comportamiento tóxico
/mute usuario:@ToxicUser razón:Lenguaje ofensivo hacia otros miembros duración:6h

# Mute corto de advertencia
/mute usuario:@WarningUser razón:Advertencia por incumplir reglas duración:30m

# Mute largo por infracción seria
/mute usuario:@SeriousOffender razón:Acoso a otros miembros duración:24h
```

### Casos de Uso

**Escalación gradual:**
```
# Primera advertencia
/mute usuario:@NewOffender razón:Primera advertencia - lee las reglas duración:15m

# Segunda advertencia
/mute usuario:@SecondWarning razón:Segunda advertencia - comportamiento continuo duración:1h

# Advertencia seria
/mute usuario:@FinalWarning razón:Advertencia final antes de ban duración:12h
```

**Situaciones específicas:**
```
# Durante eventos o anuncios importantes
/mute usuario:@Disruptor razón:Interrumpir anuncio importante duración:30m

# Por flood/spam
/mute usuario:@Flooder razón:Flood excesivo en chat duración:2h

# Por contenido inapropiado
/mute usuario:@InappropriateContent razón:Compartir contenido inapropiado duración:4h
```

---

## /warn

**Descripción:** Sistema completo de advertencias con historial.
**Permisos requeridos:** Gestionar Mensajes

### Subcomandos

#### add
Añade una advertencia al historial del usuario.

**Sintaxis:**
```
/warn add usuario:<@usuario> razón:<texto>
```

**Parámetros:**
- `usuario` (Usuario, requerido): Usuario a advertir
- `razón` (String, requerido): Motivo de la advertencia

**Ejemplos:**
```
# Advertencia por lenguaje
/warn add usuario:@BadLanguage razón:Uso de lenguaje inapropiado en #general

# Advertencia por spam
/warn add usuario:@SpamUser razón:Envío repetitivo de mensajes en múltiples canales

# Advertencia por off-topic
/warn add usuario:@OffTopic razón:Conversaciones no relacionadas en #genshin-help

# Advertencia por menciones excesivas
/warn add usuario:@MentionSpammer razón:Mencionar usuarios innecesariamente múltiples veces
```

#### list
Muestra todas las advertencias de un usuario.

**Sintaxis:**
```
/warn list usuario:<@usuario>
```

**Ejemplo:**
```
/warn list usuario:@ProblematicUser
```

#### remove
Elimina una advertencia específica del historial.

**Sintaxis:**
```
/warn remove usuario:<@usuario> index:<número>
```

**Ejemplo:**
```
# Remover la primera advertencia
/warn remove usuario:@ImprovedUser index:1
```

#### clear
Elimina todas las advertencias de un usuario.

**Sintaxis:**
```
/warn clear usuario:<@usuario>
```

**Ejemplo:**
```
# Limpiar historial de usuario reformado
/warn clear usuario:@ReformedUser
```

### Casos de Uso

**Sistema de tres advertencias:**
```
# Primera advertencia
/warn add usuario:@NewUser razón:Primera advertencia - revisar reglas del servidor

# Segunda advertencia
/warn add usuario:@SecondChance razón:Segunda advertencia - comportamiento continuo inapropiado

# Tercera advertencia (antes de ban)
/warn add usuario:@LastChance razón:Tercera advertencia - próxima infracción resultará en ban
```

**Seguimiento de comportamiento:**
```
# Verificar historial antes de sancionar
/warn list usuario:@CheckUser

# Añadir nueva advertencia basada en historial
/warn add usuario:@RepeatOffender razón:Cuarta infracción - patrón de comportamiento problemático
```

**Gestión de advertencias:**
```
# Remover advertencia antigua por buen comportamiento
/warn remove usuario:@GoodBehavior index:1

# Limpiar historial después de período de prueba
/warn clear usuario:@CleanSlate
```

---

## /unban

**Descripción:** Desbanea a un usuario del servidor.
**Permisos requeridos:** Banear Miembros

**Sintaxis:**
```
/unban usuario-id:<ID> [razón:<texto>]
```

**Parámetros:**
- `usuario-id` (String, requerido): ID del usuario a desbanear
- `razón` (String, opcional): Motivo del desbaneo

**Ejemplos:**
```
# Desbaneo por apelación aceptada
/unban usuario-id:123456789012345678 razón:Apelación aceptada - comportamiento reformado

# Desbaneo por error administrativo
/unban usuario-id:987654321098765432 razón:Ban incorrecto - error administrativo

# Desbaneo después de tiempo cumplido
/unban usuario-id:456789123456789012 razón:Tiempo de ban cumplido - segunda oportunidad

# Desbaneo sin razón específica
/unban usuario-id:789123456789123456
```

### Casos de Uso

**Proceso de apelación:**
```
# Después de revisar apelación
/unban usuario-id:123456789012345678 razón:Apelación revisada y aceptada por el equipo de moderación
```

**Corrección de errores:**
```
# Ban por error
/unban usuario-id:987654321098765432 razón:Ban aplicado por error - disculpas por la inconveniencia
```

**Segunda oportunidad:**
```
# Después de período de reflexión
/unban usuario-id:456789123456789012 razón:Segunda oportunidad después de 30 días - comportamiento esperado mejorado
```

---

## /lock y /unlock

**Descripción:** Controla el acceso de escritura a canales.
**Permisos requeridos:** Gestionar Canales

### /lock
Bloquea un canal para que los usuarios no puedan escribir.

**Sintaxis:**
```
/lock [canal:<#canal>] [razón:<texto>]
```

**Parámetros:**
- `canal` (Canal, opcional): Canal a bloquear (actual si no se especifica)
- `razón` (String, opcional): Motivo del bloqueo

**Ejemplos:**
```
# Bloquear canal actual
/lock razón:Mantenimiento del servidor

# Bloquear canal específico
/lock canal:#general razón:Limpieza de spam

# Bloqueo durante evento
/lock canal:#chat-general razón:Evento en curso - solo anuncios

# Bloqueo de emergencia
/lock razón:Situación de emergencia - canal temporalmente cerrado
```

### /unlock
Desbloquea un canal previamente bloqueado.

**Sintaxis:**
```
/unlock [canal:<#canal>]
```

**Ejemplos:**
```
# Desbloquear canal actual
/unlock

# Desbloquear canal específico
/unlock canal:#general
```

### Casos de Uso

**Mantenimiento del servidor:**
```
# Antes del mantenimiento
/lock canal:#general razón:Mantenimiento programado - regresamos en 30 minutos

# Después del mantenimiento
/unlock canal:#general
```

**Control de situaciones:**
```
# Durante drama o conflicto
/lock razón:Enfriamiento necesario - reabriremos cuando se calmen los ánimos

# Después de resolver el conflicto
/unlock
```

**Eventos especiales:**
```
# Durante anuncio importante
/lock canal:#anuncios razón:Anuncio importante en curso

# Después del anuncio
/unlock canal:#anuncios
```

---

## /ticket-panel

**Descripción:** Genera un panel interactivo para crear tickets de soporte.
**Permisos requeridos:** Gestionar Canales

**Sintaxis:**
```
/ticket-panel canal:<#canal> categoria:<categoría>
```

**Parámetros:**
- `canal` (Canal, requerido): Canal donde se enviará el panel
- `categoria` (Categoría, requerido): Categoría donde se crearán los tickets

**Ejemplos:**
```
# Panel básico de soporte
/ticket-panel canal:#crear-ticket categoria:Soporte

# Panel para reportes
/ticket-panel canal:#reportes categoria:Moderación

# Panel para sugerencias
/ticket-panel canal:#sugerencias categoria:Feedback
```

### Casos de Uso

**Sistema de soporte completo:**
```
# Panel principal de soporte
/ticket-panel canal:#soporte categoria:Tickets-Soporte

# Panel para reportes de usuarios
/ticket-panel canal:#reportar-usuario categoria:Reportes

# Panel para problemas técnicos
/ticket-panel canal:#problemas-técnicos categoria:Soporte-Técnico
```

**Organización por departamentos:**
```
# Soporte general
/ticket-panel canal:#soporte-general categoria:Soporte-General

# Soporte VIP
/ticket-panel canal:#soporte-vip categoria:Soporte-VIP

# Apelaciones
/ticket-panel canal:#apelaciones categoria:Apelaciones
```

---

## Comandos de Modmail

### /modmail-reply
**Descripción:** Responde a un modmail activo.
**Uso:** Permite a los moderadores responder a mensajes privados de usuarios.

### /modmail-anonreply
**Descripción:** Responde anónimamente a un modmail.
**Uso:** Respuesta sin revelar la identidad del moderador.

### /modmail-reopen
**Descripción:** Reabre un modmail cerrado.
**Uso:** Útil cuando se necesita continuar una conversación.

### /modmail-tag
**Descripción:** Añade etiquetas organizacionales a modmails.
**Uso:** Categoriza y organiza conversaciones de modmail.

### /modmail-block
**Descripción:** Bloquea a un usuario del sistema modmail.
**Uso:** Previene spam o abuso del sistema de modmail.

---

## /logs

**Descripción:** Configura el sistema de logs del servidor.
**Permisos requeridos:** Gestionar Servidor

### Funcionalidad
Este comando abre un panel para configurar:
- Canales de logs por tipo de evento
- Eventos a registrar
- Formato de los logs
- Filtros y exclusiones

**Ejemplo:**
```
/logs
```

### Tipos de Logs Disponibles

**Logs de Moderación:**
- Baneos y desbaneos
- Kicks y mutes
- Advertencias
- Cambios de roles

**Logs de Servidor:**
- Miembros que se unen/salen
- Cambios de canales
- Cambios de roles
- Actualizaciones del servidor

**Logs de Mensajes:**
- Mensajes eliminados
- Mensajes editados
- Mensajes en canales específicos

---

## /verified-send

**Descripción:** Envía un mensaje como usuario verificado.
**Permisos requeridos:** Gestionar Mensajes

### Funcionalidad
Permite a los moderadores enviar mensajes oficiales con:
- Marca de verificación
- Formato especial
- Autoridad administrativa

**Uso típico:**
- Anuncios oficiales
- Comunicados importantes
- Respuestas oficiales a la comunidad

---

## Mejores Prácticas de Moderación

### Escalación de Sanciones

**Nivel 1 - Advertencia:**
```
/warn add usuario:@Usuario razón:Primera infracción - revisar reglas
```

**Nivel 2 - Mute temporal:**
```
/mute usuario:@Usuario razón:Segunda infracción duración:1h
```

**Nivel 3 - Kick:**
```
/kick usuario:@Usuario razón:Tercera infracción - tómate un descanso
```

**Nivel 4 - Ban temporal:**
```
/ban add usuario:@Usuario razón:Cuarta infracción duración:7d
```

**Nivel 5 - Ban permanente:**
```
/ban add usuario:@Usuario razón:Múltiples infracciones - ban permanente
```

### Documentación de Acciones

**Siempre incluye razones detalladas:**
```
# ❌ Malo
/ban add usuario:@Usuario razón:Mal comportamiento

# ✅ Bueno
/ban add usuario:@Usuario razón:Spam repetitivo en #general después de múltiples advertencias, ignorando reglas del servidor
```

**Mantén consistencia:**
- Usa el mismo formato para razones similares
- Documenta el contexto completo
- Incluye referencias a reglas específicas

### Comunicación con el Usuario

**Antes de sancionar:**
1. Advertencia verbal en chat
2. Mensaje privado explicando la situación
3. Oportunidad de corrección

**Durante la sanción:**
1. Explicación clara del motivo
2. Duración específica (si aplica)
3. Pasos para apelar o mejorar

**Después de la sanción:**
1. Seguimiento del comportamiento
2. Reconocimiento de mejoras
3. Posible reducción de sanciones

---

> **Importante:** La moderación efectiva requiere consistencia, transparencia y comunicación clara. Siempre documenta tus acciones y mantén un enfoque justo y profesional.