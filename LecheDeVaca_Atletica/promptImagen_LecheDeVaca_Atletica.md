# Prompt para Generación de Imagen: Protagonista Leche de Vaca (Estilo Atlética)

Este documento contiene las especificaciones técnicas y los prompts optimizados para generar la imagen canónica de la protagonista antropomórfica del episodio: **Leche de Vaca** en estilo **Atlética** (antropomórfica femenina, musculosa, tonificada y seductora, basada en el envase de cartón de leche).

---

## 1. Especificaciones de diseño del personaje

- **Personaje:** Envase de cartón de leche de vaca (*gable-top carton*) personificado de forma antropomórfica femenina.
- **Arquetipo y Estilo:** Atlética / Fisicoculturista fitness / Femenina musculosa y seductora.
- **Encuadre:** Cuerpo completo (*full-body shot*), de pie, de frente a la cámara (*front-facing*).
- **Atributos y Vestuario deportivo:**
  - El cuerpo está estructurado a partir del envase clásico de cartón de leche (brik blanco y azul con tapón de rosca azul en la parte superior).
  - Brazos y hombros musculosos, definidos y tonificados, con manos enguantadas de blanco flexionando los bíceps con orgullo y seguridad en sí misma.
  - Porta muñequeras deportivas blancas elásticas y un reloj inteligente deportivo en la muñeca izquierda.
  - Luce un top deportivo ajustado y zapatillas / tenis deportivos modernos de suela gruesa en las piernas.
  - Rostro femenino expresivo integrado en el cartón, con mirada coqueta, pestañas definidas y una sonrisa confiada, triunfadora y seductora.
- **Fondo:** Fondo neutro y continuo de estudio fotográfico profesional (gris oscuro / ciclorama suave con viñeta sutil).
- **Iluminación:** Iluminación cinematográfica de estudio deportivo de alto contraste (*hard key light* lateral que define la musculatura y el volumen del envase, *rim light* azul eléctrico y dorado en los contornos, luz cenital tenue).
- **Composición y Formato:** Relación de aspecto horizontal **16:9** (frame de video).
- **Regla estricta:** **Sin texto**, sin letras, sin marcas comerciales impresas en el envase, sin palabras ni marcas de agua.

---

## 2. Prompt principal en inglés (Optimizado para FLUX.1, Midjourney v6, Grok Imagine y DALL-E 3)

```text
Full-body photorealistic shot of an anthropomorphic milk carton container personified as an athletic, muscular, and alluring female fitness champion. The classic white and blue gable-top cardboard milk carton has a blue screw cap on top and an expressive, confident, and seductive female face with delicate eyelashes and a triumphant smile. She has well-defined, muscular, and toned arms with white-gloved hands flexing her biceps in a powerful bodybuilder pose. She is wearing white athletic wristbands, a sleek modern smartwatch on her wrist, a stylish athletic sports top, and modern chunky running sneakers on her small standing feet. Front-facing, centered composition, looking directly into the camera. Shot in a high-end photography studio against a seamless neutral gray background. Dramatic cinematic sports studio lighting with sharp key light sculpting muscle definition and carton edges, electric blue and warm rim lights highlighting her silhouette, 8k resolution, photorealistic textures, clean frame, absolutely no text, no letters, no brand names, no typography on the carton, 16:9 aspect ratio.
```

---

## 3. Prompt en español

```text
Toma fotorealista de cuerpo completo de un envase de cartón de leche antropomórfico personificado como una campeona fitness femenina atlética, musculosa y seductora. El clásico cartón de leche blanco y azul tiene una tapa de rosca azul en la parte superior y un rostro femenino expresivo, seguro y seductor con pestañas delicadas y una sonrisa triunfante. Posee brazos bien definidos, musculosos y tonificados con manos enguantadas de blanco flexionando los bíceps en una poderosa pose de fisicoculturista. Lleva muñequeras deportivas blancas, un elegante reloj inteligente moderno en la muñeca, un top deportivo ceñido y tenis deportivos modernos en sus pies. Encuadre de frente, composición centrada, mirando directamente a la cámara. Fotografía en estudio profesional contra un fondo neutro gris continuo. Iluminación cinematográfica deportiva dramática con luz clave definida que esculpe los músculos y bordes del envase, luces de borde azul eléctrico y doradas resaltando su silueta, textura fotográfica 8k hiperrealista, encuadre limpio, sin texto, sin letras, sin logotipos en el cartón, relación de aspecto 16:9.
```

---

## 4. Parámetros recomendados por plataforma

### Midjourney v6 / v6.1
```text
/imagine prompt: Full-body photorealistic portrait of an anthropomorphic milk carton female character as an athletic muscular fitness bodybuilder, front view, flexing biceps, blue screw cap, sports top, smartwatch, athletic sneakers, seductive confident smile, neutral dark gray studio cyclorama, dramatic sports studio lighting, blue and gold rim light, 8k, Hasselblad 50MP --ar 16:9 --style raw --v 6.1 --no text, font, letters, typography, watermark, logo, brand
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
