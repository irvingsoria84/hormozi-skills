---
name: stack-de-bonos
description: Diseña un stack de bonos estratégicos que destruyen objeciones específicas y elevan el valor percibido de la oferta. Cada bono resuelve una barrera concreta de compra. Produce STACK_BONOS.md.
---

# Habilidad: Stack de Bonos

## Propósito

Diseñar bonos estratégicos que destruyan las objeciones más comunes y eleven el valor percibido de la oferta sin aumentar el costo de entrega.

Un bono bien diseñado no es un regalo. Es una respuesta directa a una razón para no comprar.

Regla de escritura obligatoria: nunca uses em-dashes (—) en ningún texto que generes. Usa comas, puntos, dos puntos o punto y coma en su lugar. Todo el contenido debe estar en español.

---

## Cuándo Usar Esta Habilidad

- La oferta tiene objeciones frecuentes que no se resuelven con el producto principal
- El valor percibido es bajo respecto al precio
- La tasa de conversión es baja y la garantía no es suficiente
- Quieres diferenciar la oferta sin bajar el precio

---

## Principio Central

Los bonos deben seguir el marco **FAST**:
- **F**ast (Rápido): entrega valor inmediato o acelera el resultado principal
- **A**ccurate (Preciso): resuelve una objeción específica, no general
- **S**imple: fácil de consumir e implementar
- **T**angible: se puede ver, usar o implementar directamente

---

## Comportamiento del Asistente

### Paso 1: Lee la Oferta y las Objeciones

Si existe `output/OFERTA.md`, léelo. Si existe `output/OBJECIONES.md`, léelo también. Si no, pide al usuario:
- Qué vende
- Cuáles son las objeciones más frecuentes que escucha
- Qué hace que los clientes duden o no compren

---

### Paso 2: Mapea las Objeciones más Frecuentes

Lista las 5 a 8 objeciones más comunes. Ejemplos genéricos:
- "No tengo tiempo para implementarlo"
- "¿Y si no funciona para mi caso?"
- "Ya intenté algo parecido antes"
- "No sé si puedo hacerlo yo solo"
- "Necesito saber más antes de decidir"
- "Es demasiado caro para lo que es"
- "No confío todavía en el método"

Pregunta al usuario qué objeciones escucha realmente. Esas son las que mandan.

---

### Paso 3: Diseña un Bono por Objeción

Para cada objeción, diseña un bono que la destruya directamente.

El bono puede ser:
- Una plantilla lista para usar
- Un checklist de implementación rápida
- Un ejemplo real o caso de estudio
- Una sesión de preguntas y respuestas grabada
- Un recurso de referencia rápida
- Un proceso paso a paso simplificado
- Una herramienta de diagnóstico

**Patrón de nombre de bono:**
[Adjetivo poderoso] + [Resultado] + [Formato]

Ejemplos:
- "Guía de Arranque Rápido: Tus Primeras 48 Horas"
- "Plantilla Probada de Propuesta que Convierte"
- "Checklist de Verificación: Cómo Saber si Esto es para Ti"
- "Biblioteca de Casos de Éxito de [Avatar]"

---

### Paso 4: Aplica el Marco FAST a Cada Bono

Para cada bono diseñado, verifica:
- ¿Entrega valor en menos de 24 horas? (F)
- ¿Resuelve una objeción específica, no vaga? (A)
- ¿Se puede consumir en 15 a 30 minutos? (S)
- ¿El cliente puede usarlo o ver el resultado inmediatamente? (T)

Si no pasa el filtro FAST, rediseña el bono.

---

### Paso 5: Ponle Valor Percibido a Cada Bono

Asigna un valor percibido justo en dólares o pesos. Base para calcular:
- ¿Cuánto costaría contratar a alguien para obtener este recurso?
- ¿Cuánto tiempo ahorra al cliente?
- ¿Cuánto cuesta la alternativa DIY?

---

### Paso 6: Construye el Value Stack Completo

Suma el valor de todos los bonos al valor de la oferta principal. Presenta el total apilado antes del precio real.

Formato:
```
Oferta principal: $[valor]
+ Bono 1 "[Nombre]": $[valor]
+ Bono 2 "[Nombre]": $[valor]
+ Bono 3 "[Nombre]": $[valor]
Total: $[total]
Precio hoy: $[precio real]
```

---

## Output

Escribe `output/STACK_BONOS.md` con:
- Tabla de objeciones y bono asignado a cada una
- Descripción completa de cada bono (qué incluye, formato, valor percibido, por qué funciona)
- Verificación FAST de cada bono
- Value stack completo con total apilado y precio
