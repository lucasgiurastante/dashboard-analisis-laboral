# Analizador de Propuestas Laborales — Dashboard Genérico

Dashboard 100% client-side para analizar ofertas laborales. **No incluye datos personales en el repo** — los datos de Yanaina quedan en su Google Sheet privado.

## Cómo usar (para Yanaina)

1. Abrí el link de GitHub Pages: `https://TUUSER.github.io/yanaina-dashboard/`
2. Pegá en el recuadro superior el link de tu Google Sheet con columnas: `job_id, fecha_scrapeo, titulo, empresa, ubicacion, modalidad, url, notas`
3. Click **Cargar Sheet →** — el dashboard calcula `skills/score/salario` y muestra análisis completo
4. Para actualizar: agregá nuevas rows en el Sheet y volvé a hacer click en **↻ Sincronizar Sheets** — aparece cartel `¡X trabajos nuevos cargados!` (repetidos por `job_id` se ignoran)

## Requisitos del Sheet

- Compartir → Cualquiera con el link → Lector
- Archivo → Compartir → Publicar en la web → Hoja `RAW_TRABAJOS` → CSV → Publicar (para evitar bloqueo CORS)

## Archivos

- `index.html` / `dashboard.html` — dashboard genérico (3 demos embebidos, sin datos reales)
- `yanaina_jobs.json` — solo demo de 3 filas (no subir datos reales)
- `.gitignore` — ignora `*.private.json`

## Privacidad

Los datos reales nunca se suben a GitHub. Solo se cargan en el navegador al pegar el Sheet. GitHub Pages sirve solo el código genérico.

## Desarrollo

- `python3 -m http.server 8000` luego abrir `http://localhost:8000/`
