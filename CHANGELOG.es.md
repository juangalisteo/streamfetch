# Historial de versiones

[English](CHANGELOG.md) · **Español**

Todos los cambios importantes de StreamFetch se apuntan aquí.
Formato basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/)
y versiones según [Semantic Versioning](https://semver.org/lang/es/).

## [1.0.0] · 04-11-2026

Primera versión. Hecha sobre la base de [VideoFetch](https://github.com/juangalisteo/videofetch) v1.2.0.

### Añadido
- Descarga de vídeos en streaming (`.m3u8` HLS, `.mpd` DASH, `.mp4` directos) de cualquier web.
- **02 · Página de origen** (*Referer*): se rellena sola según el enlace (p. ej. `tella.tv`)
  o se escribe a mano; se recuerda.
- Aviso de **enlace caducado**: lee la fecha de los enlaces firmados (CloudFront `Policy` / `Expires`).
- Botón **«¿Cómo consigo el enlace?»** con los pasos (F12 → Red → `m3u8` → Copiar URL).
- Mensajes claros para DRM, acceso denegado (403), no encontrado (404) y enlace no válido.
- Si el vídeo se llama «manifest», «master»…, el archivo se llama `StreamFetch <fecha>`.
- Descarga de trozos en paralelo y reintentos para vídeos largos.
- Lo mismo que VideoFetch: MP4 H.264 + AAC listo para editores, MP3, 720p / 1080p / Máxima,
  botón **SRT** (subtítulos del vídeo o creados con IA Whisper), ES / EN y modo consola
  (`--referer`, `--name`, `--srt`, `--lang en`).
- Color de la app: **verde** (`#22C55E`).
