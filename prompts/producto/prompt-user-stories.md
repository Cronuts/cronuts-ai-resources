# Prompt: Escribir User Stories

## Metadatos

| Campo | Valor |
|-------|-------|
| **Tipo** | prompt |
| **Área** | producto |
| **Herramienta** | Claude |
| **Versión** | 1.0 |

---

## Descripción

Genera user stories bien estructuradas con criterios de aceptación en formato Gherkin (Given/When/Then) a partir de una descripción de funcionalidad. Listas para llevar al backlog.

---

## Cuándo usar

- Necesitas desglosar una épica en historias concretas
- Quieres criterios de aceptación detallados y testeables
- Preparas un sprint y necesitas historias estimables

---

## Instrucciones de uso

1. Copia el bloque PROMPT
2. Sustituye `[EPICA]` con la épica o funcionalidad a desglosar
3. Sustituye `[USUARIO]` con el tipo de usuario (ej: "usuario registrado", "admin", "visitante")
4. Sustituye `[CONTEXTO]` con detalles relevantes del producto

---

## PROMPT

```
Eres un Product Manager experto en metodologías ágiles.

Funcionalidad a desarrollar:
[EPICA]

Usuario principal: [USUARIO]
Contexto del producto: [CONTEXTO]

Genera user stories siguiendo este formato exacto:

---
**Historia [N]: [Título]**

**Como** [tipo de usuario],
**quiero** [acción o capacidad],
**para** [beneficio o valor que obtiene].

**Criterios de aceptación:**
- **Dado** [contexto/precondición]
  **Cuando** [acción del usuario]
  **Entonces** [resultado esperado]

**Notas técnicas:** [dependencias, restricciones o aclaraciones para desarrollo]
**Estimación sugerida:** [XS/S/M/L/XL]
---

Genera todas las historias necesarias para cubrir la funcionalidad completa.
Incluye:
- Happy path principal
- Casos edge relevantes
- Estados de error visibles al usuario
- Historias de admin/backoffice si aplica

Ordénalas de mayor a menor valor para el usuario.
```

---

## Ejemplo de uso

**Input:**
> Épica: Login con Google
> Usuario: visitante que quiere registrarse
> Contexto: App B2C de gestión de gastos personales

**Output esperado:**
> Historia 1: Login con cuenta de Google (happy path)
> Historia 2: Primer acceso — completar perfil tras login con Google
> Historia 3: Error si cuenta de Google no tiene email verificado
> Historia 4: Reconexión si token de Google expira...

---

## Notas y limitaciones

- Revisa las estimaciones: son orientativas, el equipo debe refinarlo
- Los criterios Gherkin son punto de partida para QA, no sustituto del refinamiento
- Añade manualmente el enlace a diseño / Figma en cada historia
