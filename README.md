# hormozi-skills

**Convierte cualquier idea de negocio en una oferta completa y vendible usando los marcos de Alex Hormozi.**

![Licencia](https://img.shields.io/badge/licencia-MIT-blue)
![Claude Code](https://img.shields.io/badge/Claude%20Code-compatible-blueviolet)
![Plataforma](https://img.shields.io/badge/plataforma-Claude%20Code%20%7C%20Codex-lightgrey)
![Inspirado por](https://img.shields.io/badge/inspirado%20por-Alex%20Hormozi-orange)

---

> Biblioteca de habilidades para agentes de IA. Descríbele tu negocio y obtén un sistema de oferta completo: investigación de mercado, estructura de oferta, precios, pitch, ganchos, página de ventas y un resumen ejecutivo, todo escrito en archivos en una sola sesión.

---

## El Problema

Construir una oferta convincente es difícil. La mayoría de fundadores, coaches y consultores:

- Escriben ofertas vagas que no convierten: *"Ayudo a las personas a hacer crecer su negocio"*
- Ponen precios incorrectos: demasiado bajos para ser tomados en serio o demasiado altos sin justificación
- Omiten la capa de ventas: sin ganchos, sin pitch, sin copy de página de ventas

**hormozi-skills** resuelve esto de extremo a extremo. Un orquestador, cinco subagentes especializados, 12 habilidades, 13 archivos de salida.

---

## Inicio Rápido

### Claude Code

Agrega el marketplace e instala el plugin:

```bash
/plugin marketplace add irvingsoria84/hormozi-skills
/plugin install hormozi-skills@hormozi-skills
```

Luego invoca el agente orquestador o una habilidad específica:

```bash
hormozi-orquestador
```

### Codex

Instala directamente desde GitHub:

```bash
codex plugin install https://github.com/irvingsoria84/hormozi-skills
```

### Instalación Manual

Si prefieres los archivos de habilidades sin el flujo de plugin:

```bash
# Clona la biblioteca
git clone https://github.com/irvingsoria84/hormozi-skills
cd hormozi-skills

# Copia habilidades y agentes a tu configuración de Claude
cp -r skills/ agents/ ~/.claude/
```

> [!TIP]
> Describe tu negocio en lenguaje natural: una idea en borrador, un brain dump o tu oferta actual. El orquestador te entrevista, detecta tu etapa y construye todo desde ahí.

---

## Lo Que Obtienes

13 archivos de salida escritos en `output/` en una sola sesión:

| Archivo | Contenido |
|---------|-----------|
| `INVESTIGACION_MERCADO.md` | Nicho validado, mapa de dolores, señales de demanda |
| `OFERTA.md` | Oferta Grand Slam completa: avatar, obstáculos, mapa de soluciones, value stack |
| `ANGULOS_OFERTA.md` | 6 a 8 ángulos de posicionamiento, ordenados por potencia |
| `AUDITORIA_OFERTA.md` | Puntuación por dimensión y correcciones prioritarias |
| `VALOR_PERCIBIDO.md` | Naming mejorado, empaquetado, encuadre y percepción de valor |
| `STACK_BONOS.md` | Estructura de bonos que destruye objeciones con valor percibido |
| `PRECIOS.md` | Precio anclado en valor, niveles, historia de justificación |
| `OBJECIONES.md` | Creencias ocultas, cambios de creencia, respuestas listas para usar |
| `PITCH.md` | Versiones corta, media y larga del pitch |
| `GANCHOS.md` | 30 o más ganchos en 8 tipos, ordenados por impacto |
| `PAGINA_VENTAS.md` | Copy completo de página de ventas, sección por sección |
| `ONE_PAGER.md` | Resumen ejecutivo ultra condensado de toda la estrategia comercial |

---

## Biblioteca de Habilidades

Usa cualquier habilidad de forma independiente, sin necesitar el orquestador:

| Habilidad | Propósito | Output |
|-----------|-----------|--------|
| `mercado-objetivo` | Valida tu nicho y extrae dolor real del mercado | INVESTIGACION_MERCADO.md |
| `oferta-gran-slam` | Construye una oferta Grand Slam desde cualquier idea | OFERTA.md |
| `angulos-de-oferta` | Genera ángulos de posicionamiento y modelo de negocio | ANGULOS_OFERTA.md |
| `auditoria-oferta` | Audita y puntúa una oferta existente | AUDITORIA_OFERTA.md |
| `valor-percibido` | Aumenta la percepción de valor, reduce fricción | VALOR_PERCIBIDO.md |
| `stack-de-bonos` | Diseña bonos que eliminan objeciones | STACK_BONOS.md |
| `estrategia-precios` | Fija precios anclados en valor con justificación | PRECIOS.md |
| `destructor-objeciones` | Identifica y destruye objeciones clave | OBJECIONES.md |
| `mecanismo-entrega` | Elige el modelo de entrega y escala | ENTREGA.md |
| `pitch-hormozi` | Escribe pitch de ventas en 3 versiones | PITCH.md |
| `ganchos-hormozi` | Genera ganchos de alto impacto para contenido y anuncios | GANCHOS.md |
| `pagina-ventas` | Escribe el copy completo de tu página de ventas | PAGINA_VENTAS.md |

> [!TIP]
> Omite el orquestador y llama cualquier habilidad directamente: `/auditoria-oferta`, `/estrategia-precios`, `/pagina-ventas`. Cada una funciona sola sin contexto previo.

---

## Sistema de Agentes

```
hormozi-orquestador
├── sub-mercado    → INVESTIGACION_MERCADO.md
├── sub-oferta     → OFERTA.md + ANGULOS_OFERTA.md
├── sub-valor      → AUDITORIA_OFERTA.md + VALOR_PERCIBIDO.md + STACK_BONOS.md
├── sub-precios    → PRECIOS.md + OBJECIONES.md
└── sub-ventas     → PITCH.md + GANCHOS.md + PAGINA_VENTAS.md + ONE_PAGER.md
```

Orden de dependencia: mercado → oferta → (valor en paralelo con precios) → ventas

El orquestador detecta tu etapa del funnel (idea, oferta rota, necesita capa de ventas, escalado de servicio) y ejecuta solo los subagentes que necesitas.

---

## Como Funciona

1. **Recepción** — Dale al orquestador cualquier cosa: una idea cruda, tu oferta actual, un brain dump o una página de ventas
2. **Entrevista** — Preguntas enfocadas, de una en una, cada una con una respuesta sugerida
3. **Detección de etapa** — Clasifica tu situación (Etapa A a E), muestra qué subagentes se ejecutarán
4. **Delegación** — Lanza subagentes en orden de dependencia, pasando briefs estructurados
5. **Resumen** — Produce `output/ONE_PAGER.md`: oferta en un párrafo, decisiones clave, 3 acciones principales, mejor gancho para usar hoy

---

## Estructura del Repositorio

```
hormozi-skills/
├── skills/    # 12 habilidades independientes para agentes
├── agents/    # Orquestador + 5 subagentes
├── output/    # Documentos generados (comienza vacío)
└── input/     # Coloca aquí tus ofertas, notas o páginas de ventas existentes
```

---

## Para Quién Es Esto

- Fundadores, coaches, consultores y freelancers construyendo ofertas
- Cualquiera que aplique la metodología Hormozi y quiera ejecución con IA, no solo consejos
- Agentes de codificación que ejecutan pipelines de generación de ofertas

## Para Quién No Es

- Redactores genéricos que buscan plantillas de llenar: este sistema piensa, no solo rellena
- Desarrolladores que necesitan una biblioteca de código: esto es basado en prompts, nativo para agentes
- Personas que quieren una respuesta única sin iteración: el orquestador te entrevista

---

## Marcos de Referencia

Construido sobre la metodología de ofertas de Alex Hormozi de *$100M Offers* y *$100M Leads*:

- Construcción de la Oferta Grand Slam
- Ecuación de valor: resultado ideal x probabilidad percibida / retraso en el tiempo x esfuerzo y sacrificio
- Reversión de obstáculos en soluciones
- Ingeniería de value stack y bonos
- Diseño de garantías (incondicional, condicional, basada en esfuerzo)
- Anclaje de precio y valor percibido
- Arquitectura de ganchos (interrupción de patrón, identidad, resultado, curiosidad)

---

## Créditos

Inspirado en el trabajo de Alex Hormozi. Adaptado al español para agentes de IA.
