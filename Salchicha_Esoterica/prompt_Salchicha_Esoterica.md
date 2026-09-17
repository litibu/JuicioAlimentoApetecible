# Prompt para Generación de Imagen: Protagonista Salchicha (Estilo Esotérica)

Este documento contiene las especificaciones técnicas y los prompts optimizados para generar la imagen canónica de la protagonista antropomórfica del episodio: **Salchicha** en estilo **Esotérica** (personaje antropomórfico femenino personificado a partir del empaque al vacío de salchichas rosadas, con aureola y alas de ángel o santa).

---

## 1. Especificaciones de diseño del personaje

- **Personaje:** Empaque al vacío de salchichas rosadas personificado de forma antropomórfica femenina.
- **Arquetipo y Estilo:** Esotérica / Ángel o santa / Intercesora beatífica del lonche cotidiano.
- **Encuadre:** Cuerpo completo (*full-body shot*), de pie, de frente a la cámara (*front-facing*).
- **Atributos y Vestuario sacro:**
  - El cuerpo está estructurado a partir de un empaque al vacío transparente de salchichas tipo Viena, con las piezas rosadas visibles a través del plástico brillante.
  - Rostro femenino expresivo integrado en el cabezal del empaque: mirada compasiva, pestañas delicadas y sonrisa serena de santa.
  - Aureola dorada circular flotando sobre la cabeza.
  - Grandes alas de plumas blancas con matices dorados, desplegadas a la espalda.
  - Manos antropomórficas juntas en actitud de oración o ligeramente abiertas en bendición.
  - Escapulario o velo de luz dorada muy sutil sobre los hombros del empaque.
  - Pequeños pies de pie sobre el suelo del estudio, estilizados a partir del cierre inferior del empaque.
- **Fondo:** Fondo neutro y continuo de estudio fotográfico profesional (gris cálido / ciclorama suave con viñeteado sutil).
- **Iluminación:** Iluminación cinematográfica de estudio con haz cenital dorado divino (*top light* cálido), *key light* frontal suave que modela el plástico y las salchichas, *rim light* dorado en alas y aureola.
- **Composición y Formato:** Relación de aspecto horizontal **16:9** (frame de video).
- **Regla estricta:** **Sin texto**, sin letras, sin marcas comerciales impresas en el empaque, sin palabras ni marcas de agua.

---

## 2. Prompt principal en inglés (Optimizado para FLUX.1, Midjourney v6, Grok Imagine y DALL-E 3)

```text
Full-body photorealistic cinematic studio portrait of an anthropomorphic vacuum-sealed pack of pink Vienna sausages personified as a serene female angel-saint. The standing clear plastic sausage package has visible plump pink sausages inside glossy vacuum wrap, an expressive compassionate feminine face with delicate eyelashes and a gentle blessing smile, a glowing golden circular halo floating above her head, and large white-gold feathered wings spread behind her. She stands front-facing and centered, palms joined in prayer, small feet planted on the studio floor. Shot in a high-end photography studio against a seamless warm-gray cyclorama. Dramatic cinematic lighting with a divine golden overhead shaft of light, soft key light sculpting the plastic wrap and sausages, golden rim light on the wings and halo, crisp 8k photorealistic textures, clean frame, absolutely no text, no letters, no brand names, no typography on the package, 16:9 aspect ratio.
```

---

## 3. Prompt en español

```text
Toma fotorealista de cuerpo completo de un empaque al vacío de salchichas rosadas antropomórfico, personificado como un ángel o santa femenina serena. El paquete de plástico transparente de pie muestra salchichas tipo Viena rosadas y plump bajo el plástico brillante, un rostro femenino compasivo y expresivo con pestañas delicadas y una sonrisa de bendición, una aureola dorada circular flotando sobre la cabeza y grandes alas de plumas blancas y doradas desplegadas a la espalda. De frente a cámara, composición centrada, palmas juntas en oración, pequeños pies apoyados en el suelo del estudio. Fotografía en estudio profesional contra un ciclorama gris cálido continuo. Iluminación cinematográfica dramática con un haz cenital dorado divino, luz clave suave que esculpe el plástico y las salchichas, luces de borde doradas en alas y aureola, textura fotográfica 8k hiperrealista, encuadre limpio, sin texto, sin letras, sin logotipos en el empaque, relación de aspecto 16:9.
```

---

## 4. Parámetros recomendados por plataforma

### Midjourney v6 / v6.1
```text
/imagine prompt: Full-body photorealistic portrait of an anthropomorphic female vacuum-packed pink sausage package as a serene angel-saint, front view, prayer pose with joined palms, glowing golden halo, large white-gold feathered wings, clear plastic wrap with visible pink Vienna sausages, compassionate smile, warm gray studio cyclorama, divine golden overhead light, cinematic rim light, 8k, Hasselblad 50MP --ar 16:9 --style raw --v 6.1 --no text, font, letters, typography, watermark, logo, brand
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
- Verificar que el resultado sea cuerpo completo, de frente, con aureola y alas, **sin texto** en el empaque.
