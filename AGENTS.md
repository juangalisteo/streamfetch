# AGENTS.md — Reglas para la IA · StreamFetch

Valen para cualquier agente que trabaje en este proyecto: Claude, Codex (ChatGPT) u otros. Aquí solo hay reglas permanentes; el estado del trabajo está en `AGENT_AI/ESTADO.md`.

## 1. Idioma y trato

- Respuestas siempre en **español**, con palabras sencillas: en el chat y en los archivos.
- Cuando haya que decidir algo, el agente da su recomendación y explica por qué en una o dos frases.
- Antes de cambiar nada, se explica qué se va a cambiar y se espera la confirmación del propietario.
- Si un archivo cambia, se entrega completo (guardado en la carpeta o para descargar), nunca en trozos para pegar.

## 2. Protección del trabajo

- Si el propietario dice que está descargando algo, no se toca nada hasta que avise.
- StreamFetch y VideoFetch comparten casi todo el código: en cada cambio se dice si afecta a uno o a los dos.
- Sin el sí del propietario no se sube nada a GitHub ni se crea una versión.
- Antes de borrar o sustituir algo, se dice qué es y se espera la confirmación del propietario. Si hay que borrar algo y el agente no puede, lo deja marcado de forma clara.
- Después de cada cambio, el propietario cierra y vuelve a abrir el programa: se le recuerda.

## 3. Código

- **Textos que ve el usuario:** nunca directamente en `interfaz.py` o `descargador.py`. Van en `APP/idiomas.py`, en español y en inglés, y se usan con `t("clave")`.
- **Comentarios y descripciones del código, en inglés.**
- Las rutas se calculan desde `APP/descargador.py` (`ROOT`, `LIB = SISTEMA`, `DOWNLOADS`): la carpeta se puede mover.
- Los nombres de archivos y carpetas del programa (`.cmd`, `SISTEMA`, `DOWNLOADS`, `APP`…) no se traducen ni se cambian, para no romper instalaciones.
- Diseño: fondo grafito monocromo y un solo color de señal, el verde `#22C55E`.
- No se programa nada para saltarse DRM.

## 4. Versiones

Si cambia la versión, se cambia en todos estos sitios a la vez: `APP_VERSION` (en `APP/interfaz.py`), `README.md` y `README.es.md`, `CHANGELOG.md` y `CHANGELOG.es.md`, los dos banners de `docs/`, `00_LEEME.txt` y `00_README_EN.txt`, y las cabeceras de los `.py`.

## 5. Nombres de carpetas y archivos

Las normas completas están en `00_CONFIG/02_NAMING.md`. En este proyecto el código y sus carpetas siguen el estándar de Python y de GitHub (`APP/`, `docs/`, `README.md`, `requirements.txt`…). Lo que no es código sigue las normas. No se cambian los nombres del sistema de trabajo con IA: `00_INICIO_CHAT.md`, `00_CONFIG/` y todo lo que hay en `AGENT_AI/`.

## 6. Escritura y comprobación

- Todo texto que se entregue (README, CHANGELOG, textos de la ventana, resúmenes) aplica `00_CONFIG/01_WRITING_RULES.md`, en los dos idiomas.
- Los cambios se prueban antes de guardarlos. Desde la nube no hay acceso a las webs de vídeo: se prueba con archivos locales y listas de formatos simuladas, y el propietario prueba con enlaces reales.
- Al guardar en el ordenador del propietario, se comprueba después (por el tamaño del archivo) que se ha guardado la versión nueva.

## 7. Publicación y privacidad

- Licencia **GPL-3.0-or-later** (`LICENSE`, texto oficial sin tocar). Autores: Juan Bautista Galisteo Marqués (@juangalisteo) y Juan Manuel Casado Triguero (@juanmacasado).
- `00_INICIO_CHAT.md`, `00_CONFIG/` y `AGENT_AI/` son privados: nunca se suben a GitHub (están en `.gitignore`). Al subir desde la web de GitHub, no se arrastran.

## 8. Al cerrar una tarea

- `AGENT_AI/ESTADO.md` se actualiza al terminar cada cambio: qué se hizo, qué está pendiente y cuál es el siguiente paso.
- Las preguntas sencillas no necesitan cierre.
