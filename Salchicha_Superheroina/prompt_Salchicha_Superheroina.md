# Prompt para Generación de Imagen: Protagonista Salchicha (Estilo Superheroína)

Este documento contiene las especificaciones técnicas y los prompts optimizados para generar la imagen canónica de la protagonista antropomórfica del episodio: **Salchicha** en estilo **Superheroína** (personaje antropomórfico femenino personificado a partir del empaque al vacío de salchichas rosadas, con capa, antifaz y guantes).

---

## 1. Especificaciones de diseño del personaje

- **Personaje:** Empaque al vacío de salchichas rosadas personificado de forma antropomórfica femenina.
- **Arquetipo y Estilo:** Superheroína / Heroína de cómic / Protectora del lonche.
- **Encuadre:** Cuerpo completo (*full-body shot*), de pie, de frente a la cámara (*front-facing*).
- **Atributos y Vestuario de Superheroína:**
  - El cuerpo está estructurado a partir de un empaque al vacío transparente de salchichas tipo Viena, con las piezas rosadas visibles a través del plástico brillante.
  - Rostro femenino expresivo integrado en el cabezal del empaque: mirada viva, pestañas delicadas y sonrisa confiada y triunfante.
  - Antifaz azul de superheroína estilizado alrededor de los ojos.
  - Capa roja brillante de superheroína que ondea majestuosamente hacia atrás sobre los hombros.
  - Brazos y manos estilizados con elegantes guantes blancos, posando con los puños en la cintura en pose clásica de cómic.
  - Pequeñas piernas con botas rojas de vuelo que descansan firmemente sobre el suelo.
- **Fondo:** Fondo neutro y continuo de estudio fotográfico profesional (gris oscuro / ciclorama suave con sutil viñeteado).
- **Iluminación:** Iluminación cinematográfica de estudio de alto contraste (*hard key light* frontal/lateral que modela el empaque y la capa, *rim light* dorado y azul eléctrico en los contornos, luz cenital difusa).
- **Composición y Formato:** Relación de aspecto horizontal **16:9** (frame de video).
- **Regla estricta:** **Sin texto**, sin letras, sin marcas comerciales impresas en el empaque, sin palabras ni marcas de agua.

---

## 2. Prompt principal en inglés (Optimizado para FLUX.1, Midjourney v6, Grok Imagine y DALL-E 3)

```text
Full-body photorealistic cinematic studio portrait of an anthropomorphic vacuum-sealed pack of pink Vienna sausages personified as a courageous female superhero. The standing clear plastic sausage package has visible plump pink sausages inside glossy vacuum wrap, an expressive charismatic feminine face with delicate eyelashes, a sleek blue superhero eye mask, and a confident heroic smile. She is wearing a vibrant flowing red superhero cape billowing behind her back, stylish white-gloved hands with fists resting on her hips in a classic comic book power pose, and small standing feet wearing red superhero boots. Front-facing, centered composition, looking directly into the camera. Shot in a high-end photography studio against a seamless neutral dark gray studio background. Dramatic cinematic lighting with sharp key light sculpting the plastic wrap, sausages and cape, golden and electric blue rim lights highlighting her silhouette, crisp 8k photorealistic textures, clean frame, absolutely no text, no letters, no brand names, no typography on the package, 16:9 aspect ratio.
```

---

## 3. Prompt en español

```text
Toma fotorealista de cuerpo completo de un empaque al vacío de salchichas rosadas antropomórfico, personificado como una valiente superheroína femenina. El paquete de plástico transparente de pie muestra salchichas tipo Viena rosadas bajo el plástico brillante, un rostro femenino carismático y expresivo con pestañas delicadas, un elegante antifaz azul de superheroína y una sonrisa heroica y segura. Lleva una vibrante capa roja de superheroína ondeando a su espalda, elegantes manos con guantes blancos posadas con los puños en la cintura en una clásica pose de poder de cómic, y pequeños pies de pie con botas rojas de superheroína. Encuadre de frente, composición centrada, mirando directamente a la cámara. Fotografía en estudio profesional contra un fondo neutro gris oscuro continuo. Iluminación cinematográfica dramática con luz clave definida que esculpe el plástico, las salchichas y la capa, luces de borde doradas y azul eléctrico resaltando su silueta, textura fotográfica 8k hiperrealista, encuadre limpio, sin texto, sin letras, sin logotipos en el empaque, relación de aspecto 16:9.
```

---

## 4. Parámetros recomendados por plataforma

### Midjourney v6 / v6.1
```text
/imagine prompt: Full-body photorealistic portrait of an anthropomorphic female vacuum-packed pink sausage package as a superhero, front view, hands on hips comic power pose, red cape billowing, blue superhero eye mask, white gloves, red boots, clear plastic wrap with visible pink Vienna sausages, confident smile, neutral dark gray studio cyclorama, cinematic studio lighting, rim light, 8k, Hasselblad 50MP --ar 16:9 --style raw --v 6.1 --no text, font, letters, typography, watermark, logo, brand
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

### Grok Imagine
- Usar el **prompt principal en inglés** (apartado 2).
- Relación de aspecto: **16:9**.
- Verificar que el resultado sea cuerpo completo, de frente, con capa, antifaz y guantes, **sin texto** en el empaque.
