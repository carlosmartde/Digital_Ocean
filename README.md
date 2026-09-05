# DigitalOcean - Exposición interactiva

Página web interactiva en español para explicar DigitalOcean durante una exposición. Incluye:

- explorador de productos y servicios;
- despliegue de una aplicación en cinco etapas;
- recorrido visual de una petición;
- diseño adaptable para computadora, proyector y móvil.

## Ejecutar localmente

Necesitas Node.js 22 o posterior.

```bash
npm install
npm run dev
```

Abre la dirección que aparezca en la terminal.

## Generar la versión estática

```bash
npm install
npm run build
```

El sitio generado queda en `dist/client`.

## Publicar gratis en DigitalOcean

1. Sube todo el contenido de esta carpeta a un repositorio de GitHub.
2. En DigitalOcean abre **Create > App Platform**.
3. Conecta tu cuenta de GitHub y selecciona el repositorio.
4. Asegúrate de elegir **Static Site**, no **Web Service**.
5. Usa `npm run build` como comando de construcción.
6. Usa `dist/client` como directorio de salida.
7. Revisa que el resumen indique el plan **Free / USD 0** antes de desplegar.

App Platform volverá a publicar el sitio automáticamente cuando envíes cambios a la rama seleccionada.

## Estructura principal

- `app/page.tsx`: contenido e interacciones.
- `app/globals.css`: diseño responsive.
- `public/`: recursos estáticos.
- `next.config.ts`: exportación estática para DigitalOcean.

No necesita base de datos, variables de entorno ni un servidor permanente.
