# Contrato simple de contenido (v1)

Todos los archivos en `content/` son UTF-8 JSON. Los listados son arrays; `site.json` y `practical.json` son objetos. `slug` es único por colección. `id` es estable. Un campo sin dato se expresa con `null` o `[]`, nunca con un teléfono, dirección o coordenada inventados. Las imágenes usan rutas `/images/archivo.jpg`, que la aplicación transforma a la URL raw del repo. `demo: true` identifica ejemplos que deben rotularse como demostración en la UI; para contenido real usar `demo: false` después de sustituir los datos. Las imágenes de paisajes son reales y sus licencias/créditos están en `media.json`.

La aplicación debe validar el JSON, tolerar colecciones vacías y no fallar si faltan campos opcionales. No publicar coordenadas de mapa si son `null`.
