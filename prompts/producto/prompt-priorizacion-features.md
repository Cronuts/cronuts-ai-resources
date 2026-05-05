# Prompt: Priorización de features (RICE + MoSCoW)

## Metadatos

| Campo | Valor |
|-------|-------|
| **Tipo** | prompt |
| **Área** | producto |
| **Herramienta** | Claude |
| **Versión** | 1.0 |

---

## Descripción

Evalúa y prioriza una lista de features usando frameworks RICE (Reach, Impact, Confidence, Effort) y MoSCoW. Genera un backlog ordenado con justificación para cada decisión.

---

## Cuándo usar

- Tienes una lista larga de features y necesitas ordenarlas
- Debes defender el roadmap ante stakeholders
- Prepares una sesión de priorización con el equipo

---

## Instrucciones de uso

1. Lista tus features en `[LISTA_FEATURES]` (una por línea, con contexto si lo tienes)
2. Describe el contexto en `[CONTEXTO_NEGOCIO]`: objetivo del trimestre, recursos disponibles, restricciones
3. Opcional: indica en `[CRITERIOS_EXTRA]` si hay factores específicos que pesar (deuda técnica, compromisos con clientes, dependencias regulatorias...)

---

## PROMPT

```
Eres un Product Manager experto en priorización estratégica de producto.

Contexto del negocio y objetivos actuales:
[CONTEXTO_NEGOCIO]

Lista de features a priorizar:
[LISTA_FEATURES]

Criterios adicionales a considerar:
[CRITERIOS_EXTRA]

Para cada feature:

1. **Evaluación RICE** (escala 1-10 para cada factor):
   - Reach: cuántos usuarios se benefician por periodo
   - Impact: cuánto mejora la métrica objetivo (0.25=mínimo, 0.5=bajo, 1=medio, 2=alto, 3=masivo)
   - Confidence: qué tan seguros estamos de Reach e Impact (%)
   - Effort: semanas de trabajo de un ingeniero
   - Score RICE = (Reach × Impact × Confidence) / Effort

2. **Clasificación MoSCoW**: Must / Should / Could / Won't (para este ciclo)

3. **Justificación** en 2-3 frases: por qué este score y esta clasificación

Tras evaluar todas, genera:
- Tabla resumen ordenada por RICE score
- Top 3 recomendadas para el próximo sprint/ciclo con argumento
- Advertencias: features con alta urgencia percibida pero bajo RICE (por qué no priorizarlas aún)
- Dependencias entre features si las detectas

Sé honesto si los datos son insuficientes para puntuar con confianza.
```

---

## Ejemplo de uso

**Input:**
> Contexto: Q2, objetivo aumentar retención D30. Equipo de 3 devs.
> Features: [1. Push notifications de recordatorio, 2. Modo oscuro, 3. Exportar a CSV, 4. Onboarding personalizado por segmento]
> Criterios extra: Modo oscuro prometido en redes hace 2 meses

**Output esperado:**
> RICE scores: Onboarding personalizado (18.5) > Push notifications (12) > CSV export (4.2) > Modo oscuro (3.1)
> Recomendación: Onboarding + Push para Q2. Modo oscuro: programar para Q3 y comunicar fecha externamente...

---

## Notas y limitaciones

- RICE es una herramienta, no una verdad absoluta: úsala para estructurar la conversación, no para evitarla
- Los scores que genera el modelo son estimaciones basadas en tu descripción — ajústalos con datos reales si los tienes
- Involucra a tech en la estimación de Effort antes de cerrar el roadmap
