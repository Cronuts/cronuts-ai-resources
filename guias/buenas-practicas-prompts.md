# Guía: Buenas prácticas para escribir prompts de producto

Principios para sacar el máximo partido a los prompts del repositorio y crear los tuyos propios.

---

## El principio fundamental

**El modelo responde a lo que le das.** Un prompt vago produce output vago. Un prompt con contexto, objetivo y formato claro produce trabajo útil.

Regla de oro: escribe el prompt como si se lo estuvieras explicando a un consultor muy capaz que lleva 5 minutos en la empresa y no sabe nada de vuestro producto.

---

## Los 4 elementos de un buen prompt de producto

### 1. Rol
Dile quién debe ser. El rol activa un conjunto de conocimiento y estilo de respuesta.

**Mal:** "Analiza este PRD"
**Bien:** "Actúa como un Product Manager senior con experiencia en SaaS B2B. Analiza este PRD..."

### 2. Contexto
Qué es tu producto, quiénes son tus usuarios, cuál es la situación. Más contexto = mejor output.

**Mal:** "Escribe user stories para el checkout"
**Bien:** "Escribe user stories para el checkout. Contexto: ecommerce de moda, 80% de ventas en mobile, usuarios de 25-40 años, tasa de abandono en checkout del 68%"

### 3. Tarea con formato definido
Qué quieres exactamente y cómo quieres que lo estructure.

**Mal:** "Dame ideas para mejorar la retención"
**Bien:** "Dame 5 ideas para mejorar la retención D30. Para cada una: descripción en 2 frases, esfuerzo estimado (alto/medio/bajo) y métrica que impactaría"

### 4. Restricciones
Qué no debe hacer, qué límites tiene, qué debe evitar.

**Ejemplo:** "No incluyas soluciones que requieran cambios en la base de datos. El roadmap de infra está congelado este trimestre."

---

## Técnicas avanzadas

### Chain of thought
Para análisis complejos, pide que razone antes de concluir:
> "Antes de darme la recomendación, analiza en voz alta los trade-offs de cada opción."

### Few-shot: dar ejemplos
Si necesitas un formato muy específico, muestra un ejemplo de lo que quieres:
> "Quiero el output en este formato: [ejemplo]. Genera 5 más igual."

### Iterar, no empezar de cero
El output del modelo es un borrador. Refínalo en la misma conversación:
> "Buen punto el de los costes de soporte. Expande esa sección y añade benchmarks del sector."

### Separar en pasos
Para tareas largas, divide en prompts encadenados:
1. Primero pide el análisis
2. Luego pide la síntesis de ese análisis
3. Luego pide las recomendaciones basadas en esa síntesis

---

## Errores comunes

| Error | Por qué falla | Corrección |
|-------|--------------|------------|
| Prompt de una línea para tarea compleja | Falta contexto → output genérico | Añade rol + contexto + formato |
| Pedir "lo mejor" sin definir criterios | "Mejor" es ambiguo | Define qué métrica optimiza |
| No especificar el receptor del output | Tono y detalle erróneos | "Este doc lo leerá el CEO, no técnicos" |
| Aceptar el primer output sin iterar | Los modelos mejoran con feedback | Refina en la misma conversación |
| Dar demasiadas tareas a la vez | Calidad cae en todas | Un objetivo principal por prompt |

---

## Cómo contribuir un prompt al repositorio

Si creas un prompt que te ha funcionado bien:
1. Usa la [plantilla estándar](../plantillas/plantilla-recurso.md)
2. Incluye un ejemplo de uso real (puedes anonimizar)
3. Nómbralo como `prompt-[qué-hace].md`
4. Ponlo en `prompts/[tu-área]/`
5. Abre una Pull Request

La calidad del repositorio depende de que compartamos lo que realmente funciona.
