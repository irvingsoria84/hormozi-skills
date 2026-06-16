# INSTRUCCIONES DE USO

Bienvenido a **hormozi-skills**, una biblioteca de herramientas de inteligencia artificial para construir ofertas de negocio irresistibles usando los marcos de Alex Hormozi.

Esta guía está pensada para cualquier persona, aunque no tenga experiencia previa con inteligencia artificial.

---

## ¿Qué hace esto?

Describes tu negocio o idea y la IA te entrega una estrategia comercial completa:

- Investigación de tu mercado ideal
- Una oferta estructurada y convincente
- Estrategia de precios justificada
- Respuestas a las objeciones de tus clientes
- Pitch de ventas en tres versiones
- Ganchos para redes sociales y anuncios
- Copy para tu página de ventas
- Un resumen ejecutivo de toda la estrategia en una sola página

---

## Cómo Instalarlo

### Opción 1: Claude Code (la más fácil)

Si usas Claude Code (claude.ai/code), ejecuta estos dos comandos en el chat:

```
/plugin marketplace add irvingsoria84/hormozi-skills
/plugin install hormozi-skills@hormozi-skills
```

Después, reinicia Claude Code y escribe:

```
hormozi-orquestador
```

La IA te guiará paso a paso.

### Opción 2: Codex

Si usas Codex, ejecuta:

```
codex plugin install https://github.com/irvingsoria84/hormozi-skills
```

### Opción 3: Instalación Manual

1. Descarga o clona este repositorio
2. Copia las carpetas `skills/` y `agents/` dentro de la carpeta `.claude/` de tu proyecto o en `~/.claude/` para uso global
3. Reinicia tu plataforma de IA

---

## Cómo Usarlo

### Modo Completo: Orquestador

Escribe `hormozi-orquestador` (o `hormozi-orchestrator` en algunas plataformas).

El orquestador:
1. Te pide que describas tu negocio en lenguaje natural
2. Te hace algunas preguntas enfocadas, una por una
3. Detecta en qué etapa está tu negocio
4. Genera todos los documentos relevantes de forma automática

### Modo Individual: Habilidades Directas

Puedes usar cualquier herramienta por separado sin necesitar el orquestador:

| Quieres... | Escribe... |
|-----------|-----------|
| Encontrar tu mercado ideal | `/mercado-objetivo` |
| Construir tu oferta desde cero | `/oferta-gran-slam` |
| Auditar una oferta que ya tienes | `/auditoria-oferta` |
| Fijar precios con justificación | `/estrategia-precios` |
| Responder objeciones de clientes | `/destructor-objeciones` |
| Crear tu pitch de ventas | `/pitch-hormozi` |
| Generar ganchos para contenido | `/ganchos-hormozi` |
| Escribir tu página de ventas | `/pagina-ventas` |
| Ver un resumen de tu estrategia | Parte del orquestador completo |

---

## Dónde Encuentras los Resultados

Todos los archivos generados se guardan en la carpeta `output/` del directorio donde estés trabajando:

```
output/
├── INVESTIGACION_MERCADO.md
├── OFERTA.md
├── ANGULOS_OFERTA.md
├── AUDITORIA_OFERTA.md
├── VALOR_PERCIBIDO.md
├── STACK_BONOS.md
├── PRECIOS.md
├── OBJECIONES.md
├── PITCH.md
├── GANCHOS.md
├── PAGINA_VENTAS.md
└── ONE_PAGER.md   ← Resumen ejecutivo de toda la estrategia
```

Abre cualquier archivo `.md` con un editor de texto, Notion, Obsidian o cualquier visor de Markdown.

---

## Contexto que Puedes Darle a la IA

Cuanta más información des, mejor será el resultado. Puedes compartir:

- Una descripción de tu negocio en tus propias palabras
- Tu oferta actual (si tienes una)
- El texto de tu página de ventas actual
- Notas o ideas que tengas guardadas
- Incluso una descripción vaga como "ayudo a coaches a conseguir clientes"

Coloca cualquier archivo de contexto en la carpeta `input/` antes de iniciar el orquestador.

---

## Marcos Usados

Este sistema aplica los marcos de Alex Hormozi de sus libros *$100M Offers* y *$100M Leads*:

- Oferta Grand Slam
- Ecuación de valor de Hormozi
- Reversión de obstáculos en soluciones
- Ingeniería de value stack y bonos
- Diseño de garantías
- Anclaje de precio
- Arquitectura de ganchos
