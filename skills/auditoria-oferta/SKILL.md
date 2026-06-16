---
name: auditoria-oferta
description: Audita una oferta existente usando la Ecuación de Valor de Hormozi. Puntúa cada dimensión, identifica los problemas más críticos y define las correcciones prioritarias. Usa cuando una oferta no convierte o cuando quieres saber exactamente qué arreglar primero. Produce AUDITORIA_OFERTA.md.
---

# Habilidad: Auditoría de Oferta

## Propósito

Diagnosticar exactamente qué está roto en una oferta existente usando la Ecuación de Valor de Hormozi, y definir las correcciones prioritarias con mayor impacto.

Regla de escritura obligatoria: nunca uses em-dashes (—) en ningún texto que generes. Usa comas, puntos, dos puntos o punto y coma en su lugar. Todo el contenido debe estar en español.

---

## Cuándo Usar Esta Habilidad

- Una oferta no está convirtiendo y no sabes por qué
- Quieres priorizar qué arreglar antes de invertir en marketing
- Tienes una oferta y quieres un diagnóstico objetivo antes de relanzar
- Recibes objeciones frecuentes y no sabes cómo resolverlas a nivel de oferta

---

## La Ecuación de Valor Hormozi

**Valor = (Resultado Ideal x Probabilidad Percibida) / (Retraso en el Tiempo x Esfuerzo y Sacrificio)**

Para que una oferta convierta bien, necesita:
- Un resultado ideal claro, específico y urgente
- Alta probabilidad percibida de que funciona (prueba, camino claro, credibilidad)
- Poco tiempo hasta el primer resultado (victorias rápidas)
- Bajo esfuerzo y sacrificio percibido

---

## Comportamiento del Asistente

### Paso 1: Recopila la Oferta

Pide al usuario la descripción de su oferta actual. Puede ser:
- Un texto de descripción
- Una URL de página de ventas
- Un documento de oferta existente
- Una descripción verbal

Si existe `output/OFERTA.md`, léelo primero.

---

### Paso 2: Puntúa Cada Dimensión (1 a 10)

Escala:
- 1 a 3: problema crítico
- 4 a 6: necesita mejora
- 7 a 8: sólido
- 9 a 10: fuerte

**10 Dimensiones a Auditar:**

**1. Resultado Ideal**
Preguntas: ¿Es el resultado claro y medible? ¿Es específico? ¿Es urgente para el cliente?
Señales débiles: términos vagos ("crecer", "mejorar", "optimizar"), sin plazo, sin métrica.

**2. Probabilidad Percibida**
Preguntas: ¿Hay testimonios o casos de éxito? ¿Es el proceso creíble? ¿Hay prueba del método?
Señales débiles: promesas sin respaldo, sin resultados de clientes, proceso poco claro.

**3. Retraso en el Tiempo**
Preguntas: ¿Cuándo obtienen el primer resultado? ¿Hay victorias rápidas diseñadas?
Señales débiles: largo proceso antes de ver resultados, sin hito de victoria rápida.

**4. Esfuerzo y Sacrificio**
Preguntas: ¿Se siente difícil de implementar? ¿Hay demasiados pasos? ¿Las instrucciones son confusas?
Señales débiles: proceso complejo, muchos requisitos previos, alta carga de trabajo para el cliente.

**5. Ajuste con el Mercado**
Preguntas: ¿Es la audiencia específica? ¿Es el dolor urgente? ¿Pueden pagar?
Señales débiles: audiencia amplia, problema de baja urgencia, capacidad de pago incierta.

**6. Estructura de Oferta**
Preguntas: ¿Es fácil de entender qué incluye? ¿Está completa? ¿Hay elementos faltantes obvios?
Señales débiles: descripción confusa, falta garantía, falta estructura clara.

**7. Value Stack**
Preguntas: ¿Se muestra claramente el valor total? ¿Son los bonos relevantes? ¿Se apila bien el valor?
Señales débiles: sin bonos, bonos genéricos, sin valor en dólares mostrado.

**8. Precios**
Preguntas: ¿El precio está justificado? ¿Hay anclaje de valor? ¿El precio coincide con el valor prometido?
Señales débiles: precio aleatorio, sin historia de justificación, sin comparación con alternativas.

**9. Mensajes**
Preguntas: ¿Está el lenguaje orientado al resultado? ¿Habla en el idioma del cliente? ¿Es específico?
Señales débiles: lenguaje genérico, habla de características no de resultados, no resuena emocionalmente.

**10. Manejo de Objeciones**
Preguntas: ¿Hay garantía? ¿Están anticipadas las objeciones principales? ¿Se reduce el riesgo percibido?
Señales débiles: sin garantía, sin respuesta a las objeciones más comunes.

---

### Paso 3: Identifica las Correcciones Prioritarias

Ordena las dimensiones por puntuación. Las 3 con menor puntuación son las correcciones prioritarias.

Para cada corrección:
- Describe el problema específico
- Da la acción concreta para solucionarlo
- Estima el impacto en conversiones (alto, medio, bajo)

---

### Paso 4: Puntuación Post-Corrección

Estima cómo quedaría la puntuación si se aplican las 3 correcciones prioritarias.

---

## Output

Escribe `output/AUDITORIA_OFERTA.md` con:
- Puntuación por dimensión con estado
- Puntuación total
- Fortalezas identificadas
- Las 3 correcciones prioritarias con acciones específicas
- Puntuación estimada post-corrección
