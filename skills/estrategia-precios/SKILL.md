---
name: estrategia-precios
description: Fija precios anclados en el valor que entrega la oferta, no en el costo de producción ni en los precios de la competencia. Diseña una historia de justificación de precio, estructura niveles de precio y sugiere experimentos de precio. Produce PRECIOS.md.
---

# Habilidad: Estrategia de Precios

## Propósito

Fijar precios que reflejen el valor real de la oferta, no el costo de producción ni lo que cobra la competencia. Un precio bien justificado convierte mejor que un precio bajo sin contexto.

Regla de escritura obligatoria: nunca uses em-dashes (—) en ningún texto que generes. Usa comas, puntos, dos puntos o punto y coma en su lugar. Todo el contenido debe estar en español.

---

## Cuándo Usar Esta Habilidad

- No sabes qué precio poner a tu oferta
- Sientes que cobras demasiado poco pero no sabes cómo subirlo
- Tus clientes dicen que es caro pero el resultado es valioso
- Quieres diseñar niveles de precio para diferentes compradores
- Necesitas una historia clara para justificar el precio en ventas

---

## Principio Central

El precio no debe basarse en el tiempo que tardas o en lo que cobra la competencia. Debe basarse en el valor que entrega la oferta al cliente.

Marco: "Si esto ayuda a lograr [resultado], que vale [valor], entonces [precio] es una pequeña fracción de ese valor."

---

## Comportamiento del Asistente

### Paso 1: Lee la Oferta

Si existe `output/OFERTA.md` o `output/STACK_BONOS.md`, léelos. Si no, pide al usuario:
- Qué vende
- Cuál es el resultado principal que promete
- El modelo de entrega (DIY, DWY o DFY)
- A qué tipo de cliente le vende (poder de compra estimado)

---

### Paso 2: Ancla el Precio al Resultado

Calcula el valor que entrega la oferta en 4 dimensiones:

**Dinero ganado**
¿Cuánto ingreso adicional puede generar este resultado al cliente?

**Tiempo ahorrado**
¿Cuántas horas ahorra? Multiplica por el valor estimado de la hora del cliente.

**Dolor evitado**
¿Cuánto cuesta mensualmente NO resolver este problema? (en dinero, tiempo o calidad de vida)

**Oportunidad desbloqueada**
¿Qué se vuelve posible para el cliente cuando logra este resultado?

Suma estas 4 dimensiones para estimar el valor total.

---

### Paso 3: Define el Rango de Precio según el Modelo de Entrega

| Modelo | Rango Orientativo |
|--------|------------------|
| DIY (curso, plantilla, kit) | $27 a $497 |
| DWY (coaching, cohorte, programa grupal) | $500 a $3,000 |
| DFY (agencia, servicio, consultoría) | $1,000 a $10,000 o más |
| Híbrido | Depende del peso del componente DFY |

---

### Paso 4: Define 3 Puntos de Precio

- **Bajo (entrada):** sin riesgo, accesible, decisión por impulso
- **Medio (principal):** la mejor relación valor-precio, el más vendido
- **Alto (premium):** máxima experiencia y soporte, para quienes quieren el camino más rápido

---

### Paso 5: Aplica Precios Psicológicos

**Para ofertas bajo $500:**
Usa precios encantadores ($97, $197, $297, $497). Generan menor resistencia psicológica.

**Para ofertas premium:**
Usa precios redondos ($1,000, $2,500, $5,000). Señalan confianza y no necesitan justificación de "por qué no $1,200".

**Anclaje:**
Siempre muestra el valor total apilado antes del precio. El precio debe parecer una fracción del valor.

---

### Paso 6: Construye la Historia de Justificación del Precio

Escribe una narrativa en 5 pasos para usar en ventas:

1. Reafirma el resultado que promete la oferta
2. Muestra cuánto vale ese resultado (dinero, tiempo, dolor evitado)
3. Compara con la alternativa DIY: cuánto tiempo y dinero cuesta sin guía
4. Muestra el valor total apilado de la oferta
5. Revela el precio como "solo una fracción" del valor total

---

### Paso 7: Diseña Niveles de Precio (si aplica)

Si el usuario quiere múltiples niveles, diseña 3:

**Nivel 1 (Entrada):** para el cliente que quiere empezar con poco riesgo
**Nivel 2 (Principal):** para el cliente que quiere el sistema completo
**Nivel 3 (Premium):** para el cliente que quiere el resultado más rápido con máximo soporte

Para cada nivel: qué incluye, para quién es y precio.

---

### Paso 8: Sugiere Experimentos de Precio

Lista 3 experimentos concretos para encontrar el precio óptimo:
- Test A/B entre dos puntos de precio
- Opción de plan de pago
- Ventana de precio de lanzamiento
- Test de bono vs descuento

---

## Output

Escribe `output/PRECIOS.md` con:
- Anclaje de valor en las 4 dimensiones
- Rango de precio recomendado con el precio central seleccionado
- Estrategia elegida (volumen, margen o híbrido) con justificación
- Historia de justificación del precio lista para usar
- Niveles de precio diseñados (si aplica)
- Experimentos de precio a probar
