# Guía de MCPs — Claude conectado a tus herramientas

Los MCP (Model Context Protocol) permiten que Claude opere directamente dentro de tus herramientas: leer y escribir en Notion, mover archivos en Drive, crear eventos en Calendar, enviar mensajes en Slack y mucho más.

No es magia: Claude actúa sobre lo que le pides, con las mismas restricciones de permisos que tiene tu cuenta. Tú siempre confirmas antes de que haga algo irreversible.

---

## Cómo activar los MCPs

1. Entra en [claude.ai](https://claude.ai) con tu cuenta de Cronuts
2. Ve a **Configuración → Integraciones** (o el ícono de enchufes en el panel lateral)
3. Conecta cada herramienta con tu cuenta — solo hay que hacerlo una vez
4. En cualquier conversación, Claude ya puede usar las herramientas conectadas

> Los MCPs funcionan en **claude.ai** (web/app). Para Claude Code, se configuran en `~/.claude/mcp_servers.json`.

---

## MCPs disponibles y qué puede hacer Claude con ellos

---

### Notion

**Qué puede hacer Claude:**
- Buscar páginas y bases de datos por nombre o contenido
- Leer el contenido de cualquier página a la que tengas acceso
- Crear páginas nuevas en cualquier sección
- Actualizar páginas existentes: editar texto, cambiar propiedades, añadir bloques
- Consultar y filtrar bases de datos
- Crear comentarios en páginas

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Producto** | Actualizar PRDs, añadir notas a tickets, consultar roadmap, crear páginas de research |
| **Growth** | Registrar experimentos, actualizar trackers de OKRs, consultar el pipeline |
| **Contenidos** | Gestionar el calendario editorial, crear briefs, actualizar estado de piezas |
| **Paid Media** | Registrar resultados de campañas, actualizar trackers de presupuesto |

**Ejemplos:**
> "Busca en Notion la página del roadmap Q2 y dime qué features están en estado 'En progreso'"

> "Crea una nueva página en la sección de Research con el título 'Síntesis entrevistas — [Proyecto]' y añade esta estructura: [pega estructura]"

---

### Google Drive

**Qué puede hacer Claude:**
- Buscar archivos por nombre, tipo o contenido
- Leer documentos, hojas de cálculo y presentaciones
- Crear archivos nuevos (docs, sheets)
- Editar y actualizar contenido de archivos existentes
- Copiar archivos y consultar permisos

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Producto** | Buscar specs antiguas, leer datos exportados, crear documentos de briefing |
| **Growth** | Leer exports de campañas, actualizar hojas de resultados, consolidar datos |
| **Content Manager / Social Media** | Buscar assets, leer el calendario de contenidos, crear guiones |
| **Filmmaker** | Buscar briefs de vídeo, leer guiones, crear documentos de producción |
| **Paid Media** | Leer informes de rendimiento, actualizar hojas de seguimiento de presupuesto |

**Ejemplos:**
> "Busca en Drive el documento 'Informe mensual abril' y dame un resumen ejecutivo de los KPIs principales"

> "Crea una hoja de cálculo en la carpeta 'Campañas 2026' con las columnas: Campaña, Canal, Presupuesto, Impresiones, Clicks, CPC, Conversiones"

---

### Gmail

**Qué puede hacer Claude:**
- Leer emails (búsqueda por remitente, asunto, fecha)
- Redactar borradores listos para revisar y enviar
- Resumir hilos de conversación

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Producto** | Resumir feedback de clientes recibido por email, preparar respuestas |
| **Growth** | Analizar respuestas a campañas de outreach, redactar follow-ups |
| **Paid Media** | Resumir comunicaciones con proveedores, redactar informes para clientes |
| **Todos** | Redactar emails profesionales, resumir hilos largos |

**Ejemplos:**
> "Lee los últimos 5 emails de [cliente] y dame un resumen de qué pide y el tono de la conversación"

> "Redacta un email de seguimiento para [nombre] tras la reunión de hoy. Puntos clave: [lista]"

---

### Google Calendar

**Qué puede hacer Claude:**
- Leer eventos del calendario (próximos, por fecha, por persona)
- Crear eventos nuevos con invitados, descripción y duración
- Buscar disponibilidad

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Producto** | Crear eventos de review, sprint planning, sesiones de user research |
| **Contenidos** | Programar reuniones de planificación editorial |
| **Todos** | Planificar reuniones, buscar hueco libre en la agenda |

**Ejemplo:**
> "Crea un evento 'Revisión de PRD — Feature X' para el jueves a las 10h, duración 1h, e invita a [emails]"

---

### Make (Integromat)

**Qué puede hacer Claude:**
- Ejecutar escenarios de automatización existentes
- Leer y consultar data stores
- Crear y actualizar registros en data stores
- Ver el estado de ejecuciones pasadas
- Listar escenarios activos

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Producto** | Ejecutar escenarios de automatización de producto, consultar y actualizar data stores, disparar notificaciones |
| **Growth** | Lanzar automatizaciones de lead generation, consultar datos del CRM automatizado |
| **Paid Media** | Ejecutar pipelines de reporte, actualizar datos de campañas |
| **Contenidos** | Lanzar flujos de publicación, activar workflows de distribución |

**Ejemplos:**
> "Ejecuta el escenario 'Sync leads CRM' y dime el resultado"

> "Consulta el data store de campañas y dame los registros donde el estado sea 'activo'"

---

### Slack

**Qué puede hacer Claude:**
- Enviar mensajes a canales o personas
- Leer mensajes recientes de un canal

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Todos** | Enviar updates de proyecto, notificaciones automáticas, resúmenes de reunión |

**Ejemplo:**
> "Envía al canal #producto un resumen de los cambios del roadmap de esta semana: [lista de cambios]"

---

### Figma

**Qué puede hacer Claude:**
- Acceder a archivos de diseño
- Leer la estructura de componentes y capas
- Extraer información de diseños (textos, colores, estilos)

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Lead Designer** | Auditar consistencia de componentes, documentar el design system |
| **Producto** | Leer diseños para escribir specs técnicas precisas |
| **Content Manager** | Consultar assets disponibles, leer copies en los diseños |

**Ejemplo:**
> "Accede al archivo 'App v3 — Diseño' y lista todos los textos de los botones principales"

---

### Gamma

**Qué puede hacer Claude:**
- Crear presentaciones completas a partir de un brief o contenido

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Producto** | Presentaciones de roadmap, decks de features para stakeholders |
| **Growth** | Decks de resultados, propuestas |
| **Paid Media** | Informes de campaña en formato presentación |
| **Todos** | Cualquier presentación rápida |

**Ejemplo:**
> "Crea una presentación en Gamma con el título 'Resultados Q1 2026' y estas secciones: [lista]"

---

### draw.io

**Qué puede hacer Claude:**
- Crear y editar diagramas: flujos, arquitecturas, mapas de proceso, user journeys

**Por equipo:**

| Equipo | Casos de uso |
|--------|-------------|
| **Producto** | User journeys, flows de producto, arquitecturas de features |
| **Growth** | Mapas de funnel, diagramas de experimentos |
| **Todos** | Cualquier diagrama de proceso o flujo |

**Ejemplo:**
> "Crea un diagrama de flujo del proceso de onboarding con estos pasos: [lista]"

---

## Combina herramientas en una sola conversación

El mayor valor de los MCPs no es usar uno solo — es encadenarlos:

> "Lee el brief en Drive, crea la página en Notion con el contenido estructurado y avisa en el canal #contenidos de Slack cuando esté lista"

> "Busca en Notion las notas de las últimas 3 entrevistas de usuario, redacta un resumen y guárdalo en Drive en la carpeta 'Research'"

> "Mira mi calendario de esta semana, identifica huecos de 1h para una reunión con [persona] y crea el evento con agenda incluida"

---

## Tips

- **Nombra exacto**: Claude busca por texto. "Informe Q1 Cronuts" encuentra más rápido que "el informe de este trimestre"
- **Para acciones irreversibles, pide preview**: "Antes de enviarlo, muéstrame cómo quedaría"
- **Contexto en el Project**: si trabajas siempre con los mismos Notion/Drive, crea un Claude Project y menciona las carpetas/páginas clave en las instrucciones del proyecto

---

## Qué MCP necesita cada equipo

| MCP | Growth | Producto | Content Manager | Filmmaker | Lead Designer | Social Media | Paid Media |
|-----|--------|----------|-----------------|-----------|---------------|--------------|------------|
| Notion | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Google Drive | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Gmail | ✓ | ✓ | — | — | — | — | ✓ |
| Google Calendar | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Make | ✓ | ✓ | — | — | — | — | ✓ |
| Slack | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Figma | — | ✓ | ✓ | — | ✓ | — | — |
| Gamma | ✓ | ✓ | ✓ | — | — | ✓ | ✓ |
| draw.io | — | ✓ | — | — | — | — | — |

---

*¿Tienes un caso de uso que no está aquí? Añádelo con una Pull Request.*
