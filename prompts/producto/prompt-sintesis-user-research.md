# Prompt: Síntesis de investigación con usuarios

## Metadatos

| Campo | Valor |
|-------|-------|
| **Tipo** | prompt |
| **Área** | producto |
| **Herramienta** | Claude |
| **Versión** | 1.0 |

---

## Descripción

Analiza notas, transcripciones o resúmenes de entrevistas con usuarios y extrae insights accionables, patrones de comportamiento y oportunidades de producto. Convierte horas de research en un informe estructurado.

---

## Cuándo usar

- Tras ronda de entrevistas de usuario (discovery o validación)
- Para sintetizar resultados de encuestas con respuestas abiertas
- Cuando tienes notas de usability testing y necesitas priorizar problemas

---

## Instrucciones de uso

1. Copia el PROMPT
2. En `[NOTAS_ENTREVISTAS]` pega las notas o transcripciones (puedes pegar varias separadas por `---`)
3. Indica en `[OBJETIVO_RESEARCH]` qué querías aprender
4. Ajusta `[N_ENTREVISTAS]` con el número de participantes

---

## PROMPT

```
Eres un UX Researcher experto en síntesis de investigación cualitativa.

Objetivo de la investigación: [OBJETIVO_RESEARCH]
Número de entrevistas/participantes: [N_ENTREVISTAS]

Notas de las entrevistas:
[NOTAS_ENTREVISTAS]

Analiza todo el material y genera un informe de síntesis con:

## 1. Resumen ejecutivo
3-5 frases con los hallazgos más importantes. Pensado para un stakeholder que no leerá el resto.

## 2. Patrones identificados
Agrupa los hallazgos en 3-6 patrones principales. Para cada uno:
- Nombre del patrón
- Descripción
- Evidencia (citas o referencias a entrevistas específicas)
- Frecuencia (cuántos participantes lo mencionaron / mostraron)

## 3. Jobs to be Done
Qué trabajos funcionales, emocionales y sociales están intentando completar los usuarios.

## 4. Fricciones y pain points
Lista priorizada por frecuencia e intensidad. Para cada uno: descripción, impacto percibido en el usuario.

## 5. Comportamientos sorprendentes
Lo que no esperabas encontrar. Workarounds, comportamientos no previstos, usos inesperados.

## 6. Oportunidades de producto
3-5 oportunidades concretas derivadas del research, con la evidencia que las sustenta.

## 7. Preguntas abiertas
Qué sigue sin respuesta y requeriría más investigación.

Cita con "[P1]", "[P2]"... para referenciar participantes sin usar nombres reales.
```

---

## Ejemplo de uso

**Input:**
> Objetivo: entender por qué usuarios abandonan el onboarding a mitad
> N: 6 entrevistas
> Notas: [transcripciones pegadas]

**Output esperado:**
> Patrón 1: "No entienden el valor hasta el paso 3" (4/6 participantes), Pain point principal: piden datos de tarjeta antes de ver el producto, Oportunidad: trial sin registro de pago...

---

## Notas y limitaciones

- El modelo no inventa datos: solo sintetiza lo que le das
- Cuantas más notas y detalle, mejor síntesis
- Valida los insights principales con el equipo antes de presentarlos
- Para transcripciones muy largas, divide en varias conversaciones
