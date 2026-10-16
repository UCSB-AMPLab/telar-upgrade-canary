---
layout: default
title: Resumen de actualización
---

## Resumen de actualización
- **Desde:** 1.8.1
- **Hasta:** 1.8.2
- **Fecha:** 2026-10-16
- **Cambios automatizados:** 13
- **Pasos manuales:** 2

## Cambios automatizados aplicados

### Configuración (2 archivos)

- [x] Se actualizó package.json
- [x] Se actualizó package-lock.json

### Scripts (7 archivos)

- [x] Se actualizó scripts/dev-only-files.txt
- [x] Se actualizó scripts/telar/dev_only_files.py
- [x] Se eliminó scripts/migrations/: este sitio usa el lanzador de actualización, que descarga una copia verificada de las migraciones cada vez que se ejecuta.
- [x] Se eliminó scripts/telar_upgrade.py: la actualización se ejecuta con las herramientas verificadas que descarga `scripts/upgrade.py`
- [x] Se eliminó scripts/telar_upgrade_common.py: la actualización se ejecuta con las herramientas verificadas que descarga `scripts/upgrade.py`
- [x] Se eliminó scripts/telar_upgrade_regen.py: la actualización se ejecuta con las herramientas verificadas que descarga `scripts/upgrade.py`
- [x] Se eliminó scripts/telar_upgrade_report.py: la actualización se ejecuta con las herramientas verificadas que descarga `scripts/upgrade.py`

### Documentación (2 archivos)

- [x] Se actualizó README.md
- [x] Se actualizó CHANGELOG.md

### Otros (2 archivos)

- [x] telar-content/spreadsheets/glossary.csv: la entrada sobre Telar quedó solo en el idioma de tu sitio
- [x] telar-content/spreadsheets/glossary.csv: las filas de instrucciones ahora indican la carpeta telar-content/texts/glossary/

## Pasos manuales necesarios

Por favor completa estos pasos:

1. **Borra `.github/workflows/telar-tests.yml` (opcional).** Este workflow ejecuta las pruebas del propio Telar y solo corre en los repositorios de Telar; en tu sitio no hace más que aparecer como una verificación omitida. GitHub no permite que una actualización automática modifique archivos de workflow, y por eso borrarlo te toca a ti. Los archivos de pruebas pueden quedarse: no intervienen en nada de lo que el sitio construye o publica. ([guía](https://telar.org/guia/configuracion/actualizacion/))
2. **Deja en un solo idioma la entrada sobre Telar en tu hoja del glosario.** La actualización ya quitó el párrafo en el otro idioma de la fila «telar» de glossary.csv, pero tu sitio toma las hojas de cálculo de Google Sheets, así que la próxima construcción vuelve a traer los dos párrafos. En la hoja del glosario, borra de la definición de la fila «telar» el párrafo en el otro idioma. ([guía](https://telar.org/guia/configuracion/actualizacion/))

## Recursos

- [Documentación completa](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Reportar problemas](https://github.com/UCSB-AMPLab/telar/issues)
