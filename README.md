# Hormozi Skills en Español: El Motor de Ofertas Irresistibles ($100M+)

**Hormozi Skills** es una factoría automatizada de estrategia comercial y copywriting diseñada para el ecosistema hispanohablante. Permite a agentes de IA (como Claude Code o Codex) actuar como consultores de negocio de élite para estructurar, auditar y vender ofertas de alto valor basándose en la metodología de Alex Hormozi (*$100M Offers* y *$100M Leads*).

![Licencia](https://img.shields.io/badge/licencia-MIT-blue)
![Claude Code](https://img.shields.io/badge/Claude%20Code-compatible-blueviolet)
![Plataforma](https://img.shields.io/badge/plataforma-Claude%20Code%20%7C%20Codex-lightgrey)
![Metodología](https://img.shields.io/badge/metodolog%C3%ADa-Alex%20Hormozi-orange)

---

## ¿Por qué esta versión es única?

Este repositorio no es una simple traducción literal. Se ha rediseñado desde cero con un enfoque de alto impacto para el mercado hispano:

* **Adaptación Cultural y Lingüística:** Redacción fluida, natural y persuasiva en español, ideal para conectar con clientes en Latinoamérica y España.
* **Regla de Redacción Limpia (Sin Em-Dashes):** Los agentes tienen prohibido usar guiones largos (`—`). Los documentos generados utilizan una puntuación clásica y elegante (comas, dos puntos, punto y coma) para garantizar una lectura profesional y limpia.
* **Estructura Optimizada (12 Habilidades):** Las 17 habilidades del repositorio original se han consolidado en **12 módulos estratégicos** más densos y sin redundancias.
* **El "One Pager" de Cierre:** Incluye un 13.º documento de salida que funciona como un resumen ejecutivo ultra condensado de toda tu estrategia comercial.

---

## Inicio Rápido (Instalación)

Puedes utilizar este sistema directamente en tus herramientas de IA favoritas o de forma local.

### Opción A: Claude Code
Para integrar estas habilidades y agentes en tu CLI de Claude Code, añade el marketplace e instala el plugin:

```bash
/plugin marketplace add irvingsoria84/hormozi-skills
/plugin install hormozi-skills@hormozi-skills
```

Una vez instalado, reinicia Claude Code e inicia el orquestador principal escribiendo:
```bash
hormozi-orquestador
```

### Opción B: Codex
Si utilizas Codex, puedes instalar el plugin directamente desde GitHub:

```bash
codex plugin install https://github.com/irvingsoria84/hormozi-skills
```

### Opción C: Instalación Manual
Si prefieres usar los prompts y guías de agentes sin el flujo de plugins, clona la biblioteca y cópiala a tu configuración de Claude:

```bash
# Clona el proyecto
git clone https://github.com/irvingsoria84/hormozi-skills
cd hormozi-skills

# Copia los agentes y habilidades a tu directorio local de Claude
cp -r skills/ agents/ ~/.claude/
```

---

## Arquitectura del Sistema

El proyecto está estructurado bajo un modelo de **dos capas**:

### 1. El Orquestador y los Subagentes
El punto de entrada principal es `hormozi-orquestador`. Este agente evalúa tu estado actual a través de una entrevista estructurada (una pregunta a la vez, ofreciéndote sugerencias rápidas) y delega la redacción a subagentes especialistas según tu etapa del funnel (desde una simple idea hasta un negocio que busca escalar).

```
[Usuario] hormozi-orquestador (Diagnóstico y Entrevista)
 ├── sub-mercado INVESTIGACION_MERCADO.md
 ├── sub-oferta OFERTA.md + ANGULOS_OFERTA.md
 ├── sub-valor AUDITORIA_OFERTA.md + VALOR_PERCIBIDO.md + STACK_BONOS.md
 ├── sub-precios PRECIOS.md + OBJECIONES.md
 └── sub-ventas PITCH.md + GANCHOS.md + PAGINA_VENTAS.md + ONE_PAGER.md
```

### 2. Habilidades Independientes (Skills)
Si no deseas ejecutar el flujo completo del orquestador, puedes llamar a cualquier habilidad de forma individual directamente en tu chat de IA (por ejemplo, `/estrategia-precios` o `/pagina-ventas`).

---

## Entregables: ¿Qué obtienes en `output/`?

Dependiendo de tu punto de partida, el sistema generará hasta 13 documentos estratégicos en tu carpeta `output/`:

| Archivo Generado | Solución Estratégica | Origen |
| :--- | :--- | :--- |
| **`INVESTIGACION_MERCADO.md`** | Nicho validado, dolores profundos y señales reales de demanda. | `sub-mercado` / `/mercado-objetivo` |
| **`OFERTA.md`** | Definición del avatar, mapeo de obstáculos y soluciones clave de tu Oferta Grand Slam. | `sub-oferta` / `/oferta-gran-slam` |
| **`ANGULOS_OFERTA.md`** | 6 a 8 ángulos creativos de posicionamiento ordenados por impacto. | `sub-oferta` / `/angulos-de-oferta` |
| **`AUDITORIA_OFERTA.md`** | Análisis crítico y puntuación detallada de la viabilidad de tu oferta actual. | `sub-valor` / `/auditoria-oferta` |
| **`VALOR_PERCIBIDO.md`** | Ajustes de empaquetado, nomenclatura y valor percibido (Ecuación de Valor). | `sub-valor` / `/valor-percibido` |
| **`STACK_BONOS.md`** | Estructura de bonos diseñados para eliminar la fricción de compra. | `sub-valor` / `/stack-de-bonos` |
| **`PRECIOS.md`** | Modelos de precios anclados en valor y su correspondiente justificación psicológica. | `sub-precios` / `/estrategia-precios` |
| **`OBJECIONES.md`** | Guía de contra-argumentación para anticipar y disolver barreras de compra. | `sub-precios` / `/destructor-objeciones` |
| **`ENTREGA.md`** | Mapeo del mecanismo óptimo (DIY, DWY, DFY), cronograma de entrega y escalabilidad. | `/mecanismo-entrega` |
| **`PITCH.md`** | Versiones corta, mediana y larga del discurso comercial de tu producto. | `sub-ventas` / `/pitch-hormozi` |
| **`GANCHOS.md`** | +30 ganchos de alta conversión clasificados por tipos (curiosidad, identidad, etc.). | `sub-ventas` / `/ganchos-hormozi` |
| **`PAGINA_VENTAS.md`** | Estructura y copy persuasivo completo para tu página de aterrizaje (landing page). | `sub-ventas` / `/pagina-ventas` |
| **`ONE_PAGER.md`** | **Resumen Comercial Ejecutivo:** Tu oferta en un párrafo, decisiones críticas y 3 acciones inmediatas. | `sub-ventas` |

---

## ¿Para quién es esta biblioteca?

* **Fundadores y Creadores:** Que quieren estructurar una oferta de alto valor de forma ágil y validada científicamente.
* **Consultores y Copywriters:** Que buscan un framework riguroso para acelerar la creación de propuestas y páginas de venta para sus clientes.
* **Agentes de Desarrollo e IA:** Que necesitan un conjunto modular de reglas e instrucciones de negocio (basado en prompts y libre de em-dashes) para pipelines automatizados.

---

## Marcos de Trabajo Hormozi Integrados

Este sistema ejecuta en código de prompt las metodologías más famosas de Alex Hormozi:
* **La Ecuación del Valor:** Multiplicar el Resultado Ideal y la Probabilidad Percibida de Logro, mientras se minimiza el Tiempo de Espera y el Esfuerzo/Sacrificio del cliente.
* **La Oferta Grand Slam:** Cómo transformar un servicio genérico en un producto único y difícil de comparar.
* **Estrategias de Garantías:** Diseño de garantías incondicionales, condicionales y basadas en el esfuerzo para eliminar el riesgo del comprador.
* **Anclaje de Precios:** Cómo vender valor real en lugar de competir por tarifas por hora.

---

## Licencia

Este proyecto se distribuye bajo la licencia **MIT** de código abierto. Siéntete libre de adaptarlo, integrarlo a tus plataformas y compartirlo.
