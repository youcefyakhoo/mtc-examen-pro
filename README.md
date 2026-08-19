
## MTC Examen Pro — entrega

Esta aplicación es un frontend React estático con 954 preguntas oficiales organizadas por licencia. El progreso se guarda localmente en el navegador mediante `localStorage`; no requiere backend ni base de datos.

### Ejecutar localmente

```bash
pnpm install
pnpm dev
```

### Verificar y compilar

```bash
pnpm check
pnpm build
```

El build genera los archivos estáticos en `dist/public`. Para Cloudflare Pages configura el comando de build `pnpm run build:pages` y el directorio de salida `dist/public`; desde la terminal usa `pnpm run deploy:pages` o `pnpm exec wrangler pages deploy dist/public --project-name simelacromtc`. Para el flujo alternativo de Workers Static Assets usa `pnpm build` y `pnpm exec wrangler deploy`; `wrangler.jsonc` ya apunta a `dist/public` y configura `not_found_handling: single-page-application`. No mezcles ambos flujos. Antes de publicar, completa los datos legales del titular, sustituye el dominio del sitemap y configura tu Publisher ID de AdSense/CMP.

### Nota sobre el contenido

Las preguntas provienen de los balotarios oficiales proporcionados para este proyecto. Las explicaciones añadidas para preguntas que no traían explicación en el PDF muestran la alternativa oficial correcta; conviene revisarlas con el reglamento vigente antes de publicar.
