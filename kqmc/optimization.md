# Consejos de Optimización KQMC

## Fundamentos de Optimización

### 🎯 Principios Básicos

La optimización de builds en Genshin Impact sigue principios matemáticos específicos que el verificador KQMC evalúa:

1. **Diminishing Returns**: Cada stat tiene un punto de rendimiento decreciente
2. **Opportunity Cost**: Mejorar un stat significa sacrificar otro
3. **Synergy**: Algunos stats se potencian mutuamente
4. **Context Dependency**: La build óptima depende del contexto de uso

### 📊 Jerarquía de Prioridades

#### Nivel 1: Stats Fundamentales
- **Crit Rate**: Base para daño consistente
- **Crit DMG**: Multiplicador de daño crítico
- **ATK%/HP%/DEF%**: Stat principal según scaling del personaje

#### Nivel 2: Stats Situacionales
- **Elemental DMG Bonus**: Multiplicador específico
- **Energy Recharge**: Para rotaciones fluidas
- **Elemental Mastery**: Para reacciones elementales

#### Nivel 3: Stats Secundarios
- **ATK/HP/DEF Flat**: Valores base adicionales
- **Healing Bonus**: Para sanadores especializados
- **Physical DMG Bonus**: Para builds físicas

## Optimización por Rol

### 🗡️ DPS Principal

#### Prioridades Optimizadas
```
1. Crit Rate (60-70%) → Consistencia de daño
2. Crit DMG (120-200%) → Maximizar críticos
3. ATK% (112%+) → Stat base principal
4. Elemental DMG Bonus → Multiplicador específico
5. Energy Recharge (120-140%) → Uptime de burst
```

#### Ratios Objetivo
- **Crit Rate : Crit DMG** = 1:2
- **ATK Total** = 1,800-2,500
- **Crit Value** = 180-220+
- **Efficiency** = 75%+

#### Ejemplo: Diluc DPS
```
Stats Objetivo:
Crit Rate: 65% | Crit DMG: 130% | CV: 195
ATK: 2,100 | Pyro DMG: 46.6% | ER: 130%

Artefactos Recomendados:
4pc Crimson Witch of Flames
Sands: ATK% | Goblet: Pyro DMG | Circlet: Crit Rate/DMG
```

### ⚡ Sub-DPS

#### Prioridades Optimizadas
```
1. Elemental DMG Bonus → Daño de habilidades
2. Crit Rate (50-60%) → Consistencia moderada
3. Crit DMG (100-150%) → Burst damage
4. Energy Recharge (140-180%) → Rotación fluida
5. ATK% → Stat base
```

#### Ratios Objetivo
- **Energy Recharge** = 140-180%
- **Crit Value** = 140-180
- **Elemental DMG** = 46.6%
- **Efficiency** = 70%+

#### Ejemplo: Xingqiu Sub-DPS
```
Stats Objetivo:
Crit Rate: 55% | Crit DMG: 110% | CV: 165
ATK: 1,800 | Hydro DMG: 46.6% | ER: 180%

Artefactos Recomendados:
4pc Emblem of Severed Fate
Sands: ATK%/ER% | Goblet: Hydro DMG | Circlet: Crit Rate
```

### 🛡️ Support

#### Prioridades Optimizadas
```
1. Energy Recharge (180-250%) → Uptime de utility
2. HP%/DEF% → Survivability y scaling
3. Elemental Mastery → Reacciones
4. Crit Rate (30-50%) → Si aplica Favonius
5. Healing/Shield Bonus → Especialización
```

#### Ratios Objetivo
- **Energy Recharge** = 200-250%
- **HP/DEF Total** = Según scaling
- **Elemental Mastery** = 100-300
- **Efficiency** = 60%+

#### Ejemplo: Bennett Support
```
Stats Objetivo:
HP: 22,000+ | ER: 220% | Healing: +15%
Crit Rate: 40% (Favonius) | EM: 150

Artefactos Recomendados:
4pc Noblesse Oblige
Sands: ER%/HP% | Goblet: HP% | Circlet: Healing/HP%
```

## Estrategias de Farming

### 🎲 Eficiencia de Resin

#### Prioridad de Dominios
1. **Artefactos principales** (80% del tiempo)
2. **Materiales de ascensión** (15% del tiempo)
3. **Libros de talento** (5% del tiempo)

#### Rotación Semanal Sugerida
```
Lunes-Miércoles: Farming de artefactos
Jueves: Materiales de ascensión
Viernes-Domingo: Artefactos + talentos
```

### 🎯 Targeting de Artefactos

#### Criterios de Calidad

##### Tier S (Keeper)
- **4 substats útiles** desde nivel 0
- **3+ rolls** en Crit Rate/DMG
- **Efficiency** > 80%

##### Tier A (Usable)
- **3 substats útiles** + 1 neutral
- **2-3 rolls** en stats críticos
- **Efficiency** 70-80%

##### Tier B (Temporal)
- **2-3 substats útiles**
- **1-2 rolls** en stats importantes
- **Efficiency** 60-70%

##### Tier F (Fodder)
- **<2 substats útiles**
- **0-1 rolls** en stats críticos
- **Efficiency** <60%

### 📈 Progresión Gradual

#### Fase 1: Fundación (AR 45-50)
```
Objetivo: Sets completos con stats principales correctos
Criterio: Efficiency >50%, substats secundarios
Tiempo: 2-4 semanas por personaje
```

#### Fase 2: Optimización (AR 50-55)
```
Objetivo: Mejorar substats, balancear ratios
Criterio: Efficiency >65%, Crit Value >140
Tiempo: 4-8 semanas por personaje
```

#### Fase 3: Perfección (AR 55+)
```
Objetivo: Min-maxing, builds especializadas
Criterio: Efficiency >75%, Crit Value >180
Tiempo: 2-6 meses por personaje
```

## Técnicas Avanzadas

### 🧮 Cálculo de Valor

#### Fórmula de Crit Value
```
CV = (Crit Rate × 2) + Crit DMG

Ejemplo:
65% Crit Rate + 130% Crit DMG = (65×2) + 130 = 260 CV
```

#### Efficiency Score
```
Efficiency = (Substats Actuales / Substats Máximos Posibles) × 100

Factores:
- Número de rolls en substats útiles
- Valor de cada roll (bajo/medio/alto)
- Distribución entre stats críticos
```

### ⚖️ Balanceo de Stats

#### Regla del 1:2 (Crit Rate:Crit DMG)
```
Óptimo matemático para maximizar daño promedio

Ejemplos balanceados:
50% CR : 100% CD
60% CR : 120% CD
70% CR : 140% CD
```

#### Excepciones a la Regla
- **Cryo DPS** con 4pc Blizzard Strayer: Menos Crit Rate necesario
- **Kokomi**: No puede hacer crítico, ignorar Crit stats
- **Favonius weapons**: Priorizar Crit Rate para proc

### 🔄 Optimización Iterativa

#### Proceso de Mejora
1. **Evaluar build actual** con KQMC
2. **Identificar bottleneck** principal
3. **Farmear mejoras específicas**
4. **Re-evaluar y ajustar**
5. **Repetir hasta satisfacción**

#### Criterios de Parada
```
Build "Suficiente":
- Crit Value >160
- Efficiency >70%
- Puede completar contenido objetivo

Build "Excelente":
- Crit Value >180
- Efficiency >80%
- Top 10% de builds del personaje
```

## Optimización por Contenido

### 🏰 Spiral Abyss

#### Floor 9-10 (Fácil)
```
Requisitos mínimos:
- Crit Value >140
- Efficiency >60%
- Builds funcionales, no perfectas
```

#### Floor 11-12 (Difícil)
```
Requisitos recomendados:
- Crit Value >170
- Efficiency >75%
- Builds optimizadas, synergy de equipo
```

### 🌍 Overworld

#### Exploración General
```
Prioridades:
1. Velocidad de movimiento
2. Utility (mining, cooking, etc.)
3. Daño suficiente para mobs
4. Survivability
```

#### Boss Farming
```
Prioridades:
1. Daño burst alto
2. Energy Recharge para rotaciones
3. Resistencia a interrupciones
4. Healing/shielding
```

### 🎭 Eventos y Challenges

#### Adaptabilidad
- **Builds flexibles** que funcionen en múltiples escenarios
- **Multiple sets** para diferentes buffs de evento
- **Utility characters** bien construidos

## Herramientas Complementarias

### 📱 Calculadoras Externas

#### Genshin Optimizer
- **Optimización automática** de artefactos
- **Comparación de builds** múltiples
- **Simulación de daño** detallada

#### Enka Network
- **Showcase automático** de builds
- **Comparación con otros jugadores**
- **Tracking de progreso** temporal

### 📊 Tracking de Progreso

#### Métricas a Seguir
1. **Crit Value** por personaje
2. **Efficiency** promedio del roster
3. **Tiempo de clear** en Abyss
4. **Satisfacción personal** con builds

#### Herramientas de Registro
```
Spreadsheet personal:
- Fecha de última mejora
- Stats actuales vs objetivo
- Prioridad de farming
- Notas de optimización
```

## Consejos Psicológicos

### 🎯 Gestión de Expectativas

#### Realismo
- **Perfección es cara**: Últimas mejoras requieren mucho tiempo
- **80/20 rule**: 80% del rendimiento con 20% del esfuerzo
- **Diminishing returns**: Cada mejora es más difícil que la anterior

#### Satisfacción
- **Define "suficiente"** para cada personaje
- **Celebra mejoras** incrementales
- **No compares** con whales o streamers

### 🔄 Evitar Burnout

#### Rotación de Objetivos
- **Alterna entre personajes** para evitar frustración
- **Mezcla farming** con otros contenidos
- **Toma descansos** del artifact farming

#### Perspectiva a Largo Plazo
- **Builds mejoran gradualmente** con el tiempo
- **Nuevos artefactos** aparecen constantemente
- **Meta evoluciona**, adaptabilidad > perfección

---

¿Necesitas ayuda optimizando un personaje específico? Únete a nuestro [servidor de soporte](/support) donde expertos pueden revisar tu build y sugerir mejoras específicas.