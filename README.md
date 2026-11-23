# Catálogo — fichas con filtros Y / O / NO

Catálogo personal para lo que quieras (juegos, libros, películas, inventario…). Tú defines los campos (categoría, dificultad, etiquetas, números, fechas…) y luego filtras combinando condiciones con **Y**, **O** y **NO**. Se instala como app (PWA) en el PC (Chrome) y en Android.

**App:** https://carlosmera10.github.io/catalogo/

## Qué hace

- **Varios catálogos**, cada uno con sus propios campos. Plantillas: vacío, juegos de mesa (con 14 ejemplos y vistas de prueba), libros, películas y series, inventario.
- **Tipos de campo**: texto corto, texto largo, número, fecha, categoría (una opción), etiquetas (varias opciones), sí/no, valoración (estrellas), enlace e imagen (foto del móvil, reducida automáticamente, o URL).
- **Filtros rápidos** (panel lateral) para categorías, etiquetas, sí/no y valoración:
  - un toque **incluye**, otro **excluye (NO)**, otro quita;
  - dentro de un campo las opciones se unen con **O**; en etiquetas se puede pedir **alguna (O)** o **todas (Y)**;
  - entre campos, **Y** (o **O**, si se cambia);
  - cada opción muestra cuántas fichas saldrían.
- **Filtro avanzado**: condiciones sobre cualquier campo (contiene, =, ≥, entre, antes de, en los últimos N días, tiene alguna/todas/ninguna…), agrupadas con paréntesis, cada grupo con Y u O y con NO para invertirlo. Muestra la expresión en lenguaje normal y el recuento en directo.
- **Búsqueda** en todos los campos, sin tildes ni mayúsculas: varias palabras = todas, `-palabra` excluye, `"frase exacta"`.
- **Vistas guardadas**: búsqueda + filtros rápidos + filtro avanzado + orden, con un toque.
- **Orden** por cualquier campo (las categorías se ordenan según el orden de sus opciones) y aleatorio.
- **Tres vistas**: tarjetas, lista y tabla (pulsando la cabecera se ordena).
- **🎲 Al azar**: elige una ficha entre las filtradas.
- **📊 Resumen**: recuentos por opción y mínimo / media / máximo / suma de los números, sobre lo filtrado.
- **Ficha**: navegación anterior/siguiente, duplicar, borrar con «Deshacer»; tocar una etiqueta filtra por ella.
- **Importar / exportar**: copia de seguridad completa (.json), catálogo suelto (.json), CSV con punto y coma para Excel (todo o lo filtrado), importar CSV o **pegar celdas de Excel** (crea los campos que falten y adivina su tipo).
- Tema claro / oscuro / automático. Atajos: `/` buscar, `N` nueva ficha, `Esc` cerrar, `←` `→` en el detalle.

Los datos se guardan **solo en el dispositivo** (IndexedDB del navegador). Para pasarlos de un dispositivo a otro, usa la copia de seguridad.

## Archivos

| Archivo | Para qué |
|---|---|
| `index.html` | Toda la app (HTML + CSS + JS, sin dependencias) |
| `app.webmanifest` | Datos para instalarla como aplicación |
| `sw.js` | Service worker: funciona sin conexión. Si lo cambias, sube el número de `CACHE` |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Iconos |
