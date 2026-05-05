# Prompt: Actualización de stakeholders

## Metadatos

| Campo | Valor |
|-------|-------|
| **Tipo** | prompt |
| **Área** | producto |
| **Herramienta** | Claude |
| **Versión** | 1.0 |

---

## Descripción

Redacta comunicaciones claras y estructuradas para stakeholders: actualizaciones de estado, cambios de roadmap, decisiones de producto o resúmenes de sprint. Adapta el tono y nivel de detalle al receptor.

---

## Cuándo usar

- Necesitas comunicar un cambio de roadmap o retraso
- Preparas el update semanal/quincenal de producto
- Quieres presentar una decisión con su razonamiento a dirección o cliente

---

## Instrucciones de uso

1. Rellena `[SITUACION]` con los hechos: qué pasó, qué se decidió, qué cambió
2. Indica en `[RECEPTOR]` a quién va dirigido (CEO, equipo técnico, cliente, inversor...)
3. Especifica `[TONO]` si necesitas uno concreto (ejecutivo/directo, consultivo, tranquilizador...)
4. Añade en `[CONTEXTO_PREVIO]` qué saben ya los receptores para no repetir lo obvio

---

## PROMPT

```
Eres un Product Manager con excelentes habilidades de comunicación ejecutiva.

Situación a comunicar:
[SITUACION]

Receptor(es): [RECEPTOR]
Tono deseado: [TONO]
Contexto previo que ya conocen: [CONTEXTO_PREVIO]

Redacta la comunicación siguiendo estas reglas:
- Empieza con el mensaje más importante (no con contexto)
- Sé directo sobre malas noticias si las hay — no enterrarlas al final
- Incluye siempre: qué pasó/se decidió → por qué → qué impacto tiene → qué se hace ahora
- Termina con una acción clara o próximo paso concreto
- Adapta el nivel técnico al receptor
- Longitud: lo necesario, no más

Genera dos versiones si aplica:
1. Versión larga: para email o doc
2. Versión corta: para Slack/mensaje directo (máx 3-4 líneas)
```

---

## Ejemplo de uso

**Input:**
> Situación: La feature de pagos se retrasa 2 semanas porque encontramos un problema de seguridad en la integración con Stripe que hay que resolver antes del lanzamiento.
> Receptor: CEO y equipo comercial
> Tono: directo, sin alarmar
> Contexto previo: saben que lanzábamos pagos el día 15

**Output esperado:**
> "El lanzamiento de pagos se mueve al día 29. Durante las pruebas de seguridad detectamos una vulnerabilidad en la integración con Stripe que requiere corrección antes de ir a producción. Lanzar con ese riesgo no es una opción. El equipo ya está trabajando en la solución — tenemos alta confianza en el nuevo plazo. Las demos comerciales planificadas pueden continuar con el entorno de pruebas que ya funciona. Os mantendremos informados si hay cualquier cambio."

---

## Notas y limitaciones

- Revisa siempre antes de enviar: el modelo puede suavizar demasiado malas noticias o viceversa
- Para comunicaciones muy sensibles (despidos, conflictos), pide solo la estructura y redacta tú el contenido delicado
