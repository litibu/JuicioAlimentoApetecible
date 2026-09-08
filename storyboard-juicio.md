---
name: storyboard-juicio
description: Genera guionLiterario.md y guionTecnico.md con bocetos PNG por escena   
para videos de Juicio Alimento Apetecible. Solicita título y estilo. Úsalo con   
/storyboard-juicio, "storyboard", "guion literario", "guion técnico", "bocetos",   
"imágenes de escenas".  
argument-hint: "[título] [estilo]"  
when-to-use:   
- "juicio"
- "juicio alimento"
user-invocable: true
disable-model-invocation: false 
metadata: 
 author: "Norberto Velasco"
 short-description: "Guion literario + técnico + PNG por escena"
---

El cuerpo debe ordenar al agente en este orden, sin saltarse pasos.

**Paso A — Pedir inputs (obligatorio, antes de escribir)**

Si el usuario no los dio:
1. Título del guion (nombre del alimento acusado / capítulo). Ejemplo: Leche de Vaca.
2. Estilo del guion (hook visual de la protagonista). Una sola opción:

┌──────────────┬──────────────────────────────────────────┐
│ Estilo       │ Aspecto de la protagonista               │
├──────────────┼──────────────────────────────────────────┤
│ Superheroína │ Antropomorfizado femenino, superhéroina  │
├──────────────┼──────────────────────────────────────────┤
│ Esotérica    │ Antropomorfizado femenino, ángel o santa │
├──────────────┼──────────────────────────────────────────┤
│ Fornido      │ Antropomorfizado masculino musculoso     │
├──────────────┼──────────────────────────────────────────┤
│ Atlética     │ Antropomorfizado femenino, seductora     │
└──────────────┴──────────────────────────────────────────┘

No generar nada hasta tener ambos. Si el usuario pasa /storyboard-juicio Leche de Vaca Superheroína, no preguntar de nuevo.

**Paso B — Investigar el alimento**

Antes de redactar:

• Buscar datos reales (PROFECO / Revista del Consumidor y fuentes técnicas).
• No inventar datos científicos, médicos ni de etiquetado.
• Fijar 3 acusaciones verificables.

**Paso C — Fijar consistencia de personaje**

Leer references/personajes.md y references/estilos-visuales.md.

Reglas fijas del canal:

• Beto y Beti nunca aparecen en cuadro (solo voice over).
• El alimento acusado es el único personaje en escena.
• El estilo elegido define vestuario, pose y paleta de todas las escenas.
• Generar primero un retrato canónico imagenes/ref-protagonista.png con image_gen.
• Cada escena posterior se deriva de esa referencia con image_edit, no con un image_gen nuevo (si no, el personaje cambia de cara).

Prompt base del retrato (adaptar título + estilo):

Envase antropomorfizado de [TÍTULO], estilo [ESTILO], cuerpo completo, frente a cámara, fondo neutro de estudio, iluminación cinematográfica, 16:9, sin texto en la imagen.

**Paso D — Redactar los dos guiones**

Leer references/estructura-guion.md y references/plantillas.md.

Actos (igual que guion-juicio):

1. Hook (consumo cotidiano)
2. Acusaciones
3. Ciencia y tecnología / aditivos
4. Origen (fórmula casera, Beti)
5. Alegatos de la defensa
6. Sentencia y veredicto de compra

Cada escena del literario lleva: slugline (acto, escena, nombre), acción, acotación, diálogos.

Cada escena del técnico lleva: plano/visual, cámara, iluminación/filtros, audio/SFX/música, texto en pantalla/gráficos.

**Paso E — Renderizar un PNG por escena**

Para cada escena, en serie respecto al personaje (el retrato primero; las escenas pueden ir en paralelo después de tener la referencia):

1. Extraer de la escena: locación, acción, plano, luz, texto en pantalla.
2. Llamar image_edit con image: [ruta de ref-protagonista.png].
3. Aspecto 16:9 (frame de video).
4. Guardar como imagenes/escena-NN-<slug-del-nombre>.png.
5. No pedir al modelo de imagen que dibuje párrafos de diálogo; el texto va en el markdown. Si hay rótulo corto (máx. 3–4 palabras), incluirlo; si el texto es largo, dejarlo solo en el guion.

**Paso F — Escribir los archivos y vincular las imágenes**

Crear el directorio output/<slug>/imagenes/ y los dos markdown.

Plantilla de escena en guionLiterario.md:

### ESCENA 1 — HOOK: «SÚPER LECHE DE VACA»

![Escena 1 — Hook: Súper Leche de Vaca](imagenes/escena-01-hook-super-leche.png)

| Campo | Detalle |
| :--- | :--- |
| **Acto** | Acto 1 — Planteamiento |
| **Escena** | 1 |
| **Nombre** | Hook. Día. Interior. |
| **Duración estimada** | 00:00 – 00:28 |

**Acción:** ...
**(PERSONAJE, tono, movimiento)**
Diálogo.

Plantilla de escena en guionTecnico.md:

### ESCENA 1 — HOOK

![Escena 1 — Hook](imagenes/escena-01-hook-super-leche.png)

- **Plano / Visual:** ...
- **Cámara:** ...
- **Iluminación / filtros:** ...
- **Audio / SFX / Música:** ...
- **Texto en pantalla / Gráficos:** ...

Misma ruta relativa en ambos archivos (imagenes/...). Al final, apartado Referencias consultadas con URLs reales.

Paso G — Entregar al usuario

Listar rutas de guionLiterario.md, guionTecnico.md y la carpeta imagenes/. Confirmar título, estilo y número de escenas/PNG.
