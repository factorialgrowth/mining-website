# Geoandina · Tech & Mining Analytics

Sitio web corporativo estático y portafolio de soluciones en **Business Intelligence (BI)**, **Data Logging Geológico**, **Software a Medida** e **Inteligencia Artificial** aplicado al sector minero y empresarial en el Perú.

---

## Archivos del Proyecto

- `index.html`: Página principal corporativa (Hero ejecutivo, Pilares, 9 Líneas de Negocio con metodología de 5 etapas, Demo Semianimada Interactiva de perforaciones Cu-Mo, Casos de Uso, Sección de Cumplimiento Normativo en Perú / Ley N.° 29733, Preguntas Frecuentes y Contacto Directo sin formularios).
- `portal-geometalurgico.html`: Workbench geometalúrgico completo v3.1 (carga de CSV, 11 reglas QA/QC por muestra, vistas espaciales 1:1 sincronizadas, dispersión log-log Cu vs Mo, linaje del dato y exportación).
- `vercel.json`: Configuración de despliegue estático para Vercel (`cleanUrls`).

---

## Cómo editar los datos de contacto y marca

Antes de publicar en producción, abre `index.html` y edita el bloque `SITE_CONFIG` al inicio de la etiqueta `<script>` (alrededor de la línea 893):

```js
const SITE_CONFIG = {
  brandShort: 'Geoandina',
  brandFull: 'Geoandina Tech & Analytics',
  brandSub: 'SOLUCIONES TECNOLÓGICAS PARA MINERÍA · PERÚ',
  parentCompany: 'Geoandina',
  phone: '+51 999 000 000',
  phoneHref: 'tel:+51999000000',
  whatsappHref: 'https://wa.me/51999000000',
  email: 'contacto@geoandina.pe',
  emailHref: 'mailto:contacto@geoandina.pe',
  city: 'La Molina, Lima – Perú',
  address: 'Av. La Molina, La Molina 15024, Lima',
  year: '2026'
};
```

Al guardar, los cambios se reflejan automáticamente en el encabezado, Hero, tarjetas de contacto directo, modales y pie de página.

---

## Vista previa local rápida

Puedes abrir `index.html` directamente en tu navegador o levantar un servidor local desde esta carpeta:

```bash
python3 -m http.server 8080
```

Luego abre `http://localhost:8080` en tu navegador.

---

## Despliegue en GitHub + Vercel (Plan Gratuito)

1. **Crear repositorio en GitHub**:
   - Crea un nuevo repositorio en GitHub (público o privado).
   - Sube los archivos de esta carpeta:
     ```bash
     git init
     git add .
     git commit -m "Versión inicial del sitio web corporativo y demo minera"
     git branch -M main
     git remote add origin https://github.com/<tu-usuario>/<tu-repo>.git
     git push -u origin main
     ```

2. **Conectar con Vercel**:
   - Inicia sesión en [vercel.com](https://vercel.com) (puedes agregar colaboradores/administradores desde **Settings → Members** o trabajar bajo un equipo).
   - Haz clic en **Add New… → Project**.
   - Importa el repositorio de GitHub recién creado.
   - En **Framework Preset**, selecciona **Other** (sitio estático HTML sin paso de compilación) y haz clic en **Deploy**.

3. **Vincular dominio propio (opcional)**:
   - Dentro del proyecto en Vercel ve a **Settings → Domains**, agrega tu dominio y apunta los registros DNS indicados.
   - Cada `git push` futuro a `main` actualizará la página en línea automáticamente.
