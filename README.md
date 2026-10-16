# Mood Radio 🎧

Cuestionario musical con IA. Una inteligencia artificial crea **12 preguntas** sobre tu
personalidad, tu estado de ánimo y tus gustos; después analiza tus respuestas y te
recomienda **5 canciones** hechas a tu medida.

## Qué hace

1. La IA genera un cuestionario nuevo de 12 preguntas cada vez.
2. Respondes una pregunta a la vez, con barra de progreso.
3. Al terminar, tus respuestas se envían de vuelta a la IA para analizar tu perfil.
4. Recibes tu perfil y un catálogo de 5 canciones. Cada una incluye **título, artista,
   género y una breve justificación** de por qué encaja contigo, con un botón para
   buscarla en Spotify.

## Tecnologías

- HTML, CSS y JavaScript (sin instalar nada, sin servidor)
- API de [Groq](https://console.groq.com) (capa gratuita) con el modelo `openai/gpt-oss-20b`

## Cómo usarlo

1. Descarga o clona este repositorio.
2. Consigue una clave de API gratuita en https://console.groq.com/keys
3. Copia `config.example.js` y nómbralo `config.js`.
4. Abre `config.js` y reemplaza `PEGA_AQUI_TU_CLAVE_DE_GROQ` por tu clave.
5. Abre `cuestionario-musical.html` en tu navegador (doble clic) y pulsa el botón de inicio.

## Archivos

| Archivo | Para qué sirve |
| --- | --- |
| `cuestionario-musical.html` | La aplicación completa (interfaz y lógica) |
| `config.example.js` | Plantilla de configuración, sin clave |
| `config.js` | Tu configuración con la clave. **No se sube a GitHub** (está en `.gitignore`) |
| `.gitignore` | Evita que `config.js` se suba al repositorio |

## Seguridad de la clave

- Nunca escribas tu clave dentro del HTML ni la subas a GitHub.
- Esta app llama a la API directamente desde el navegador, así que la clave es visible
  para quien use la página. Úsala en tu computadora. Si la publicas en internet
  (por ejemplo en GitHub Pages), cualquiera podría copiar la clave. Para eso haría falta
  un pequeño servidor que la guarde.
- Si una clave se expone por accidente, revócala en la consola de Groq y crea otra.
