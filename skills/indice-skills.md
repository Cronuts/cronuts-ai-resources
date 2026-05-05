# Skills de Claude Code — Índice

Skills instaladas en Claude Code del equipo. Cada una añade capacidades especializadas al asistente.

> **¿Qué es una skill?** Un módulo que expande lo que Claude puede hacer: desde generar interfaces UI hasta hacer scraping web o auditar seguridad. Se instala una vez y está disponible en todas las conversaciones.

---

## Cómo instalar una skill

Ver guía completa: [Cómo instalar skills y agents](../guias/como-instalar-skills-agents.md)

Comando rápido en Claude Code:
```
/install-skill [nombre-skill]
```

---

## Skills disponibles

### Diseño y Frontend

#### `ui-ux-pro-max` ⭐
**Lo que hace:** Diseño UI/UX de alto nivel. Genera interfaces con 67 estilos visuales, 96 paletas de color, 57 combinaciones de tipografía y 25 tipos de gráficos. Soporta React, Next.js, Vue, Svelte, SwiftUI, React Native, Flutter, Tailwind y shadcn/ui.

**Cuándo usar:** Crear una pantalla nueva, diseñar un componente, explorar estilos visuales, prototipar una UI rápido.

**Cómo activar:** Escribe `/ui-ux-pro-max` o describe lo que quieres diseñar y Claude lo detecta automáticamente.

**Versión instalada:** 2.5.0

---

#### `frontend-design`
**Lo que hace:** Crea interfaces frontend distintivas y listas para producción. Foco en calidad de diseño: landing pages, dashboards, componentes React, aplicaciones web.

**Cuándo usar:** Cuando necesitas una UI completa con alta calidad visual, no solo funcional.

---

#### `senior-frontend`
**Lo que hace:** Desarrollo frontend avanzado con ReactJS, NextJS, TypeScript y Tailwind CSS. Incluye scaffolding de componentes, optimización de rendimiento y análisis de bundles.

**Cuándo usar:** Proyectos de frontend en producción que necesitan arquitectura sólida, optimización y buenas prácticas.

---

#### `refero-design`
**Lo que hace:** Metodología de diseño Research-First usando Refero MCP. Busca referencias de UI reales antes de diseñar: pantallas, flows y patrones de productos existentes.

**Cuándo usar:** Al empezar un diseño nuevo, especialmente cuando necesitas referencias de cómo lo resuelven otras apps.

**Requiere:** MCP de Refero configurado.

---

### Scraping y Automatización

#### `apify-ultimate-scraper` ⭐
**Lo que hace:** Scraper universal con IA. Extrae datos de Instagram, Facebook, TikTok, YouTube, Google Maps, Google Search, Google Trends, Booking.com y TripAdvisor.

**Casos de uso:** Generación de leads, monitorización de marca, análisis de competidores, investigación de influencers, análisis de tendencias, extracción de datos para research.

**Cuándo usar:** Cuando necesitas datos de cualquiera de estas plataformas sin escribir código.

---

#### `apify-actor-development`
**Lo que hace:** Desarrolla, depura y despliega Apify Actors: programas serverless en la nube para scraping web, automatización y procesamiento de datos.

**Cuándo usar:** Cuando necesitas un scraper o automatización personalizada que no cubre `apify-ultimate-scraper`.

---

#### `apify-actorization`
**Lo que hace:** Convierte proyectos existentes en Apify Actors. Soporta JavaScript/TypeScript, Python y cualquier lenguaje con un wrapper CLI.

**Cuándo usar:** Tienes un script de scraping o procesamiento y quieres convertirlo en un Actor desplegable en Apify.

---

#### `apify-generate-output-schema`
**Lo que hace:** Genera schemas de output para Apify Actors analizando el código fuente (dataset_schema.json, output_schema.json, key_value_store_schema.json).

**Cuándo usar:** Al crear o actualizar un Actor de Apify y necesitas documentar su output.

---

### SEO y Contenido

#### `schema-markup`
**Lo que hace:** Añade, corrige y optimiza schema markup y datos estructurados (JSON-LD). Soporta FAQ schema, product schema, review schema y más tipos de schema.org.

**Cuándo usar:** Quieres mejorar rich snippets en Google, implementar structured data o validar que el schema existente es correcto.

---

### Seguridad

#### `mcp-sentinel`
**Lo que hace:** Monitorización de seguridad para skills y MCP servers. Escanea contra múltiples bases de datos de vulnerabilidades (GitHub Advisory DB, CVE feeds, mcpscan.ai, Snyk) y alertas comunitarias.

**Cuándo usar:** Antes de instalar un MCP server nuevo, o para auditar los que ya tienes instalados.

---

### Productividad y Comunicación

#### `caveman`
**Lo que hace:** Modo de comunicación ultra-comprimido. Reduce ~75% el uso de tokens manteniendo precisión técnica. Varios niveles: lite, full, ultra, y variantes en chino clásico (wenyan).

**Cuándo usar:** Conversaciones técnicas largas donde quieres respuestas densas y sin relleno.

**Activar:** Escribe `/caveman` (full por defecto) o `/caveman lite|ultra`.

---

#### `caveman-commit`
**Lo que hace:** Genera mensajes de commit ultra-comprimidos en formato Conventional Commits. Sujeto ≤50 chars, cuerpo solo cuando el "por qué" no es obvio.

**Cuándo usar:** Al hacer commits — `/caveman-commit`.

---

#### `caveman-review`
**Lo que hace:** Reviews de código ultra-comprimidos. Cada comentario: ubicación, problema, fix. Sin relleno.

**Cuándo usar:** Revisar PRs rápido — `/caveman-review`.

---

#### `compress`
**Lo que hace:** Comprime archivos de memoria en lenguaje natural (CLAUDE.md, todos, preferencias) a formato caveman para ahorrar tokens. Guarda backup del original.

**Cuándo usar:** Tu CLAUDE.md o archivos de contexto son muy grandes y quieres reducirlos.

---

#### `find-skills`
**Lo que hace:** Ayuda a descubrir e instalar skills cuando no sabes cuál usar para una tarea. Busca en el marketplace y recomienda según tu necesidad.

**Cuándo usar:** "¿Existe alguna skill para X?" — actívala con `/find-skills`.

---

## Instalar todas las skills del equipo

Ver: [Guía de instalación](../guias/como-instalar-skills-agents.md)