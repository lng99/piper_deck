# Guía de Uso y Modificación - Piper Deck Landing Page

Este documento explica cómo está construido el sitio web de **Piper Deck** y cómo utilizar el panel de administración (CMS) para modificar sus contenidos sin necesidad de tocar el código fuente.

---

## 1. Estructura del Proyecto

El sitio web está desarrollado utilizando tecnologías web estándar (HTML, CSS, y JavaScript) sin frameworks pesados para garantizar máxima velocidad y personalización. Todo el contenido dinámico es gestionado mediante **Netlify CMS** (ahora conocido como Decap CMS).

Archivos y carpetas principales:
- `index.html`: Es la estructura principal y el contenido base de la página.
- `styles.css`: Contiene todos los estilos visuales (colores, fuentes, animaciones y diseño responsivo).
- `script.js`: Maneja la interactividad de la página: carruseles, el modal de detalle de cabañas, el visor de fotos (lightbox) y el envío a WhatsApp.
- `content/site.json`: Es el archivo de base de datos donde se guardan los textos, enlaces y rutas a imágenes que se configuran desde el CMS.
- `admin/config.yml`: Es el archivo que le dice al panel de administración del CMS qué campos mostrarte para que puedas editarlos.
- `assets/`: Carpeta donde se guardan las imágenes, logos y fotos subidas.

---

## 2. Cómo modificar el sitio usando Netlify CMS

No necesitas saber programación para cambiar los textos, fotos o agregar nuevas cabañas. Puedes hacerlo desde un panel de control intuitivo.

### Acceso al Panel
1. En la barra de direcciones de tu navegador, ingresa al dominio de tu sitio y agrégale `/admin` al final. Por ejemplo: `www.tudominio.com/admin`
2. Si es la primera vez, el sistema te pedirá iniciar sesión.
3. Una vez dentro, verás el panel de control de Netlify CMS.

### Modificar Contenidos
En la barra lateral izquierda, verás una sección llamada **"Contenido de la landing"** -> **"Página principal"**. Al hacer clic allí, verás todos los bloques de la página web organizados de la siguiente manera:

- **Marca**: Para cambiar el nombre, subtítulo o logo principal.
- **Portada (Hero)**: Controla la foto principal gigante que se ve al entrar, junto con su título y textos de bienvenida.
- **Datos rápidos**: Los 3 números destacados que aparecen bajo la portada (ej. años de oficio).
- **Quiénes somos**: Tu texto de presentación, imagen y viñetas descriptivas.
- **Servicios**: Los cuatro bloques de servicios.
- **Contacto**: Todos tus datos de contacto (WhatsApp, Email, Dirección, Facebook) y los textos del formulario.
- **Pie de página**: Los textos del final de la página.

### Administrar la Galería de Cabañas (Modal)
Esta es la sección más potente. En el bloque de **"Galería"**, dentro de la pestaña **"Fotos"**, puedes agregar, quitar o editar cada cabaña mostrada en el carrusel de trabajos realizados.

Al editar una cabaña, tendrás los siguientes campos:
1. **Imagen principal (exterior)**: La foto que aparece en el carrusel principal.
2. **Nombre y Descripción visible**: El texto cortito que sale abajo en el carrusel.
3. **Nombre y Descripción detallada**: El título grande y el texto largo que aparece **cuando se abre la ventana modal**.
4. **Datos clave**: Aquí puedes agregar características específicas como "Superficie: 45m²", "Dormitorios: 2", etc.
5. **Fotos exteriores**: Si agregas fotos aquí, la imagen principal del modal se convertirá en un **carrusel** donde los usuarios pueden ver varios ángulos del exterior de la casa.
6. **Fotos del interior**: Puedes subir múltiples fotos. Aparecerán debajo de los datos clave en el modal como una galería de miniaturas.
7. **Fotos del proceso de construcción**: Al igual que el interior, formarán una galería en el modal.

> **Importante:** Las secciones de fotos (interior, construcción, o extras exteriores) **sólo aparecerán en el sitio web si les subes imágenes**. Si dejas una vacía, la página es lo suficientemente inteligente para ocultar esa sección y mantener el diseño limpio.

---

## 3. Notas Finales

- Cuando termines de realizar cualquier cambio en el CMS, asegúrate de presionar el botón **"Guardar" / "Publicar"** en la parte superior.
- Al publicar, Netlify se encargará de reconstruir el sitio web de forma automática. Este proceso suele tomar unos minutos. Actualiza tu página web pública después de unos momentos para ver los cambios reflejados.
- Si subes muchas fotos, el sistema se encargará de acomodarlas en el visor de imágenes (lightbox) de manera automática. Todas las fotos en el modal se pueden hacer clic para ver a pantalla completa y usar flechas para navegar.

---

## 4. Sobre el Dominio y Hosting

Actualmente, el sitio web está alojado gratuitamente y utiliza un subdominio provisto por **Netlify** (por ejemplo: `tusitio.netlify.app`). 

Si en algún momento deseas utilizar un **dominio propio y personalizado** (por ejemplo, `www.piperdeck.com.ar` o `www.pipercabanas.com`), ten en cuenta lo siguiente:
- Deberás adquirir (comprar) el nombre de dominio a través de un proveedor registrador (como Nic.ar para dominios de Argentina, o proveedores internacionales como Namecheap, GoDaddy, etc.). Los dominios suelen pagarse de forma **anual**.
- Una vez adquirido el dominio propio, se puede configurar dentro de Netlify para que tu página web cargue con tu dirección web oficial.
