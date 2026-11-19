# Universidad AmarYYa · Cartera & Comisiones

App web para llevar la cartera, los pagos, las comisiones y las sesiones personalizadas de Universidad AmarYYa.

## Archivos
| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa (v4.19), con los datos base embebidos |
| `netlify.toml` | Configuración de publicación en Netlify |
| `.gitignore` | Evita subir respaldos con datos personales |

## Dónde se guardan los datos
En el repositorio privado **amaryya-datos**, carpeta `datos/`: un archivo por tabla (estudiantes, pagos, sesiones, closers, programas…).
Cada persona entra solo con su **usuario y contraseña** de la app, según su rol.
El acceso a GitHub va cifrado por usuario en `llaves.json`, que la app crea y actualiza sola en este repositorio.

## Publicar una versión nueva
1. **Add file → Upload files** → subir el nuevo `index.html` con el mismo nombre.
2. **Commit changes**. Netlify publica la nueva versión en segundos.

## Volver a una versión anterior
Abrir `index.html` → **History** → elegir la versión → **⋯ → View file** → descargar y volver a subir.
