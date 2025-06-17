# Verificador KQMC

El **Verificador KQMC** es la característica más avanzada de **Dark-Bot**, diseñada específicamente para analizar y verificar builds de Genshin Impact con precisión profesional.

## 🔍 ¿Qué es KQMC?

**KQMC** (KeqingMains Calculator) es un sistema de análisis que:

- ✅ Verifica la autenticidad de tus artefactos
- 📊 Analiza la distribución de estadísticas
- 🎯 Calcula el potencial de daño real
- 🔧 Detecta posibles mejoras en tu build
- 📈 Compara con builds optimizadas

## 🚀 Uso Básico

### Comando Principal

```
/tc uid:123456789
```

### Parámetros Opcionales

```
/tc uid:123456789 personaje:Hu Tao servidor:America
```

### Parámetros Disponibles

| Parámetro   | Descripción           | Valores                         |
| ----------- | --------------------- | ------------------------------- |
| `uid`       | UID de Genshin Impact | Número de 9 dígitos             |
| `personaje` | Personaje específico  | Nombre del personaje            |
| `servidor`  | Servidor de juego     | America, Europe, Asia, TW/HK/MO |
| `idioma`    | Idioma del reporte    | es, en, zh, ja, ko              |

## 📋 Requisitos Previos

Para usar el verificador correctamente:

::: warning Configuración Necesaria

1. **Showcase visible**: Tu showcase de personajes debe estar público
2. **UID correcto**: Verifica que tu UID sea de 9 dígitos
3. **Personajes equipados**: Los personajes deben tener artefactos equipados
4. **Conexión estable**: El análisis puede tardar 30-60 segundos
   :::

### Hacer tu Showcase Público

1. Abre Genshin Impact
2. Ve a **Perfil** → **Editar información**
3. Activa **"Mostrar detalles de personajes"**
4. Guarda los cambios

## 📊 Interpretando los Resultados

### Ejemplo de Reporte

```
🔧 VERIFICADOR KQMC - Hu Tao
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

👤 Usuario: Viajero#1234
🆔 UID: 123456789
🌟 Nivel: 90 | C1 | Talento: 10/9/9
⚔️ Arma: Bastón de Homa R1 (Niv. 90)

📈 ESTADÍSTICAS PRINCIPALES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
HP: 32,856 | ATK: 1,847 | DEF: 876
CRIT Rate: 68.2% | CRIT DMG: 198.4%
Pyro DMG: 46.6% | EM: 187

🎯 ANÁLISIS DE ARTEFACTOS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🌸 Flor: Crimson Witch ⭐⭐⭐⭐⭐
  ├─ HP: 4,780 (Base)
  ├─ CRIT DMG: 21.0% 🟢
  ├─ CRIT Rate: 10.5% 🟢
  ├─ ATK%: 14.0% 🟡
  └─ DEF: 19 🔴

🪶 Pluma: Crimson Witch ⭐⭐⭐⭐⭐
  ├─ ATK: 311 (Base)
  ├─ CRIT DMG: 25.6% 🟢
  ├─ HP%: 11.7% 🟡
  ├─ EM: 42 🟡
  └─ DEF%: 6.6% 🔴

⏰ Reloj: Crimson Witch ⭐⭐⭐⭐⭐
  ├─ HP%: 46.6% (Main)
  ├─ CRIT Rate: 7.8% 🟢
  ├─ CRIT DMG: 14.8% 🟢
  ├─ ATK%: 9.9% 🟡
  └─ EM: 35 🟡

🏺 Copa: Crimson Witch ⭐⭐⭐⭐⭐
  ├─ Pyro DMG: 46.6% (Main)
  ├─ CRIT DMG: 20.2% 🟢
  ├─ ATK%: 9.3% 🟡
  ├─ HP: 538 🟡
  └─ DEF%: 5.8% 🔴

👑 Circlet: Crimson Witch ⭐⭐⭐⭐⭐
  ├─ CRIT DMG: 62.2% (Main)
  ├─ CRIT Rate: 9.7% 🟢
  ├─ ATK%: 16.3% 🟢
  ├─ HP%: 4.7% 🔴
  └─ EM: 44 🟡

✅ VERIFICACIÓN COMPLETA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🟢 Artefactos: VERIFICADOS
🟢 Estadísticas: CONSISTENTES
🟢 Build: OPTIMIZADA

📊 PUNTUACIÓN FINAL: 8.7/10
```

### Códigos de Color

- 🟢 **Verde**: Estadística excelente
- 🟡 **Amarillo**: Estadística buena/promedio
- 🔴 **Rojo**: Estadística que necesita mejora

### Puntuación

- **9.0-10.0**: Build perfecta
- **8.0-8.9**: Build excelente
- **7.0-7.9**: Build muy buena
- **6.0-6.9**: Build buena
- **5.0-5.9**: Build promedio
- **<5.0**: Build necesita mejoras

## 🔧 Características Avanzadas

### Análisis de Substats

El verificador analiza cada substat para determinar:

- Número de rolls en cada estadística
- Calidad de los rolls (bajo/medio/alto)
- Potencial de mejora

### Detección de Artefactos Mixtos

Identifica automáticamente:

- Artefactos 5★ en sets 4★
- Inconsistencias en las estadísticas
- Posibles errores de configuración

### Comparación con Builds Meta

Compara tu build con:

- Builds optimizadas de la comunidad
- Recomendaciones de KeqingMains
- Estadísticas promedio por personaje

## ❌ Solución de Errores Comunes

### "UID no encontrado"

- Verifica que el UID sea correcto
- Asegúrate de que el showcase esté público
- Espera unos minutos y vuelve a intentar

### "Personaje no encontrado"

- El personaje debe estar en tu showcase
- Verifica que esté equipado con artefactos
- Usa el nombre exacto del personaje

### "Cannot find integer subs"

- Problema con artefactos mixtos (5★ en set 4★)
- El sistema está analizando estadísticas complejas
- Generalmente se resuelve automáticamente

### "Timeout de conexión"

- Los servidores de Genshin pueden estar ocupados
- Intenta en un horario diferente
- Verifica tu conexión a internet

## 🎯 Consejos para Mejores Resultados

### Preparación

1. **Actualiza tu showcase** antes del análisis
2. **Equipa tus mejores artefactos** en el personaje
3. **Usa el arma correcta** para el build
4. **Verifica los talentos** estén al nivel deseado

### Optimización

1. **Prioriza CRIT Rate/DMG** para DPS
2. **Balancea ER** para supports
3. **Considera el arma** en la distribución de stats
4. **Revisa los sets** recomendados para cada personaje

## 📚 Recursos Adicionales

- 📖 [Guía completa del verificador](/kqmc/guide)
- 🎯 [Cómo interpretar resultados](/kqmc/results)
- 🔧 [Solucionar problemas](/kqmc/troubleshooting)
- 💡 [Consejos de optimización](/kqmc/optimization)

---

::: tip ¿Sabías que?
El verificador KQMC procesa más de **1000 análisis diarios** y tiene una precisión del **99.2%** en la detección de artefactos válidos.
:::

¿Tienes problemas con el verificador? Únete a nuestro [servidor de soporte](/support) donde expertos de la comunidad pueden ayudarte a optimizar tus builds.
