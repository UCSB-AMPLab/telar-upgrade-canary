---
layout: default
title: Resumen de actualización
---

## Resumen de actualización
- **Desde:** 1.6.2
- **Hasta:** 1.7.0
- **Fecha:** 2026-09-10
- **Cambios automatizados:** 70
- **Pasos manuales:** 5

## Cambios automatizados aplicados

### Configuración (2 archivos)

- [x] Updated requirements.txt — Python dependencies for the build and upgrade scripts
- [x] Updated package.json — Dependency metadata and build scripts for v1.7.0

### Layouts (3 archivos)

- [x] Updated _layouts/index.html — Home page layout — loads the per-page home bundle
- [x] Updated _layouts/object.html — Object page layout — loads the per-page object bundle
- [x] Updated _layouts/objects-index.html — Objects index layout — loads the per-page index bundle

### Includes (1 archivo)

- [x] Updated _includes/iiif-url-warning.html — Warning shown when a IIIF URL cannot be used as given

### Scripts (56 archivos)

- [x] Updated assets/js/README.md — How the JavaScript in this directory is organised and rebuilt
- [x] Updated assets/js/home-page.js — Home page bundle
- [x] Updated assets/js/home-page.js.map — Source map for the home page bundle
- [x] Updated assets/js/iiif-thumbnails/resolve.js — Resolves a thumbnail URL from a IIIF manifest
- [x] Updated assets/js/iiif-thumbnails/explicit-thumbnails.js — Honours thumbnails declared in the spreadsheet
- [x] Updated assets/js/iiif-thumbnails/home.js — Thumbnail loading for the home page
- [x] Updated assets/js/iiif-thumbnails/objects-index.js — Thumbnail loading for the objects index
- [x] Updated assets/js/iiif-url-warning.js — IIIF URL warning bundle
- [x] Updated assets/js/iiif-url-warning.js.map — Source map for the IIIF URL warning bundle
- [x] Updated assets/js/iiif-url-warning/main.js — IIIF URL warning entry module
- [x] Updated assets/js/object-page.js — Object page bundle
- [x] Updated assets/js/object-page.js.map — Source map for the object page bundle
- [x] Updated assets/js/object-page/main.js — Object page entry module
- [x] Updated assets/js/object-page/image-object.js — Image object viewer
- [x] Updated assets/js/object-page/video-object.js — Video object player
- [x] Updated assets/js/object-page/audio-object.js — Audio object player
- [x] Updated assets/js/object-page/clip-panel.js — Clip panel for timed media
- [x] Updated assets/js/object-page/copy-feedback.js — Feedback shown when a link or citation is copied
- [x] Updated assets/js/objects-filter.js — Objects filter bundle
- [x] Updated assets/js/objects-filter.js.map — Source map for the objects filter bundle
- [x] Updated assets/js/objects-filter/main.js — Objects filter entry module
- [x] Updated assets/js/objects-filter/matching.js — Whole-word and prefix matching for the objects index search
- [x] Updated assets/js/objects-filter/search-index.js — Builds the in-page search index for the objects index
- [x] Updated assets/js/objects-filter/escape.js — Escaping helpers shared by the filter modules
- [x] Updated assets/js/objects-index-page.js — Objects index page bundle
- [x] Updated assets/js/objects-index-page.js.map — Source map for the objects index page bundle
- [x] Updated assets/js/share-panel.js — Share panel bundle
- [x] Updated assets/js/share-panel.js.map — Source map for the share panel bundle
- [x] Updated assets/js/share-panel/main.js — Share panel entry module
- [x] Updated assets/js/share-panel/warnings.js — Warnings the share panel raises about a link
- [x] Updated assets/js/telar-story.js — Story engine bundle
- [x] Updated assets/js/telar-story.js.map — Source map for the story engine bundle
- [x] Updated assets/js/telar-story/card-pool.js — Card pool the story engine reuses while scrolling
- [x] Updated assets/js/telar-story/navigation.js — Story navigation and deep linking
- [x] Updated scripts/upgrade.py — Upgrade launcher — downloads and runs the newest release's verified tooling
- [x] Updated scripts/build_local_site.py — Local build helper
- [x] Updated scripts/check_jekyll_conflicts.py — Reads the Jekyll build log and reports two files claiming one destination
- [x] Updated scripts/encrypt_protected_stories.py — Encrypts protected stories after the build
- [x] Updated scripts/generate_collections.py — Generates Jekyll collections and records the story page manifest
- [x] Updated scripts/generate_iiif.py — Generates IIIF tiles and manifests for self-hosted images
- [x] Updated scripts/iiif_utils.py — Shared IIIF helpers
- [x] Updated scripts/process_pdf.py — Converts PDF sources into page images
- [x] Updated scripts/telar/build_conflicts.py — Parses build-log conflicts for the conflict check
- [x] Updated scripts/telar/demo.py — Demo content handling
- [x] Updated scripts/telar/story_pages.py — Works out where each story renders
- [x] Updated scripts/telar/widgets.py — Widget rendering helpers
- [x] Updated scripts/telar/processors/stories.py — Story spreadsheet processing
- [x] Updated scripts/telar/processors/objects/__init__.py — Object processing package — replaces processors/objects.py
- [x] Updated scripts/telar/processors/objects/christmas_tree.py — Object processing: layered image trees
- [x] Updated scripts/telar/processors/objects/featured.py — Object processing: featured objects
- [x] Updated scripts/telar/processors/objects/frame.py — Object processing: framing and cropping
- [x] Updated scripts/telar/processors/objects/local.py — Object processing: self-hosted objects
- [x] Updated scripts/telar/processors/objects/remote.py — Object processing: remote IIIF objects
- [x] Removed assets/js/iiif-thumbnails.js — superseded by the files installed with this upgrade
- [x] Removed scripts/telar/processors/objects.py — superseded by the files installed with this upgrade
- [x] Se eliminó scripts/migrations/: este sitio usa el lanzador de actualización, que descarga una copia verificada de las migraciones cada vez que se ejecuta.

### Documentación (2 archivos)

- [x] Updated README.md — Project README, updated for v1.7.0
- [x] Updated CHANGELOG.md — Release history through v1.7.0

### Otro (6 archivos)

- [x] Updated .gitattributes — Line-ending and diff rules for the repository
- [x] Updated .ruby-version — Ruby version Telar builds against (3.2)
- [x] Updated Gemfile — Ruby dependencies for the Jekyll build
- [x] Updated Gemfile.lock — Resolved Ruby dependencies, carrying the Ruby version the Gemfile requires
- [x] Updated package-lock.json — Regenerated dependency lockfile matching package.json — always ships with it
- [x] Added _data/telar-build/ to .gitignore — the story page manifest generate_collections.py writes there is build output, regenerated on every build

## Pasos manuales necesarios

Por favor completa estos pasos:

1. **Actualiza `.github/workflows/build.yml` a mano (recomendado).** Si actualizas el sitio con el Compositor de Telar, sáltate este paso y los dos siguientes: el Compositor actualiza los archivos de workflow por ti. GitHub no permite que esta actualización modifique archivos de workflow, así que este paso lo haces tú: copia el `build.yml` actual del repositorio de Telar sobre el tuyo (ábrelo en GitHub, usa «Copy raw contents», reemplaza el archivo completo y confirma el cambio). El workflow nuevo lee el registro que Jekyll deja al construir el sitio y detiene la construcción cuando dos archivos apuntan al mismo destino, en vez de dejar que uno de los dos gane sin avisar. Eso importa más de lo que parece: la página que desaparece en silencio puede ser justo la que debía llevar el texto cifrado de una historia protegida. El workflow nuevo también trae al día las versiones fijadas de las acciones de GitHub. ([guía](https://telar.org/guia/configuracion/actualizacion/))
2. **Actualiza `.github/workflows/upgrade.yml` a mano (recomendado, no urgente).** La restricción es la misma: GitHub no permite que la actualización lo modifique por ti. Copia el `upgrade.yml` actual del repositorio de Telar sobre el tuyo (ábrelo en GitHub, usa «Copy raw contents», reemplaza el archivo completo y confirma el cambio). El workflow nuevo ejecuta el motor de actualización que viene en las herramientas verificadas que descarga. Tu copia actual sigue sirviendo, así que es cuestión de orden y no un requisito: las herramientas que descarga ahora empiezan por un lanzador que busca por su cuenta el lanzamiento más reciente. ([guía](https://telar.org/guia/configuracion/actualizacion/))
3. **Actualiza `.github/workflows/telar-tests.yml` a mano (opcional).** Aquí rige la misma restricción. En este lanzamiento solo cambiaron las versiones fijadas de las acciones, así que tu sitio se comporta igual lo hagas o no. Si prefieres tener todos los workflows al día, copia el `telar-tests.yml` actual del repositorio de Telar sobre el tuyo (ábrelo en GitHub, usa «Copy raw contents», reemplaza el archivo completo y confirma el cambio). ([guía](https://telar.org/guia/configuracion/actualizacion/))
4. **Si trabajas en el sitio desde tu computador, cambiaron dos cosas.** Telar ahora necesita Ruby 3.2 o una versión más nueva, y la integración continua construye el sitio con la 3.2.11. Instala al menos la versión 3.2 antes de la próxima construcción local. Y `scripts/upgrade.py` ya no es la herramienta de actualización, sino un lanzador: al ejecutarlo, descarga las herramientas verificadas del lanzamiento más reciente y con ellas actualiza el sitio. Así, tu copia de `scripts/upgrade.py` nunca vuelve a quedarse atrás, por mucho tiempo que pase entre una actualización y otra. ([guía](https://telar.org/guia/configuracion/actualizacion/))
5. **Lo que cambió para tu contenido.** Ahora puedes indicar `width` y `height` en los elementos de un carrusel, y así la construcción no tiene que abrir cada imagen para medirla. En el índice de objetos, la búsqueda encuentra palabras completas, además de los comienzos de palabra. En los objetos de una sola página, las coordenadas que copias ya no traen número de página. Y si el identificador de una historia protegida lleva un guion bajo, la construcción ahora cifra el texto de la historia en la página que Jekyll produce realmente para ella. ([guía](https://telar.org/guia))

## Recursos

- [Documentación completa](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Reportar problemas](https://github.com/UCSB-AMPLab/telar/issues)
