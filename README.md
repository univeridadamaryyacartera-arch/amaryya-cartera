# Universidad AmarYYa · Cartera & Comisiones (v4.18)

App web para llevar y analizar la cartera de la Universidad AmarYYa: estudiantes, pagos, comisiones de closers y apoyo, terapeutas, sesiones personalizadas, bolsillo y panel gerencial.

**Acceso libre:** la app no tiene usuarios, contraseñas ni roles. Cualquier persona que abra el enlace puede leer, registrar, editar y eliminar toda la información. Comparte el enlace solo con el equipo.

## Archivos del repositorio

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa. Trae como datos base 65 estudiantes y 69 pagos (exportación 2026-11-05). |
| `netlify/functions/db.mjs` | Base de datos compartida del equipo (Netlify Functions + Netlify Blobs). |
| `netlify.toml` | Configuración de publicación en Netlify. |
| `package.json` | Dependencia de la base de datos (`@netlify/blobs`). Netlify la instala sola. |
| `.gitignore` | Archivos que no se suben a GitHub. |

## Cómo subirlo a GitHub (sin programas, desde el navegador)

1. Entra a tu repositorio **amaryya-cartera** en github.com (usuario AngelaYPC).
2. Si ya existía un `index.html` anterior, se reemplazará al subir el nuevo.
3. Clic en **Add file → Upload files**.
4. Descomprime el ZIP en tu computador y **arrastra todo el contenido** (no la carpeta exterior): `index.html`, `netlify.toml`, `package.json`, `README.md`, `.gitignore` y la carpeta `netlify`.
   - Si `.gitignore` no aparece (archivo oculto), no importa; es opcional.
   - Verifica que quede la ruta `netlify/functions/db.mjs` dentro del repositorio.
5. Escribe un mensaje como "v4.18 acceso libre" y clic en **Commit changes**.

## Cómo publicarlo en Netlify

- **Si el sitio ya está conectado a este repositorio:** Netlify publica solo al recibir el commit (en 1–2 minutos).
- **Si es la primera vez:** en app.netlify.com → **Add new site → Import an existing project → GitHub** → elige `amaryya-cartera`. Deja los campos como vienen (el `netlify.toml` ya los define) y clic en **Deploy**.

No hay que configurar claves ni variables: Netlify Blobs viene incluido en el sitio.

## Primer uso

- La primera vez que alguien abre la app publicada, la base está vacía y se carga sola con los datos base (65 estudiantes, 69 pagos).
- **Si ya registraron información en la versión de Claude** y quieres pasarla a Netlify: en la versión de Claude ve a **Ajustes → ⬇ Copia de seguridad (JSON)**; luego, en la versión de Netlify, en **Ajustes** elige ese archivo y usa **🔍 Revisar copia** para restaurarlo.
- En **Ajustes** aparece "🟢 Compartido con tu equipo". El botón **Probar guardado** confirma que todas las tablas guardan bien.

## Cómo funciona la información compartida

- Todo lo que alguien registra se guarda en la base de Netlify y aparece en las pantallas de las demás personas en unos 5 segundos.
- Si dos personas guardan al mismo tiempo, la base aplica ambos cambios sin perder ninguno.
- Si abres `index.html` directamente desde tu computador (doble clic), **no** se conecta a la base: verás un aviso y lo que registres no se comparte.

## Limitación conocida

- **Lectura automática de comprobantes** (subir la imagen y detectar valor, moneda, fecha y plataforma): solo funciona dentro de Claude. En Netlify el pago se registra escribiendo los datos a mano.
