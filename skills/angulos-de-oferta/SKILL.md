---
name: angulos-de-oferta
description: Genera múltiples ángulos de posicionamiento para una oferta existente y ayuda a elegir el modelo de negocio correcto. Usa cuando la oferta existe pero no resuena, cuando quieres encontrar un nuevo ángulo de entrada al mercado o cuando necesitas decidir cómo estructurar el modelo de negocio. Produce ANGULOS_OFERTA.md.
---

# Habilidad: Ángulos de Oferta y Modelo de Negocio

## Propósito

Generar múltiples ángulos de posicionamiento para la misma oferta central y seleccionar el modelo de negocio que mejor se ajusta a las restricciones y metas del usuario.

Regla de escritura obligatoria: nunca uses em-dashes (—) en ningún texto que generes. Usa comas, puntos, dos puntos o punto y coma en su lugar. Todo el contenido debe estar en español.

---

## Cuándo Usar Esta Habilidad

- La oferta existe pero no resuena con la audiencia
- Quieres encontrar un ángulo de entrada diferente
- Necesitas decidir cómo estructurar el modelo de negocio
- Quieres reposicionarte para un segmento diferente
- Buscas el ángulo más convincente para una campaña de marketing

---

## Comportamiento del Asistente

### Paso 1: Lee la Oferta Existente

Si existe `output/OFERTA.md`, léelo. Si no, pide al usuario que describa:
- Qué vende
- A quién
- Qué resultado promete
- A qué precio

---

### Paso 2: Genera 6 a 8 Ángulos de Posicionamiento

Para cada ángulo:
- **Nombre del ángulo** (ej. "Ángulo de velocidad")
- **Declaración de posicionamiento** en 1 a 2 líneas
- **A quién le habla mejor**
- **Por qué podría convertir**

**Tipos de ángulos a explorar:**

| Ángulo | Foco |
|--------|------|
| Resultado | El resultado final específico que obtienen |
| Velocidad | Qué tan rápido llegan al resultado |
| Sin esfuerzo | Lo que NO tienen que hacer |
| Mecanismo único | El método diferenciado que lo hace funcionar |
| Contra-intuitivo | Va en contra de lo que creen que necesitan |
| Identidad | En quién se convierten al tenerlo |
| Miedo | El dolor de no actuar ahora |
| Prueba social | Resultados de personas como ellos |

Marca con **"Recomendado"** los 2 ángulos más fuertes.

---

### Paso 3: Evalúa el Modelo de Negocio

Evalúa las tres opciones de entrega principales:

**DIY (Hazlo Tú Mismo)**
- Escala alta, costo de entrega bajo
- Menor valor percibido, menor tasa de completación
- Mejor si: el usuario tiene audiencia, quiere ingresos pasivos o recursos limitados

**DWY (Hazlo Contigo)**
- Mayor tasa de éxito, construye confianza y prueba
- Menos escalable, requiere más tiempo del usuario
- Mejor si: el usuario quiere relaciones, tiene expertise único o está construyendo prueba inicial

**DFY (Hecho Para Ti)**
- Mayor valor percibido, resultados más rápidos para el cliente
- Menor escalabilidad, mayor costo de entrega
- Mejor si: el usuario puede cobrar premium, tiene un proceso probado o el cliente no quiere aprender

O un **Híbrido** con componentes de múltiples modelos.

---

### Paso 4: Recomienda el Modelo Más Adecuado

Considera:
- Restricciones de tiempo del usuario
- Capital disponible
- Metas de ingresos
- Nivel de prueba disponible
- Preferencia de estilo de trabajo

Explica claramente los trade-offs de la recomendación.

---

### Paso 5: Genera Variaciones del Nombre de la Oferta

Para los 2 ángulos recomendados, genera 4 a 6 variaciones de nombre usando el formato MAGIC:

- **M**: hazlo sobre ellos
- **A**: anuncia el avatar
- **G**: da un objetivo claro
- **I**: indica un plazo
- **C**: palabra contenedor (sistema, programa, acelerador, blueprint, bootcamp)

---

## Output

Escribe `output/ANGULOS_OFERTA.md` con:
- Los 6 a 8 ángulos evaluados
- Los 2 ángulos recomendados con justificación
- Evaluación del modelo de negocio con recomendación
- Variaciones de nombre para los ángulos ganadores
