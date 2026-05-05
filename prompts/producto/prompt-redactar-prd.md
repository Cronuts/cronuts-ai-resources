# Prompt: Redactar PRD desde brief

## Metadatos

| Campo | Valor |
|-------|-------|
| **Tipo** | prompt |
| **Área** | producto |
| **Herramienta** | Claude |
| **Versión** | 1.0 |

---

## Descripción

Genera un PRD completo y estructurado a partir de un brief inicial. Útil cuando tienes una idea clara pero necesitas convertirla en documento formal para alinear equipo técnico y stakeholders.

---

## Cuándo usar

- Tienes una feature o producto nuevo que documentar formalmente
- Necesitas alinear a desarrollo, diseño y negocio en un solo doc
- Quieres un primer borrador rápido para refinar con el equipo

---

## Instrucciones de uso

1. Copia el bloque PROMPT
2. Sustituye `[BRIEF]` con tu descripción de la feature (puede ser informal)
3. Sustituye `[CONTEXTO_PRODUCTO]` con descripción breve de tu producto y usuarios
4. Ejecuta en Claude

---

## PROMPT

```
Actúa como un Product Manager senior con experiencia en productos digitales.

Contexto del producto:
[CONTEXTO_PRODUCTO]

Brief de la feature:
[BRIEF]

Genera un PRD completo con esta estructura:
1. Resumen ejecutivo (2-3 frases)
2. Problema del usuario y del negocio
3. Objetivos con métricas y targets
4. Fuera de alcance (3-5 items explícitos)
5. Usuarios objetivo con perfil detallado
6. Solución propuesta con user journey paso a paso
7. Requisitos funcionales priorizados como Must/Should/Could
8. Requisitos no funcionales relevantes
9. Riesgos con probabilidad, impacto y mitigación
10. Criterios de aceptación testeables
11. Métricas de éxito post-lanzamiento

Sé específico y concreto. Donde no tengas datos exactos, indica qué habría que investigar. Usa lenguaje claro, sin jerga técnica innecesaria. El doc debe ser legible por negocio y técnica.
```

---

## Ejemplo de uso

**Input:**
> Contexto: App de reservas de restaurantes, 50k usuarios activos, mobile-first.
> Brief: Queremos añadir que el usuario pueda ver el menú del restaurante antes de reservar.

**Output esperado:**
> PRD completo con problema (usuarios preguntan por el menú antes de confirmar → tasa de cancelación 23%), objetivos (reducir cancelaciones en 15%), requisitos (visualización de menú con fotos, filtros alérgenos, PDF descargable como Could), riesgos (dependencia de restaurantes para mantener menús actualizados)...

---

## Notas y limitaciones

- El PRD generado es un borrador: siempre revisar datos, métricas y contexto real
- Añade los wireframes y referencias visuales manualmente
- Los criterios de aceptación necesitan validación con QA
