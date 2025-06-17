# Cómo Interpretar Resultados del Verificador KQMC

## Estructura del Reporte

Cuando usas el comando `/tc`, el verificador KQMC genera un reporte detallado con múltiples secciones:

### 📊 Resumen General
- **Puntuación Total**: Score general de 0-100
- **Nivel de Build**: Clasificación cualitativa
- **Recomendación**: Sugerencia principal

### 🎯 Métricas Críticas
- **Crit Rate**: Probabilidad de crítico
- **Crit DMG**: Daño crítico
- **Crit Value**: Valor crítico combinado
- **Ratio**: Relación Crit Rate:Crit DMG

### ⚡ Estadísticas Principales
- **ATK Total**: Ataque combinado
- **HP Total**: Vida total
- **DEF Total**: Defensa total
- **Elemental Mastery**: Maestría elemental
- **Energy Recharge**: Recarga de energía

## Interpretación de Puntuaciones

### Sistema de Calificación

#### 🏆 Excelente (90-100)
```
✅ Build optimizada al máximo
✅ Ratios perfectos
✅ Substats de alta calidad
✅ Listo para contenido endgame
```

#### 🥇 Muy Buena (80-89)
```
✅ Build muy sólida
✅ Ratios balanceados
⚠️ Pequeñas mejoras posibles
✅ Excelente para la mayoría de contenido
```

#### 🥈 Buena (70-79)
```
✅ Build funcional
⚠️ Algunos ratios mejorables
⚠️ Substats promedio
✅ Adecuada para contenido general
```

#### 🥉 Promedio (60-69)
```
⚠️ Build básica
⚠️ Ratios desequilibrados
❌ Substats por mejorar
⚠️ Funciona pero necesita trabajo
```

#### ❌ Necesita Mejoras (<60)
```
❌ Build subóptima
❌ Ratios muy desequilibrados
❌ Substats de baja calidad
❌ Requiere atención inmediata
```

## Análisis Detallado por Métrica

### Crit Value (CV)

#### Cálculo
```
Crit Value = (Crit Rate × 2) + Crit DMG
```

#### Rangos de Evaluación
| CV Range | Calificación | Descripción |
|----------|--------------|-------------|
| 200+ | Excepcional | Build perfecta |
| 180-199 | Excelente | Muy optimizada |
| 160-179 | Muy Buena | Bien balanceada |
| 140-159 | Buena | Funcional |
| 120-139 | Promedio | Mejorable |
| <120 | Baja | Necesita trabajo |

### Efficiency Score

#### Qué Mide
- Calidad de substats en artefactos
- Distribución de stats secundarias
- Potencial de mejora restante

#### Interpretación
| Efficiency | Significado |
|------------|-------------|
| 90%+ | Artefactos casi perfectos |
| 80-89% | Artefactos excelentes |
| 70-79% | Artefactos buenos |
| 60-69% | Artefactos promedio |
| <60% | Artefactos necesitan reemplazo |

### Ratio Analysis

#### Crit Rate : Crit DMG

**Ratio Ideal**: 1:2

| Ratio | Evaluación | Recomendación |
|-------|------------|---------------|
| 1:2 | Perfecto | Mantener balance |
| 1:1.8-1.9 | Muy bueno | Subir Crit DMG ligeramente |
| 1:2.1-2.3 | Bueno | Considerar más Crit Rate |
| 1:1.5-1.7 | Bajo Crit DMG | Priorizar Crit DMG |
| 1:2.4+ | Bajo Crit Rate | Priorizar Crit Rate |

## Recomendaciones Específicas

### Por Tipo de Personaje

#### DPS Principales
```
🎯 Prioridad 1: Crit Rate 60-70%
🎯 Prioridad 2: Crit DMG 120-140%
🎯 Prioridad 3: ATK% 112%+
🎯 Prioridad 4: Elemental DMG Bonus
```

#### Sub-DPS
```
🎯 Prioridad 1: Elemental DMG Bonus
🎯 Prioridad 2: Crit Rate 50-60%
🎯 Prioridad 3: Crit DMG 100-120%
🎯 Prioridad 4: Energy Recharge 140-180%
```

#### Support/Healer
```
🎯 Prioridad 1: Energy Recharge 180-250%
🎯 Prioridad 2: HP%/DEF% según personaje
🎯 Prioridad 3: Elemental Mastery
🎯 Prioridad 4: Crit Rate (si aplica)
```

### Mejoras Sugeridas

#### Cuando CV < 160
1. **Cambiar artefactos** con substats pobres
2. **Priorizar piezas** con Crit Rate/DMG
3. **Balancear ratio** 1:2
4. **Considerar armas** con Crit substats

#### Cuando Efficiency < 70%
1. **Farmear nuevos artefactos**
2. **Mejorar substats** existentes
3. **Reemplazar piezas** con stats irrelevantes
4. **Optimizar set bonuses**

## Casos Especiales

### Personajes con Scaling Único

#### Hu Tao (HP Scaling)
- CV importante pero HP% prioritario
- Ratio 1:2 sigue aplicando
- EM valuable para reacciones

#### Itto/Albedo (DEF Scaling)
- DEF% reemplaza ATK% en prioridad
- Crit stats siguen siendo cruciales
- Energy Recharge según rol

#### Kokomi (No Crit)
- CV no aplicable
- HP% y Healing Bonus prioritarios
- Energy Recharge y EM importantes

### Builds Especializadas

#### Elemental Mastery Focus
- EM > 800 para transformative reactions
- Crit stats secundarios
- Energy Recharge según necesidad

#### Energy Recharge Focus
- ER > 200% para burst spam
- Crit stats balanceados
- ATK% o HP%/DEF% según scaling

## Limitaciones del Sistema

### Factores No Considerados
- **Buffs de equipo**: Bennett, Sara, etc.
- **Resonancias elementales**: Pyro, Geo, etc.
- **Armas específicas**: Pasivas únicas
- **Rotaciones**: Uptime de buffs
- **Enemigos**: Resistencias específicas

### Contexto Importante
- Los números son **guías**, no reglas absolutas
- **Prueba en combate** real siempre
- **Adapta según tu equipo** y estilo
- **Considera el contenido** que juegas más

## Ejemplos Prácticos

### Ejemplo 1: DPS Diluc
```
Puntuación: 85/100 (Muy Buena)
Crit Rate: 65% | Crit DMG: 130% | CV: 195
ATK: 2,100 | EM: 150 | ER: 125%

Recomendación: Excelente build balanceada
Mejora sugerida: Subir Crit DMG a 140%+
```

### Ejemplo 2: Support Bennett
```
Puntuación: 78/100 (Buena)
HP: 22,000 | ER: 220% | Healing: +15%
Crit Rate: 45% | Crit DMG: 90%

Recomendación: Excelente support build
Mejora sugerida: Más HP% para healing
```

---

¿Necesitas ayuda interpretando tus resultados específicos? Únete a nuestro [servidor de soporte](/support) donde expertos pueden analizar tu build en detalle.