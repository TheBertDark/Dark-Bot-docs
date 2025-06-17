# Solucionar Problemas del Verificador KQMC

## Errores Comunes y Soluciones

### 🚫 "Personaje no encontrado"

#### Posibles Causas
- Nombre del personaje mal escrito
- Personaje no soportado por el sistema
- Uso de caracteres especiales

#### Soluciones
```bash
# ✅ Correcto
/tc Hu Tao DPS
/tc Zhongli Support
/tc Raiden Shogun DPS

# ❌ Incorrecto
/tc HuTao DPS          # Sin espacio
/tc Hu-Tao DPS         # Con guión
/tc hu tao DPS         # Minúsculas
```

#### Lista de Nombres Válidos
| Personaje | Nombres Aceptados |
|-----------|------------------|
| Hu Tao | "Hu Tao", "HuTao" |
| Raiden Shogun | "Raiden Shogun", "Raiden", "Shogun" |
| Zhongli | "Zhongli" |
| Tartaglia | "Tartaglia", "Childe" |
| Xiao | "Xiao" |

### 🚫 "Build no válida"

#### Tipos de Build Soportados
- **DPS**: Damage dealer principal
- **Sub-DPS**: Damage dealer secundario
- **Support**: Soporte general
- **Healer**: Sanador especializado
- **Tank**: Tanque/escudo
- **Burst**: Enfoque en Elemental Burst
- **Skill**: Enfoque en Elemental Skill

#### Ejemplos Correctos
```bash
/tc Ganyu DPS
/tc Bennett Support
/tc Diona Healer
/tc Zhongli Tank
/tc Xingqiu Sub-DPS
```

### 🚫 "Datos insuficientes"

#### Requisitos del Sistema
1. **Perfil público** en Genshin Impact
2. **Personaje en showcase** (máximo 8 personajes)
3. **Artefactos equipados** en el personaje
4. **Nivel mínimo** del personaje (40+)

#### Cómo Configurar tu Perfil

##### Paso 1: Hacer Público tu Perfil
1. Abre Genshin Impact
2. Ve a **Menú** → **Amigos**
3. Selecciona **Configuración de Perfil**
4. Activa **"Mostrar detalles del personaje"**

##### Paso 2: Configurar Showcase
1. Ve a **Perfil** → **Editar Información**
2. Selecciona **"Mostrar Personajes"**
3. Añade el personaje que quieres verificar
4. Asegúrate de que tenga artefactos equipados

##### Paso 3: Verificar Configuración
```bash
# Comando para verificar si tu perfil es accesible
/profile [tu_uid]
```

### 🚫 "Error de conexión"

#### Posibles Causas
- Servidores de Genshin Impact temporalmente inaccesibles
- Mantenimiento en curso
- Problemas de red

#### Soluciones
1. **Esperar unos minutos** y reintentar
2. **Verificar estado** de servidores de Genshin
3. **Comprobar conexión** a internet
4. **Contactar soporte** si persiste

### 🚫 "UID no válido"

#### Formato Correcto de UID
- **Longitud**: 9 dígitos
- **Formato**: Solo números
- **Región**: Debe coincidir con tu servidor

#### Ejemplos
```bash
# ✅ Correcto
/tc Diluc DPS 123456789

# ❌ Incorrecto
/tc Diluc DPS 12345678    # Muy corto
/tc Diluc DPS 1234567890  # Muy largo
/tc Diluc DPS 12345678a   # Contiene letras
```

#### Cómo Encontrar tu UID
1. Abre Genshin Impact
2. Ve al **menú principal**
3. Tu UID aparece en la **esquina inferior derecha**

## Problemas de Rendimiento

### ⏱️ "Comando muy lento"

#### Causas Comunes
- Alto tráfico en el bot
- Servidores de Genshin sobrecargados
- Perfil con muchos personajes

#### Optimizaciones
1. **Usar en horarios** de menor tráfico
2. **Especificar UID** directamente
3. **Mantener showcase** con pocos personajes
4. **Esperar pacientemente** (puede tomar 30-60 segundos)

### 📊 "Resultados inconsistentes"

#### Posibles Causas
- Cambios recientes en artefactos
- Cache del sistema desactualizado
- Múltiples builds del mismo personaje

#### Soluciones
1. **Esperar 5-10 minutos** después de cambios
2. **Usar comando de refresh**:
   ```bash
   /refresh_profile [uid]
   ```
3. **Verificar que el personaje** esté en showcase
4. **Confirmar artefactos** equipados correctamente

## Problemas de Interpretación

### 🤔 "Puntuación muy baja"

#### Factores que Afectan la Puntuación
1. **Ratios desequilibrados** (Crit Rate vs Crit DMG)
2. **Substats irrelevantes** en artefactos
3. **Nivel de artefactos** bajo
4. **Set bonuses** subóptimos

#### Cómo Mejorar
1. **Priorizar Crit Rate** hasta 60-70%
2. **Balancear con Crit DMG** (ratio 1:2)
3. **Reemplazar artefactos** con substats pobres
4. **Subir nivel** de artefactos principales

### 🎯 "Recomendaciones confusas"

#### Entender las Prioridades
- **Prioridad 1**: Crítico para el funcionamiento
- **Prioridad 2**: Importante para optimización
- **Prioridad 3**: Mejoras menores
- **Prioridad 4**: Optimización avanzada

#### Orden de Mejoras Sugerido
1. **Corregir ratios** críticos primero
2. **Mejorar artefactos** principales
3. **Optimizar substats** secundarios
4. **Ajustar detalles** finales

## Limitaciones Conocidas

### 🔒 Restricciones del Sistema

#### Personajes No Soportados
- Personajes muy nuevos (primeras 2 semanas)
- Personajes con mecánicas únicas complejas
- Builds muy especializadas o experimentales

#### Métricas No Consideradas
- **Buffs de equipo**: Bennett, Sara, Kazuha
- **Resonancias**: Pyro, Geo, Electro, etc.
- **Rotaciones específicas**: Uptime de habilidades
- **Situaciones de combate**: Tipo de enemigos

### 📝 Recomendaciones Generales

#### Usar Como Guía
- Los resultados son **orientativos**
- **Prueba en combate** real siempre
- **Adapta según tu equipo** y estilo
- **Considera el contenido** que juegas

#### Complementar con Otras Herramientas
- **Calculadoras de daño** externas
- **Guías de personajes** especializadas
- **Comunidad de teorycrafting**
- **Pruebas propias** en el juego

## Obtener Ayuda Adicional

### 📞 Canales de Soporte

#### Discord
- **Canal #kqmc-help**: Ayuda específica del verificador
- **Canal #builds**: Discusión de builds
- **Canal #teorycrafting**: Análisis avanzado

#### Comandos de Diagnóstico
```bash
# Verificar estado del sistema
/kqmc_status

# Información de tu perfil
/profile_info [uid]

# Historial de verificaciones
/kqmc_history

# Reportar problema
/report_issue [descripción]
```

### 🐛 Reportar Bugs

#### Información Necesaria
1. **Comando exacto** usado
2. **UID** del jugador
3. **Mensaje de error** completo
4. **Captura de pantalla** si es posible
5. **Hora aproximada** del error

#### Formato de Reporte
```
Comando: /tc Diluc DPS 123456789
Error: "Personaje no encontrado"
Hora: 15:30 GMT-5
UID: 123456789
Servidor: América
```

### 💡 Consejos Adicionales

#### Mejores Prácticas
1. **Mantén tu perfil actualizado** regularmente
2. **Usa nombres estándar** de personajes
3. **Especifica builds claras** (DPS, Support, etc.)
4. **Ten paciencia** con los tiempos de respuesta
5. **Lee los resultados** completamente antes de preguntar

#### Recursos Útiles
- [Guía completa del verificador](/kqmc/guide)
- [Cómo interpretar resultados](/kqmc/results)
- [Consejos de optimización](/kqmc/optimization)
- [Preguntas frecuentes](/faq)

---

¿Sigues teniendo problemas? Únete a nuestro [servidor de soporte](/support) donde expertos de la comunidad pueden ayudarte paso a paso.