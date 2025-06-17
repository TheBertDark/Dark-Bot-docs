# Guía Completa del Verificador KQMC

## ¿Qué es el Verificador KQMC?

El verificador KQMC (Key Quality Metric Calculator) es una herramienta avanzada integrada en Dark-Bot que analiza y evalúa builds de personajes en Genshin Impact.

## Características Principales

### 🎯 Análisis Detallado
- Evaluación de estadísticas principales
- Cálculo de ratios críticos
- Análisis de substats
- Recomendaciones de mejora

### 📊 Métricas Avanzadas
- **Crit Value**: Valor crítico total
- **Efficiency**: Eficiencia de artefactos
- **Potential**: Potencial de mejora
- **Score**: Puntuación general

## Cómo Usar el Verificador

### Comando Básico
```
/tc [personaje] [build]
```

### Parámetros
- `personaje`: Nombre del personaje a analizar
- `build`: Tipo de build (DPS, Support, etc.)

### Ejemplo de Uso
```
/tc Hu Tao DPS
/tc Zhongli Support
/tc Ganyu Freeze
```

## Interpretación de Resultados

### Puntuación General
- **90-100**: Excelente build
- **80-89**: Muy buena build
- **70-79**: Buena build
- **60-69**: Build promedio
- **<60**: Necesita mejoras

### Métricas Específicas

#### Crit Value
Calculado como: `(Crit Rate × 2) + Crit DMG`
- **Óptimo**: >180
- **Bueno**: 160-180
- **Promedio**: 140-160
- **Bajo**: <140

#### Efficiency
Porcentaje de eficiencia de substats
- **Excelente**: >80%
- **Bueno**: 70-80%
- **Promedio**: 60-70%
- **Bajo**: <60%

## Consejos de Optimización

### Prioridades por Rol

#### DPS Principal
1. Crit Rate/DMG balance
2. ATK% y ATK flat
3. Elemental DMG Bonus
4. Energy Recharge (si necesario)

#### Sub-DPS
1. Elemental DMG Bonus
2. Crit Rate/DMG
3. ATK%
4. Energy Recharge

#### Support
1. Energy Recharge
2. HP% o DEF% (según personaje)
3. Elemental Mastery
4. Crit Rate/DMG (si aplica)

### Ratios Recomendados

#### Crit Rate vs Crit DMG
- **Ratio ideal**: 1:2
- **Mínimo Crit Rate**: 50-60%
- **Máximo Crit DMG**: 200-250%

#### Energy Recharge
- **DPS**: 120-140%
- **Sub-DPS**: 140-180%
- **Support**: 180-250%

## Limitaciones del Sistema

### Factores No Considerados
- Sinergias de equipo
- Rotaciones específicas
- Buffs externos
- Situaciones de combate específicas

### Recomendaciones Adicionales
- Usa el verificador como guía, no como verdad absoluta
- Considera el contexto de tu equipo
- Prueba diferentes builds en combate real
- Ajusta según tu estilo de juego

## Solución de Problemas

### Errores Comunes

#### "Personaje no encontrado"
- Verifica la ortografía del nombre
- Usa nombres en inglés o español
- Consulta la lista de personajes soportados

#### "Build no válida"
- Usa tipos de build reconocidos
- Ejemplos: DPS, Support, Healer, Tank

#### "Datos insuficientes"
- Asegúrate de tener artefactos equipados
- Verifica que el personaje esté en tu showcase
- Actualiza tu perfil de Genshin Impact

### Obtener Ayuda

Si tienes problemas con el verificador:
1. Consulta las [preguntas frecuentes](/faq)
2. Revisa la [guía de solución de problemas](/kqmc/troubleshooting)
3. Únete a nuestro [servidor de soporte](/support)

---

¿Necesitas más ayuda? Únete a nuestro [servidor de soporte](/support) donde expertos de la comunidad pueden ayudarte a optimizar tus builds.