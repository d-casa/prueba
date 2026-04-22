# D'Casa · Eventos & Alquiler

Sitio web oficial de D'Casa Eventos & Alquiler, organizadora de eventos con cobertura en Santa Ana Xalmimilulco, Puebla capital y Zacatelco.

## 📁 Estructura

```
dcasa-site/
├── index.html              ← El sitio completo (HTML + CSS + JS en un solo archivo)
└── assets/
    ├── logo.jpg            ← Logo D'Casa (también usado como favicon)
    ├── branding-carpa.jpg  ← Branding de respaldo (no se usa en la página)
    ├── galeria-mesa-principal.jpg
    ├── galeria-iglesia.jpg
    ├── galeria-xv-centros.jpg
    └── galeria-bautizo.jpg
```

**Todas las rutas son relativas** (`assets/...`), por lo que funciona tanto en:
- `https://usuario.github.io/` (repo raíz)
- `https://usuario.github.io/dcasa/` (subdirectorio)
- Cualquier dominio propio

---

## 🚀 Cómo publicar en GitHub Pages

### Opción A — Repo nuevo (recomendada)

1. Crea un repositorio en GitHub, por ejemplo `dcasa-site`.
2. Sube los dos elementos a la raíz del repo:
   - `index.html`
   - carpeta `assets/`
3. En el repo, ve a **Settings → Pages**.
4. En *Source*, elige la rama (`main` o `master`) y carpeta `/ (root)`.
5. Guarda. En 1–2 minutos tu sitio estará en `https://TU-USUARIO.github.io/dcasa-site/`.

### Opción B — Dominio personalizado

1. En la misma pantalla de *Pages*, agrega tu dominio (ej. `alquilerdcasa.com`) en *Custom domain*.
2. En tu proveedor de DNS crea un registro `CNAME` apuntando a `TU-USUARIO.github.io`.
3. Espera la propagación (minutos a horas) y activa *Enforce HTTPS*.

### Opción C — Desde línea de comandos

```bash
git init
git add .
git commit -m "Sitio D'Casa inicial"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/dcasa-site.git
git push -u origin main
```

Luego activa Pages desde la configuración del repo.

---

## ✏️ Cómo editar el sitio

Todo está en un solo archivo `index.html`. Las secciones están marcadas con comentarios (`<!-- NOSOTROS -->`, `<!-- GALERÍA -->`, etc.) para localizarlas rápido.

### Cambiar el número de WhatsApp
Busca `522271012702` en el archivo y reemplázalo. El `52` al inicio es el código de México (necesario para que WhatsApp abra con el número correcto).

### Cambiar el Facebook
Busca `facebook.com/search/top?q=Alquiler%20D'Casa` y reemplázalo con la URL completa de la página de Facebook cuando la tengas (ej. `https://www.facebook.com/AlquilerDCasaOficial`).

### Agregar más fotos a la galería
1. Agrega la imagen a `assets/`.
2. En la sección `<!-- GALERÍA -->`, duplica un bloque `<figure class="galeria__item">...` y ajusta `src`, `alt` y el texto de la etiqueta.
3. El grid se autoajusta en móvil; en desktop puedes modificar el `grid-column: span` en el CSS para controlar el tamaño.

### Cambiar testimonios
En el bloque `<script>` al final, busca el array `const testimonios = [...]`. Edita el texto, nombre y evento. Los tres testimonios actuales son **plantillas de ejemplo** — reemplázalos con comentarios reales de tus clientes cuando los tengas.

### Cambiar colores
Todos los colores están en variables CSS al inicio (`:root`). Los principales:
- `--ink` — Negro principal
- `--ivory` — Crema de fondo
- `--gold` — Dorado champagne (acentos)
- `--rose` — Rosa polvo (sutiles resaltes)

---

## 🎨 Decisiones de diseño

- **Tipografía:** *Italiana* (display muy fino) + *Cormorant Garamond* (itálica romántica) + *Jost* (cuerpo moderno). Se cargan de Google Fonts.
- **Paleta:** Marfil cálido, tinta profunda, dorado champagne y detalles en rosa polvo. Respeta el logo minimalista y se alinea con la estética romántica de tus fotos.
- **Movimiento:** Preloader con reveal de letras, hero con staggered entry, fade-in por scroll con `IntersectionObserver`, Ken Burns sutil en la imagen del hero, hover orgánico en cards y galería.
- **Performance:** Un solo archivo HTML, sin frameworks, sin build. Imágenes con `loading="lazy"` excepto la del hero.
- **Accesibilidad:** `prefers-reduced-motion` respetado, `aria-label` en íconos, contraste AA en textos principales, navegación por teclado funcional.

---

## 🔧 Próximas mejoras sugeridas

1. **Optimizar imágenes** — Las JPGs actuales están bien pero pueden convertirse a WebP para cargas más rápidas (usar [Squoosh](https://squoosh.app/)).
2. **Más fotos reales** — Idealmente 12–20 fotos en la galería para más variedad. Prioriza fotos horizontales y verticales mezcladas.
3. **Testimonios reales** — Reemplaza las 3 plantillas con comentarios auténticos de clientes (con permiso).
4. **Google Analytics** — Agregar el snippet antes del `</head>` para medir tráfico.
5. **Formulario de contacto** — Si quieres que manden mensajes sin WhatsApp, conectar con Formspree o Netlify Forms (ambos gratuitos hasta cierto volumen).
6. **Dominio propio** — `alquilerdcasa.com` o similar da mucha más profesionalidad que `usuario.github.io/...`

---

## 📞 Contacto comercial

- **WhatsApp:** 227 101 2702 · 222 527 0258
- **Horario:** Lunes a viernes, 8:00 – 17:00 h
- **Cobertura:** Santa Ana Xalmimilulco · Puebla capital · Zacatelco

---

*Donde la elegancia se encuentra con la perfección.*
