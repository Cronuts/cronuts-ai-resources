# Prompt: Análisis de competencia

## Metadatos

| Campo | Valor |
|-------|-------|
| **Tipo** | prompt |
| **Área** | producto |
| **Herramienta** | Claude |
| **Versión** | 1.0 |

---

## Descripción

Estructura un análisis competitivo a partir de información sobre competidores. Identifica gaps, ventajas diferenciales y oportunidades de producto.

---

## Cuándo usar

- Antes de definir una nueva feature o producto
- Para preparar una sesión de estrategia de producto
- Cuando necesitas justificar una decisión ante stakeholders con benchmarks

---

## Instrucciones de uso

1. Copia el PROMPT
2. Pega en `[INFO_COMPETIDORES]` todo lo que sepas: screenshots, descripciones, precios, reviews de usuarios, capturas de App Store...
3. Ajusta `[NUESTRO_PRODUCTO]` con tu contexto
4. Indica en `[FOCO]` qué área quieres analizar (UX, pricing, features, posicionamiento...)

---

## PROMPT

```
Eres un analista de producto con experiencia en benchmarking competitivo.

Nuestro producto: [NUESTRO_PRODUCTO]

Información sobre competidores:
[INFO_COMPETIDORES]

Área de análisis: [FOCO]

Analiza esta información y genera:

## 1. Tabla comparativa
Compara los competidores y nuestro producto en las dimensiones más relevantes para [FOCO].

## 2. Fortalezas de cada competidor
Para cada uno: qué hacen bien y por qué importa al usuario.

## 3. Debilidades y gaps
Qué no resuelven bien. Qué quejas tienen los usuarios (si hay reviews).

## 4. Nuestra posición actual
Dónde estamos respecto a la competencia. Honesto, sin sesgo favorable.

## 5. Oportunidades de diferenciación
3-5 oportunidades concretas donde podríamos tener ventaja real. Prioriza por impacto estimado y esfuerzo.

## 6. Amenazas a vigilar
Movimientos competitivos que deberíamos monitorizar.

## 7. Recomendaciones de producto
Acciones concretas de corto plazo (0-3 meses) y medio plazo (3-12 meses) basadas en el análisis.

Sé directo y específico. Evita generalidades. Si hay información insuficiente para algún punto, indícalo.
```

---

## Ejemplo de uso

**Input:**
> Nuestro producto: herramienta de gestión de proyectos para agencias creativas
> Info competidores: [pegado de páginas de precios de Notion, Monday, Asana + capturas de reviews en G2]
> Foco: pricing y propuesta de valor

**Output esperado:**
> Tabla comparativa de planes, análisis de quejas comunes (Monday demasiado complejo, Notion sin estructura suficiente para proyectos), oportunidad: pricing por proyecto en lugar de por seat para agencias pequeñas...

---

## Notas y limitaciones

- Claude no accede a internet: proporciona tú la información del competidor
- Más información = análisis más preciso. Pega reviews reales si puedes
- Valida las oportunidades con usuarios antes de priorizarlas
