# Universidad AmarYYa · Cartera & Comisiones

App web para llevar la cartera, los pagos, las comisiones y las sesiones personalizadas de Universidad AmarYYa.

## Archivos
| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa (v4.18), con los datos base embebidos |
| `netlify.toml` | Configuración de publicación en Netlify |
| `.gitignore` | Evita subir respaldos con datos personales |

## Dónde se guardan los datos
En el repositorio privado **amaryya-datos**, carpeta `datos/`: un archivo por tabla (estudiantes, pagos, sesiones, closers, programas…).
Cada persona se conecta una sola vez con el usuario de GitHub, el nombre del repositorio de datos y su token.

## Publicar una versión nueva
1. **Add file → Upload files** → subir el nuevo `index.html` con el mismo nombre.
2. **Commit changes**. Netlify publica la nueva versión en segundos.

## Volver a una versión anterior
Abrir `index.html` → **History** → elegir la versión → **⋯ → View file** → descargar y volver a subir.
