# Cronuts AI Resources

Centro de recursos compartidos de IA para el equipo de Cronuts: prompts, agents, skills, plantillas y guías.

> Si creas algo útil, compártelo. Este repositorio vale lo que el equipo le ponga.

---

## Empieza aquí

| Quiero... | Ir a |
|-----------|------|
| Usar un prompt listo para mi área | [`/prompts`](./prompts/) |
| Instalar un agente especializado en Claude Code | [`/agents`](./agents/) + [guía de instalación](./guias/como-instalar-skills-agents.md) |
| Instalar una skill en Claude Code | [`/skills`](./skills/) + [guía de instalación](./guias/como-instalar-skills-agents.md) |
| Conectar Claude a Notion, Drive, Slack... | [Guía de MCPs](./guias/guia-mcps.md) |
| Contribuir un recurso nuevo | [Plantilla estándar](./plantillas/plantilla-recurso.md) |
| Primera vez en GitHub | [Cómo usar este repo](./guias/como-usar-este-repo.md) |

---

## Prompts por área

Listos para copiar y usar. Sustituye los `[corchetes]` con tu contexto.

### Producto
| Prompt | Para qué |
|--------|---------|
| [Redactar PRD](./prompts/producto/prompt-redactar-prd.md) | PRD completo desde un brief inicial |
| [User Stories](./prompts/producto/prompt-user-stories.md) | Historias de usuario con criterios Gherkin |
| [Análisis de competencia](./prompts/producto/prompt-analisis-competencia.md) | Benchmarking competitivo estructurado |
| [Síntesis de user research](./prompts/producto/prompt-sintesis-user-research.md) | Patrones e insights desde notas de entrevistas |
| [Priorización de features](./prompts/producto/prompt-priorizacion-features.md) | RICE + MoSCoW con justificación |
| [Comunicación a stakeholders](./prompts/producto/prompt-comunicacion-stakeholders.md) | Updates, cambios de roadmap, decisiones |

### Copywriting
| Prompt | Para qué |
|--------|---------|
| [Newsletter](./prompts/copywriting/prompt-newsletter.md) | Redacción de newsletters |

> ¿Eres de Growth, Contenidos, Social Media o Paid Media? Esta carpeta es tuya — [añade tus prompts](./guias/como-usar-este-repo.md).

---

## Agents

Asistentes especializados para Claude Code. Se instalan una vez y Claude los activa automáticamente.

→ [Cómo instalar agents](./guias/como-instalar-skills-agents.md)

| Agent | Área | Para qué |
|-------|------|---------|
| [frontend-developer](./agents/desarrollo/frontend-developer.md) | Desarrollo | Apps frontend completas: React, Vue, Angular, TypeScript |
| [wordpress-master](./agents/desarrollo/wordpress-master.md) | Desarrollo | WordPress: rendimiento, WooCommerce, headless CMS |
| [seo-analyzer](./agents/marketing/seo-analyzer.md) | Marketing / Growth | Auditorías SEO técnicas, Core Web Vitals, schema markup |
| [security-auditor](./agents/seguridad/security-auditor.md) | Transversal | Auditorías de seguridad, compliance SOC2/ISO27001/PCI DSS |
| [agent-investigador-producto](./agents/agent-investigador-producto.md) | Producto | Research de producto: mercado, competencia, user insights |

---

## Skills

Módulos de capacidades para Claude Code. Cada skill añade habilidades especializadas al asistente.

→ [Índice completo de skills](./skills/indice-skills.md) · [Cómo instalar skills](./guias/como-instalar-skills-agents.md)

| Skill | Para qué |
|-------|---------|
| [ui-ux-pro-max](./skills/ui-ux-pro-max/) | Diseño UI/UX: 67 estilos, 96 paletas, 13 frameworks |
| [frontend-design](./skills/frontend-design/) | Interfaces frontend de alta calidad visual |
| [senior-frontend](./skills/senior-frontend/) | Desarrollo frontend avanzado con Next.js, TypeScript, Tailwind |
| [refero-design](./skills/refero-design/) | Diseño research-first con referencias de UI reales |
| [apify-ultimate-scraper](./skills/apify-ultimate-scraper/) | Scraping de Instagram, TikTok, Google Maps, YouTube... |
| [apify-actor-development](./skills/apify-actor-development/) | Desarrollo de Apify Actors personalizados |
| [schema-markup](./skills/schema-markup/) | SEO estructurado: JSON-LD, rich snippets |
| [mcp-sentinel](./skills/mcp-sentinel/) | Seguridad: auditoría de MCPs y skills instalados |
| [caveman](./skills/caveman/) | Respuestas ultra-comprimidas, menos tokens |
| [compress](./skills/compress/) | Comprime archivos de contexto para ahorrar tokens |
| [find-skills](./skills/find-skills/) | Descubre e instala skills del marketplace |

---

## MCPs — Claude conectado a tus herramientas

Con los MCPs, Claude opera directamente en Notion, Drive, Slack, Gmail, Calendar, Figma, Make y Gamma.

→ [Guía completa de MCPs por equipo](./guias/guia-mcps.md)

| MCP | Growth | Producto | Contenidos | Paid Media |
|-----|:------:|:--------:|:----------:|:----------:|
| Notion | ✓ | ✓ | ✓ | ✓ |
| Google Drive | ✓ | ✓ | ✓ | ✓ |
| Gmail | ✓ | ✓ | — | ✓ |
| Google Calendar | ✓ | ✓ | ✓ | ✓ |
| Make | ✓ | ✓ | — | ✓ |
| Slack | ✓ | ✓ | ✓ | ✓ |
| Figma | — | ✓ | ✓ | — |
| Gamma | ✓ | ✓ | ✓ | ✓ |

---

## Plantillas

| Plantilla | Para qué |
|-----------|---------|
| [Plantilla de recurso](./plantillas/plantilla-recurso.md) | Base para añadir cualquier recurso a este repo |
| [Plantilla de PRD](./plantillas/plantilla-prd.md) | PRD completo con todas las secciones |

---

## Guías

| Guía | Para qué |
|------|---------|
| [Guía de MCPs](./guias/guia-mcps.md) | Qué MCPs hay, qué puede hacer Claude con cada uno y cómo configurarlos |
| [Cómo instalar skills y agents](./guias/como-instalar-skills-agents.md) | Instalar recursos en Claude Code paso a paso |
| [Buenas prácticas de prompts](./guias/buenas-practicas-prompts.md) | Cómo escribir prompts que realmente funcionen |
| [Cómo usar este repo](./guias/como-usar-este-repo.md) | Para quienes no han usado GitHub antes |

---

## Cómo contribuir

1. Navega a la carpeta correcta
2. Crea un archivo `.md` siguiendo la [plantilla estándar](./plantillas/plantilla-recurso.md)
3. Abre una Pull Request con descripción de para qué sirve

*Última actualización: Mayo 2026*
