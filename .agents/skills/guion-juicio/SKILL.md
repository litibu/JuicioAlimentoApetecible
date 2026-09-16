---
name: guion-juicio
description: Genera guionLiterario.md y guionTecnico.md más archivo markdown con el prompt para creación de imagen del alimento en juicio para realizar video. Úsalo cuando el usuario pida redactar, crear, diseñar o estructurar un guion o episodio sobre un alimento a juicio.
---

Sigue los siguientes pasos para generar los guiones, no saltarse pasos.  

## Paso A: Solicitar inputs (obligatorio, antes de escribir)
1. Título del guion (nombre del alimento acusado).
2. Estilo del guion (hook visual de la protagonista). Solicitar al usuario seleccione unicamente uno de los siguientes estilos:  

| Estilo | Aspecto de la protagonista |
| :--- | :--- |
| Superheroína | Antropomórfica femenina, superheroína |
| Esotérica | Antropomórfica femenina, ángel o santa |
| Atlética | Antropomórfica femenina, musculosa, seductora |

No generar nada hasta tener ambos inputs.

## Paso B: Investigar el alimento
Antes de redactar:
- Buscar datos reales PROFECO, https://revistadelconsumidor.profeco.gob.mx y   
  fuentes científicas en México. 
- No inventar datos científicos, médicos, nutricionales ni técnicos.
- Fijar 3 acusaciones verificables.

## Paso C: Redactar guiones literario y técnico
**En la generación de los guiones literario y técnico se debe considerar:**

### Audiencia
Mujeres trabajadoras o estudiantes de 18 a 50 años que compran los ingredientes para   
prepararse su comida para llevar al trabajo o escuela.

### Beneficio al espectador
- Evitar compra impulsiva del alimento por marketing, mediante una evaluación crítica del alimento.

### Tono de la narración del guion
El objetivo del guion es lograr crear un video de YouTube educativo y divertido que proporcione   
al espectador información científica y técnica valorable permitiendole tomar mejores decisiones de   
consumo del alimento acusado. 

### Resumen del video
Inicia con un hook visual donde se muestra varias formas de consumo cotidiano   
del alimento acusado. Se resalta el  protagonismo del alimento mediante   
una participación exageradamente  dramatizada y musicalizada del alimento.   
Posterior Beto y Beti desarrollan de forma divertida un juicio sobre el alimento acusado.  
El video concluye con un veredicto de compra para el consumidor y alertas de salud   
en el consumo cotidiano del alimento acusado.

### Fijar consistencia de personajes y estilo
1. Leer:
- resources/Personajes-Juicio.md 
- references/Atletica-Juicio.md 
- references/Esoterica-Juicio.md 
- references/Superheroina-Juicio.md 
2. El estilo elegido define vestuario, pose y paleta de todas las escenas.
3. El alimento acusado es el único personaje en escena.
4. Los personajes Beto y Beti nunca aparecen en escena, solo en voice over (no   
   generar imágenes de Beto o Beti).

### Referencia de estructura de los guiones literario y técnico
Leer resources/Estructura-Juicio.md y resources/imagenes/

### Formato de salida del guion  literario
Archivo markdown (con nombre debe ser la union de guion_Literario, Alimento y Estilo, ejemplo: "guion_Literario_Alimento_Estilo.md") con los siguientes apartados:
1. Resumen del guion literario. 
2. Guion literario.

### Formato de salidad del guion técnico
Archivo markdown (con nombre debe ser la union de guion_Tecnico, Alimento y Estilo, ejemplo: "guion_Tecnico_Alimento_Estilo.md") con los siguientes apartados:
1. Ficha técnica de producción del video.
2. Convención del guion técnico.
3. Guion técnico. 

### Prompt para generación de imagen del alimento protagonista
A partir del alimento y estilo definido por el usuario, generar archivo markdown con   
prompt para la realización de imagen fotorealista antropomorfizada femenina   
de cuerpo completo del envase, recipiente o empaque del alimento, frente a cámara, fondo neutro de estudio, iluminación   
cinematográfica, 16:9, sin texto en la imagen.

## Paso D: Crea carpeta con los archivos generados
- El nombre de la carpeta deber ser la union del Alimento y el estilo seleccionado. Ej: "Alimento_Estilo",
- Dentro de la carpeta se debe crear los archivos:
  - "guionLiterario_Alimento_Estilo.md"
  - "guionTecnico_Alimento_Estilo.md"
  - "promptImagen_Alimento_Estilo.md"
  - Imagen creada con el prompt generado, con el nombre: "[ALIMENTO]_[ESTILO].jpg".