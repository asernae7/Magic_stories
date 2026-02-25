# Magic_stories
Magical Tales AI is an interactive web application designed to create personalized reading experiences for children using cutting-edge Artificial Intelligence. The application generates unique stories, magical illustrations, and real-time voice narration.

# Características principales

Personalización Total: Historias basadas en el nombre del niño, su edad, intereses (ej. dinosaurios, espacio) y valores morales (ej. compartir, valentía).

# Generación Multimodal:

- **Texto:** Historias creativas generadas por gemini-2.5-flash.

- **Imágenes:** Ilustraciones estilo Pixar generadas por imagen-4.0.

- **Audio:** Narración fluida con voz de "abuelo cuentacuentos" generada por gemini-2.5-flash-preview-tts.

Experiencia de Usuario Fluida:

- **Precarga Inteligente:** Mientras el niño lee la primera página, el sistema genera y descarga en segundo plano las imágenes y audios de las páginas siguientes.

- **Cero Latencia:** Una vez precargado, el cambio de página y la reproducción de audio son instantáneos.

- **Manejo de Errores de Imagen:** Sistema de limpieza de caché visual al pasar de página para evitar parpadeos o imágenes incorrectas.

- **Diseño Adaptable:** Interfaz colorida y amigable optimizada para dispositivos móviles y tablets.

# 🚀 Tecnologías utilizadas

Frontend: HTML5, CSS3 (Tailwind CSS), JavaScript (Vanilla).

**IA / Modelos:**

`gemini-2.5-flash-preview-09-2025` (Generación de contenido).

`imagen-4.0-generate-001` (Generación de imágenes).

`gemini-2.5-flash-preview-tts` (Conversión de texto a voz).


# 🛠️ Instalación y Uso

Clona este repositorio o descarga el archivo index.html.

Abre el archivo index.html en cualquier navegador moderno.

Introduce tu apiKey de Google Gemini en la constante correspondiente dentro del script:
```
const apiKey = "TU_API_KEY_AQUÍ";
```
¡Empieza a crear historias mágicas!

# 🧠 Lógica de Precarga (Asset Pipeline)

Para evitar interrupciones en la lectura, el proyecto implementa un sistema de colas:

Se genera la estructura JSON del cuento completo.

Se inicia la carga de la Página 1 (Prioridad Alta).

Se ejecuta un bucle async que procesa el resto de páginas en paralelo (Imagen + Audio).

Cada página cuenta con un indicador visual de estado (Puntos de precarga) que muestra cuándo los recursos están listos.

# 📝 Licencia

Este proyecto es de uso educativo y personal. Las APIs utilizadas pertenecen a Google Generative AI.

Creado con ❤️ para fomentar la lectura en los más pequeños.
