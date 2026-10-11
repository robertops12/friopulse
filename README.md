# FríoPulse — Landing Page

Landing page comercial para **FríoPulse**, sistema IoT B2B de monitorización de cámaras frigoríficas y congeladores para hostelería y sanidad.

Sitio 100 % estático (HTML + Tailwind CSS vía CDN). No requiere build ni dependencias.

## Archivos

| Archivo | Descripción |
|---|---|
| `index.html` | Página completa (estructura, estilos Tailwind y JavaScript). |
| `netlify.toml` | Configuración de despliegue y cabeceras de seguridad para Netlify. |

## Ver en local

Abre `index.html` en el navegador o sirve la carpeta:

```bash
npx serve .
```

## Desplegar en Netlify

### Opción A — Desde GitHub (recomendado)

1. Crea un repositorio nuevo en GitHub y sube esta carpeta:

   ```bash
   git init
   git add .
   git commit -m "Landing page FríoPulse"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/friopulse.git
   git push -u origin main
   ```

2. Entra en [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import an existing project**.
3. Conecta tu cuenta de GitHub y elige el repositorio `friopulse`.
4. Configura:
   - **Build command:** *(vacío)*
   - **Publish directory:** `.`
5. Pulsa **Deploy site**. Netlify leerá `netlify.toml` automáticamente.

### Opción B — Arrastrar y soltar

Entra en [app.netlify.com/drop](https://app.netlify.com/drop) y arrastra esta carpeta.

## Personalización

- **Colores corporativos:** variables en `tailwind.config` dentro de `index.html` (paleta `brand` + acentos `cyan`/`emerald`).
- **Datos de contacto:** busca `+34 600 000 000` y `hola@friopulse.com` en `index.html`.
- **Envío del formulario:** la función de simulación está en el `<script>` final (bloque *Formulario: simulación de envío*). Para conectarlo a un servicio real (Netlify Forms, Formspree, etc.), sustituye el `setTimeout` por tu `fetch`/endpoint.
