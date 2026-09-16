# Prompt para Generación de Imagen: Protagonista Leche de Vaca (Estilo Superheroína)

Este documento contiene las especificaciones técnicas y los prompts optimizados para generar la imagen canónica de la protagonista antropomórfica del episodio: **Leche de Vaca** en estilo **Superheroína** (personaje antropomórfico femenino personificado a partir del envase de cartón de leche de vaca).

---

## 1. Especificaciones de diseño del personaje

- **Personaje:** Envase de cartón de leche de vaca (*gable-top carton*) personificado de forma antropomórfica femenina.
- **Arquetipo y Estilo:** Superheroína / Heroína de cómic / Protectora matutina.
- **Encuadre:** Cuerpo completo (*full-body shot*), de pie, de frente a la cámara (*front-facing*).
- **Atributos y Vestuario de Superheroína:**
  - El cuerpo está estructurado a partir del envase clásico de cartón de leche (brik blanco y azul con tapón de rosca azul en la parte superior).
  - Viste una capa roja brillante de superheroína que ondea majestuosamente hacia atrás sobre sus hombros.
  - Antifaz azul de superheroína estilizado alrededor de los ojos que realza una mirada femenina viva, pestañas delicadas y una sonrisa confiada y triunfante.
  - Brazos y manos estilizados con elegantes guantes blancos de superheroína, posando con los puños en la cintura en pose clásica de cómic o un puño alzado al cielo.
  - Pequeñas piernas con botas rojas de vuelo que descansan firmemente sobre el suelo.
- **Fondo:** Fondo neutro y continuo de estudio fotográfico profesional (gris oscuro / ciclorama suave con sutil viñeteado).
- **Iluminación:** Iluminación cinematográfica de estudio de alto contraste (*hard key light* frontal/lateral que modela el envase y la capa, *rim light* dorado y azul eléctrico en los contornos, luz cenital difusa).
- **Composición y Formato:** Relación de aspecto horizontal **16:9** (frame de video).
- **Regla estricta:** **Sin texto**, sin letras, sin marcas comerciales impresas en el envase, sin palabras ni marcas de agua.

---

## 2. Prompt principal en inglés (Optimizado para FLUX.1, Midjourney v6, Grok Imagine y DALL-E 3)

```text
Full-body photorealistic shot of an anthropomorphic milk carton container personified as an alluring and courageous female superhero. The classic white and blue gable-top cardboard milk carton has a blue screw cap on top and an expressive, charismatic female face with delicate eyelashes, a sleek blue superhero eye mask, and a confident heroic smile. She is wearing a vibrant flowing red superhero cape billowing behind her back, stylish white-gloved hands with fists resting on her hips in a classic comic book power pose, and small standing feet wearing red superhero boots. Front-facing, centered composition, looking directly into the camera. Shot in a high-end photography studio against a seamless neutral dark gray studio background. Dramatic cinematic lighting with sharp key light sculpting the carton and cape, golden and electric blue rim lights highlighting her silhouette, crisp 8k resolution, photorealistic textures, clean frame, absolutely no text, no letters, no brand names, no typography on the carton, 16:9 aspect ratio.
```

---

## 3. Prompt en español

```text
Toma fotorealista de cuerpo completo de un envase de cartón de leche antropomórfico personificado como una valiente y atractiva superheroína femenina. El clásico cartón de leche blanco y azul tiene una tapa de rosca azul en la parte superior y un rostro femenino carismático y expresivo con pestañas delicadas, un elegante antifaz azul de superheroína y una sonrisa heroica y segura. Lleva una vibrante capa roja de superheroína ondeando a su espalda, elegantes manos con guantes blancos posadas con los puños en la cintura en una clásica pose de poder de cómic, y pequeños pies de pie con botas rojas de superheroína. Encuadre de frente, composición centrada, mirando directamente a la cámara. Fotografía en estudio profesional contra un fondo neutro gris oscuro continuo. Iluminación cinematográfica dramática con luz clave definida que esculpe el envase y la capa, luces de borde doradas y azul eléctrico resaltando su silueta, textura fotográfica 8k hiperrealista, encuadre limpio, sin texto, sin letras, sin logotipos en el cartón, relación de aspecto 16:9.
```

---

## 4. Parámetros recomendados por plataforma

### Midjourney v6 / v6.1
```text
/imagine prompt: Full-body photorealistic portrait of an anthropomorphic female milk carton superhero character, front view, hands on hips comic power pose, red cape billowing, blue superhero eye mask, white gloves, red boots, blue screw cap, confident smile, neutral dark gray studio cyclorama, cinematic studio lighting, rim light, 8k, Hasselblad 50MP --ar 16:9 --style raw --v 6.1 --no text, font, letters, typography, watermark, logo, brand
```

### FLUX.1 [dev] / [schnell] / Stable Diffusion (ComfyUI / WebUI)
- **Positive Prompt:** *(Usar el texto del Prompt principal en inglés)*
- **Negative Prompt:**
  ```text
  text, watermark, typography, letters, words, logo, banner, blurry, cartoon, 3d render, anime, illustration, low resolution, bad anatomy, deformed hands, extra fingers, missing fingers, cropped legs, out of frame, noisy background, cluttered background
  ```
- **Aspect Ratio:** 16:9 (1344 x 768 px o 1536 x 864 px para generación nativa, escalado posterior a 4K).
- **Sampling Steps:** 28 - 35 steps.
- **CFG Scale:** 3.5 - 5.0 (para FLUX) / 7.0 (para SDXL).
