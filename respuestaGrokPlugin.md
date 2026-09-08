1. Qué produce una ejecución

En una carpeta del capítulo, por ejemplo output/<slug-del-titulo>/:

output/leche-de-vaca/
├── guionLiterario.md
├── guionTecnico.md
└── imagenes/
    ├── ref-protagonista.png
    ├── escena-01-hook-super-leche.png
    ├── escena-02-introduccion.png
    └── ...

En ambos .md, cada escena incluye:

![Escena 1 — Hook: Súper Leche de Vaca](imagenes/escena-01-hook-super-leche.png)

───

2. Crear el esqueleto del plugin

Desde la raíz del repo:

mkdir -p .grok/plugins/storyboard-juicio/.grok-plugin
mkdir -p .grok/plugins/storyboard-juicio/skills/storyboard-juicio/references
mkdir -p .grok/plugins/storyboard-juicio/skills/storyboard-juicio/examples

Grok descubre plugins de proyecto en .grok/plugins/. También vale ~/.grok/plugins/storyboard-juicio/ (ámbito de usuario, auto-confiable).

Árbol esperado:

.grok/plugins/storyboard-juicio/
├── .grok-plugin/
│   └── plugin.json
├── plugin.json
├── README.md
└── skills/
    └── storyboard-juicio/
        ├── SKILL.md
        ├── references/
        │   ├── personajes.md
        │   ├── estructura-guion.md
        │   ├── estilos-visuales.md
        │   └── plantillas.md
        └── examples/
            └── escena-ejemplo.md

.claude-plugin/plugin.json es el equivalente Claude; en Grok basta .grok-plugin/plugin.json más el plugin.json de raíz.

───

3. Manifestos

.grok/plugins/storyboard-juicio/plugin.json

{
  "name": "storyboard-juicio",
  "version": "0.1.0",
  "description": "Genera guion literario y técnico en Markdown y bocetos PNG por escena para el canal Juicio Alimento Apetecible.",
  "author": { "name": "Norberto Velasco" },
  "keywords": ["juicio", "guion", "storyboard", "alimento"]
}

.grok/plugins/storyboard-juicio/.grok-plugin/plugin.json

Mismos campos. Grok carga skills desde skills/*/SKILL.md por auto-descubrimiento.

───

4. Escribir SKILL.md (el flujo del agente, actualmente con el nombre storyboard-juicio.md)

5. Archivos de referencia (una sola fuente de verdad)

No copiar guion-juicio entero dentro de SKILL.md. El skill apunta a:

┌───────────────────┬──────────────────────────────────────────────────────────────────────┐
│ Archivo           │ Contenido                                                            │
├───────────────────┼──────────────────────────────────────────────────────────────────────┤
│ references/       │ Beto (fiscal, VO), Beti (defensa, VO, frases cortas), protagonista ( │
│ personajes.md     │ alimento antropomorfizado). Extraído de JuicioAlimentoApetecible.md. │
├───────────────────┼──────────────────────────────────────────────────────────────────────┤
│ references/       │ Actos 1–6, slugline, campos del técnico.                             │
│ estructura-guion  │                                                                      │
│ .md               │                                                                      │
├───────────────────┼──────────────────────────────────────────────────────────────────────┤
│ references        │ Los 4 hooks: paleta, vestuario, pose, luz del Acto 1, qué no cambia  │
│ /estilos-visuales │ entre escenas.                                                       │
│ .md               │                                                                      │
├───────────────────┼──────────────────────────────────────────────────────────────────────┤
│ references/       │ Bloques markdown de literario y técnico con el ![]() del PNG.        │
│ plantillas.md     │                                                                      │
├───────────────────┼──────────────────────────────────────────────────────────────────────┤
│ examples/escena-  │ Recorte de LecheGuionLiterarioEscena1a4Grok.md como tono.            │
│ ejemplo.md        │                                                                      │
└───────────────────┴──────────────────────────────────────────────────────────────────────┘

───

6. Habilitar el plugin en este repo

En .grok/config.toml (proyecto) o ~/.grok/config.toml:

[plugins]
enabled = ["storyboard-juicio"]

Plugins de proyecto en .grok/plugins/ requieren confianza:

grok plugin install ./ .grok/plugins/storyboard-juicio --trust
# o, si ya está en el árbol del repo:
grok plugin enable storyboard-juicio

Validar:

grok plugin validate .grok/plugins/storyboard-juicio
grok plugin details storyboard-juicio
grok inspect

En la TUI: /plugins → recargar con r. El slash /storyboard-juicio debe aparecer en segundos.

───

7. Uso

/storyboard-juicio

El agente pregunta título y estilo, o:

/storyboard-juicio Leche de Vaca Superheroína

También se dispara si el usuario pide “guion literario y técnico con storyboard” o “bocetos PNG de las escenas”.

───

8. Qué no meter en este plugin

• UI de tres columnas, tabla de preview y minimap de escenas del borrador storyboard-juicio.md: eso es una app web, no un plugin de Grok. El plugin trabaja por slash command + archivos en disco.
• PDF, ZIP de descarga o botón GENERAR: fuera de alcance de un plugin de skills.
• Mezcla literario+técnico en un tercer archivo: el usuario pidió solo guionLiterario.md y guionTecnico.md.
• Un PNG único tipo contact sheet: un storyboard de varias viñetas en una sola generación rompe caras y paneles. Un PNG por escena, enlazado en el markdown.

───

9. Orden de implementación (cuando pases de la descripción al código)

1. Crear carpetas y plugin.json.
2. Extraer references/ desde guion-juicio y JuicioAlimentoApetecible.md.
3. Escribir SKILL.md con los pasos A–G.
4. Añadir examples/escena-ejemplo.md.
5. Habilitar el plugin y validar.
6. Probar con un capítulo corto (4 escenas) y comprobar que los ![]() resuelven a PNG existentes.
7. Recién entonces ampliar a los 6 actos completos.

Si quieres, el siguiente paso es crear esos archivos en .grok/plugins/storyboard-juicio/ y dejarte /storyboard-juicio listo para invocar.