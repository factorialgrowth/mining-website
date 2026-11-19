# DMDStack (`DMDStack.com`)

Sitio web corporativo estático y portafolio de soluciones de **DMDStack** en **Desarrollo de Software a Medida**, **Business Intelligence (BI)**, **Data Logging Geológico** e **Inteligencia Artificial** en Perú.

---

## Archivos del Proyecto

- `index.html`: Página principal corporativa con estética moderna Blanco & Azul Cobalto (Hero ejecutivo, Pilares, 9 Líneas de Negocio con metodología de 5 etapas, Demo Semianimada Interactiva de perforaciones Cu-Mo con datos 100% sintéticos, Casos de Uso, Sección de Cumplimiento Normativo en Perú / Ley N.° 29733, Preguntas Frecuentes y Contacto Directo sin formularios).
- `vercel.json`: Configuración de despliegue estático para Vercel (`cleanUrls`).

---

## Configuración de Datos (`SITE_CONFIG`)

En `index.html`, el bloque `SITE_CONFIG` centraliza los datos de marca y contacto:

```js
const SITE_CONFIG = {
  brandShort: 'DMDStack',
  brandFull: 'DMDStack',
  brandSub: 'DESARROLLAMOS SOFTWARE PARA HACER CRECER TU NEGOCIO',
  contactName: 'David Mamani',
  contactRole: 'Gerente General · DMDStack',
  phone: '+51 997 050 382',
  phoneHref: 'tel:+51997050382',
  whatsappHref: 'https://wa.me/51997050382',
  email: 'pdangel98@gmail.com',
  emailHref: 'mailto:pdangel98@gmail.com',
  city: 'La Molina - Lima - Perú',
  domain: 'DMDStack.com',
  year: '2026'
};
```

Al guardar, los cambios se reflejan automáticamente en el encabezado, Hero, tarjetas de contacto directo, modales y pie de página.

---

## Vista previa local rápida

```bash
python3 -m http.server 8080
```

Luego abre `http://localhost:8080` en tu navegador.

---

## Despliegue en GitHub + Vercel

- Repositorio: `factorialgrowth/mining-website` (rama `main`).
- Cada push a `main` actualiza automáticamente el sitio en producción en Vercel.
- Para vincular el dominio propio `DMDStack.com`, agrégalo desde **Project Settings → Domains** en el panel de Vercel y configura los registros DNS indicados.
