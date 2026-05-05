# Cómo instalar skills y agents en Claude Code

Guía paso a paso para que cualquier miembro del equipo instale los recursos de IA compartidos.

---

## Requisitos previos

- Claude Code instalado ([descargar aquí](https://claude.ai/code))
- Cuenta de Anthropic activa

---

## Instalar un Agent

Los agents son asistentes especializados que se activan automáticamente para tareas concretas (frontend, SEO, WordPress, seguridad...).

### Pasos

1. Descarga el archivo `.md` del agent que quieras desde la carpeta [`/agents`](../agents/) de este repositorio
2. Colócalo en tu directorio de agents de Claude Code:
   - **Windows:** `C:\Users\[TuUsuario]\.claude\agents\`
   - **Mac/Linux:** `~/.claude/agents/`
3. Reinicia Claude Code (o abre una nueva sesión)
4. El agent ya está disponible — Claude lo usará automáticamente cuando la tarea encaje

### Agents disponibles

| Agent | Carpeta | Para qué |
|-------|---------|----------|
| `frontend-developer.md` | `agents/desarrollo/` | Apps frontend completas (React, Vue, Angular) |
| `wordpress-master.md` | `agents/desarrollo/` | WordPress: rendimiento, WooCommerce, headless |
| `seo-analyzer.md` | `agents/marketing/` | Auditorías SEO técnicas y optimización |
| `security-auditor.md` | `agents/seguridad/` | Auditorías de seguridad y compliance |

### Instalar todos los agents de golpe

**Windows (PowerShell):**
```powershell
# Desde la carpeta donde descargaste los archivos
Copy-Item *.md "$env:USERPROFILE\.claude\agents\"
```

**Mac/Linux:**
```bash
cp *.md ~/.claude/agents/
```

---

## Instalar una Skill

Las skills son módulos de capacidades que se instalan globalmente en Claude Code.

### Opción A — Desde el marketplace (recomendado)

En Claude Code, escribe en el chat:
```
/find-skills
```
Describe lo que necesitas y la skill correcta aparecerá con opción de instalar.

O instala directamente si sabes el nombre:
```
/install-skill ui-ux-pro-max
```

### Opción B — Instalación manual

Si tienes el directorio de la skill:
1. Copia la carpeta completa de la skill en:
   - **Windows:** `C:\Users\[TuUsuario]\.claude\skills\`
   - **Mac/Linux:** `~/.claude/skills/`
2. La carpeta debe contener un archivo `SKILL.md`
3. Reinicia Claude Code

### Skills disponibles en el equipo

Ver índice completo: [indice-skills.md](../skills/indice-skills.md)

Skills más útiles para empezar:

| Skill | Cómo activar | Para qué |
|-------|-------------|----------|
| `ui-ux-pro-max` | `/ui-ux-pro-max` o descripción | Diseño UI/UX avanzado |
| `apify-ultimate-scraper` | `/apify-ultimate-scraper` | Scraping web sin código |
| `schema-markup` | `/schema-markup` | SEO estructurado |
| `caveman` | `/caveman` | Respuestas densas, menos tokens |
| `find-skills` | `/find-skills` | Descubrir más skills |

---

## Verificar qué tienes instalado

En Claude Code, abre una conversación y pregunta:
```
¿Qué skills y agents tengo instalados?
```

O ve a **Settings → Skills** en la interfaz de Claude Code.

---

## Solución de problemas

**La skill no aparece tras instalarla**
→ Reinicia Claude Code. Si persiste, verifica que la carpeta tiene `SKILL.md` en la raíz.

**El agent no se activa**
→ Comprueba que el `.md` está en `~/.claude/agents/` (no en subdirectorios). El archivo debe tener el frontmatter `name:` correcto.

**Error de permisos en Windows**
→ Ejecuta PowerShell como administrador para mover los archivos.

---

## ¿Tienes una skill o agent nuevo?

Compártelo en este repositorio:
1. Pon el archivo en la carpeta correcta (`skills/` o `agents/`)
2. Añádelo al índice correspondiente
3. Abre una Pull Request con descripción de para qué sirve

El equipo lo revisa y, si es útil, se añade al índice oficial.