# Pagancillo · contenido de ejemplo

Repositorio público de contenido para una web Next.js. **Los alojamientos, comercios, eventos y parte de los textos son ficticios y solo sirven para desarrollo.** Cada registro de ejemplo tiene `demo: true`; la interfaz debe indicarlo de manera visible. No usar el repo de muestra como guía turística definitiva.

## Estructura

- `content/site.json`: portada, introducción, categorías y destacados.
- `content/places.json`: lugares y fichas.
- `content/activities.json`: experiencias.
- `content/accommodations.json`: alojamientos de demostración.
- `content/businesses.json`: comercios de demostración.
- `content/events.json`: eventos con fechas ficticias.
- `content/practical.json`: cómo llegar e información útil.
- `content/faqs.json`: preguntas frecuentes.
- `content/media.json`: créditos, fuentes y licencias de las fotografías.
- `images/`: imágenes reales de Talampaya y Cuesta de Miranda; ninguna representa el centro de Pagancillo.

## Subir a GitHub

Creá un repositorio público llamado `pagancillo-contenido` y copiá **el contenido de esta carpeta en la raíz**. Reemplazá `USUARIO` por tu usuario u organización real. No subas credenciales.

Ejemplo de URL de datos:

```text
https://raw.githubusercontent.com/USUARIO/pagancillo-contenido/main/content/places.json
```

Ejemplo de URL de imagen:

```text
https://raw.githubusercontent.com/USUARIO/pagancillo-contenido/main/images/talampaya-panorama.jpg
```

En la web Next.js, leé los JSON en componentes de servidor o en una capa `lib/content`. Configurá `next/image` con un `remotePatterns` restringido a `raw.githubusercontent.com/USUARIO/pagancillo-contenido/main/images/**`; no permitas cualquier URL externa. Si el sitio usa `output: 'export'`, los cambios del repo de contenido requieren un nuevo build. Si corre con servidor, podés configurar revalidación de datos. Los enlaces raw apuntan a `main`; para despliegues reproducibles podés fijar un commit SHA y actualizarlo cuando publiques contenido.

## Reemplazar las muestras

1. Sustituí registros ficticios por nombres, descripciones y datos reales.
2. Agregá coordenadas solo cuando conozcas su ubicación correcta.
3. Incorporá fotografías con autorización o licencia y agregá créditos en `media.json`.
4. Cambiá `demo` a `false` después de reemplazar los datos de ejemplo.
5. Si todavía no hay datos de una sección, dejá su array vacío: la web debe mostrar un estado vacío, no inventar registros.

Las fotografías incluidas están bajo licencias CC BY-SA; mantené créditos y enlace a la licencia. Consultá `content/media.json` para cada archivo.
