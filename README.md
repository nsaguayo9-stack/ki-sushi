# Ki Sushi

Carta web con carrito y pedido por WhatsApp, preparada para Vercel.

## Desarrollo

```bash
npm install
npm run dev
```

## Publicación

Subir este directorio a un repositorio GitHub e importar ese repositorio en Vercel. Vercel detecta Vite; comando de compilación `npm run build` y directorio de salida `dist`.

El catálogo se consulta desde la URL pública de Google Sheets definida como `CSV_URL` en `src/main.js` cada vez que se abre la página o vuelve al primer plano. La copia `public/catalogo-respaldo.csv` se muestra solo si el Sheet no responde. Al actualizar productos, precios, stock o URLs de fotos en Sheets no hace falta reconstruir el proyecto; puede haber un breve retraso de publicación de Google.

Columnas esperadas: `id`, `categoría`, `nombre`, `descripción`, `opciones/tamaños`, `precio`, `stock`, `foto`. `stock=no` bloquea compras. `foto` acepta URL pública HTTPS; si está vacía o la imagen falla, se usa la tarjeta de texto.

El número de WhatsApp está en la constante `WHATSAPP`. La imagen de portada es referencial, creada para el diseño; el logo no incluye una ciudad. Comprobar la oferta y los precios vigentes con el negocio antes de publicar.
