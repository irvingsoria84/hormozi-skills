# CLAUDE.md

Este archivo proporciona instrucciones a Claude Code (claude.ai/code) cuando trabaja con este repositorio.

## Primera Ejecución: Instalación

En el primer uso, pregunta al usuario dónde instalar las habilidades y agentes:

> "¿Dónde debo instalar hormozi-skills?
> - **Proyecto** (predeterminado) — en `.claude/` dentro de la carpeta del proyecto actual. Solo disponible en este proyecto.
> - **Usuario** — en `~/.claude/` en tu directorio de inicio. Disponible en todos los proyectos.
>
> Presiona Enter para usar la opción predeterminada (proyecto)."

**Predeterminado:** nivel de proyecto (`.claude/` en el directorio de trabajo actual).

La instalación copia `skills/` y `agents/` en el directorio `.claude/` elegido:

```bash
# Proyecto (predeterminado)
cp -r skills/ agents/ .claude/

# Usuario (global)
cp -r skills/ agents/ ~/.claude/
```

> [!IMPORTANT]
> Después de la instalación, Claude Code debe reiniciarse para que las nuevas habilidades y agentes estén disponibles.

---

## Qué Es Esto

Una biblioteca de habilidades para que agentes de IA construyan sistemas de oferta inspirados en Hormozi. Sin pipeline de compilación: solo contenido. Cada carpeta en `skills/` es una habilidad independiente de agente; `agents/` contiene un orquestador y cinco subagentes.

## Arquitectura

### Sistema de Dos Capas

**Habilidades** (`skills/<nombre>/SKILL.md`) — independientes, invocables por el usuario. Cada una tiene un frontmatter con `name` y `description`. Algunas tienen una subcarpeta `references/` con material de apoyo que la habilidad lee en tiempo de ejecución.

**Agentes** (`agents/<nombre>.md`) — orquestador + subagentes. El frontmatter incluye `name`, `description`, `tools`, `model` y opcionalmente `color`.

- `hormozi-orquestador` es el punto de entrada. Entrevista al usuario, detecta la etapa del funnel y delega a los subagentes.
- Los subagentes (`sub-mercado`, `sub-oferta`, `sub-valor`, `sub-precios`, `sub-ventas`) son especialistas internos. Solo los invoca el orquestador.

### Reglas de Escritura para Todos los Agentes y Habilidades

- **Sin em-dashes (—):** Usa comas, puntos, dos puntos o punto y coma como alternativas.
- **Todo en español:** Instrucciones, preguntas al usuario, contenido generado y nombres de archivos de salida.
- **Archivos de salida:** Siempre en `output/` con los nombres definidos en cada habilidad.

## Directrices de Estilo para los Outputs

Cuando un agente o habilidad produce documentos, debe:

1. Usar español claro y directo, sin rodeos.
2. Nunca usar el carácter em-dash (—). Reemplazarlo con una coma, dos puntos o punto y coma.
3. Estructurar el contenido con encabezados Markdown.
4. Incluir ejemplos concretos, no generalidades.
5. Hacer que cada sección sea accionable.

## Habilidades Disponibles (12)

| Habilidad | Invocación |
|-----------|-----------|
| Investigación de Mercado | `/mercado-objetivo` |
| Oferta Grand Slam | `/oferta-gran-slam` |
| Ángulos de Oferta | `/angulos-de-oferta` |
| Auditoría de Oferta | `/auditoria-oferta` |
| Valor Percibido | `/valor-percibido` |
| Stack de Bonos | `/stack-de-bonos` |
| Estrategia de Precios | `/estrategia-precios` |
| Destructor de Objeciones | `/destructor-objeciones` |
| Mecanismo de Entrega | `/mecanismo-entrega` |
| Pitch Hormozi | `/pitch-hormozi` |
| Ganchos Hormozi | `/ganchos-hormozi` |
| Página de Ventas | `/pagina-ventas` |

## Agentes Disponibles

- `hormozi-orquestador` — punto de entrada principal
- `sub-mercado` — investigación de mercado (solo uso interno)
- `sub-oferta` — construcción de oferta (solo uso interno)
- `sub-valor` — optimización de valor (solo uso interno)
- `sub-precios` — precios y objeciones (solo uso interno)
- `sub-ventas` — pitch, ganchos, página de ventas y one pager (solo uso interno)

## Archivos de Salida Esperados

Todos en el directorio `output/`:

```
INVESTIGACION_MERCADO.md
OFERTA.md
ANGULOS_OFERTA.md
AUDITORIA_OFERTA.md
VALOR_PERCIBIDO.md
STACK_BONOS.md
PRECIOS.md
OBJECIONES.md
PITCH.md
GANCHOS.md
PAGINA_VENTAS.md
ONE_PAGER.md
```
