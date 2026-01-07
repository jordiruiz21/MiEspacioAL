<div align="center">

  <h1>📚 Aula Virtual / Blog de Materiales</h1>
  
  <p>
    Una plataforma educativa rápida, estética y fácil de gestionar.
    <br />
    Construida con <strong>Astro</strong> y gestionada con <strong>Decap CMS</strong>.
  </p>

  <img src="https://via.placeholder.com/800x400?text=Captura+de+la+Web" alt="Vista previa del proyecto" width="100%" style="border-radius: 10px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

  <br />
  <br />

  ![Astro](https://img.shields.io/badge/Astro-BC52EE?style=for-the-badge&logo=astro&logoColor=white)
  ![Decap CMS](https://img.shields.io/badge/Decap%20CMS-3A2F3D?style=for-the-badge&logo=netlify&logoColor=white)
  ![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)
  ![Status](https://img.shields.io/badge/Status-Terminado-success?style=for-the-badge)

</div>

<hr />

## 🧐 ¿Qué es este proyecto?

Este proyecto es un sitio web diseñado para que un profesor pueda subir **material didáctico (PDFs, imágenes)** y compartir noticias con sus alumnos sin necesidad de saber programar. 

La web simula un **cuaderno escolar** con detalles visuales como cintas adhesivas ("Washi Tape"), tipografías amables y animaciones suaves.

## ✨ Características Principales

- **⚡ Rendimiento Extremo:** Carga instantánea gracias a Astro (HTML estático).
- **📝 Gestión Fácil (CMS):** Panel de administración visual (Decap CMS) para crear posts y subir archivos arrastrando y soltando.
- **🔐 Acceso Seguro:** Panel de administración protegido con Netlify Identity.
- **📂 Sistema de Archivos:**
  - Soporte para múltiples adjuntos por entrada.
  - **Botón "Descargar Todo":** Script inteligente que descarga todos los materiales de una lección secuencialmente.
- **🎨 Diseño Único:**
  - Efecto "Washi Tape" CSS puro.
  - Animaciones de entrada (Fade In).
  - Diseño Responsive (Móvil/Tablet/PC).

## 🛠️ Tecnologías Utilizadas

* **Frontend:** [Astro](https://astro.build/) (v5)
* **CMS:** [Decap CMS](https://decapcms.org/) (anteriormente Netlify CMS)
* **Estilos:** CSS3 Moderno (Variables, Grid, Flexbox, Animations)
* **Despliegue:** [Netlify](https://netlify.com/)
* **Autenticación:** Netlify Identity

## 🚀 Instalación y Uso Local

Si quieres clonar este proyecto y probarlo en tu ordenador:

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/TU_USUARIO/NOMBRE_DEL_REPO.git](https://github.com/TU_USUARIO/NOMBRE_DEL_REPO.git)
    cd NOMBRE_DEL_REPO
    ```

2.  **Instala las dependencias:**
    ```bash
    npm install
    ```

3.  **Configura el CMS en modo local:**
    Abre `public/admin/config.yml` y descomenta la línea:
    ```yaml
    local_backend: true
    ```

4.  **Inicia el servidor de desarrollo:**
    ```bash
    npm run dev
    ```
    Y en otra terminal, inicia el proxy del CMS:
    ```bash
    npx decap-server
    ```

5.  ¡Listo! Abre `http://localhost:4321` para ver la web y `http://localhost:4321/admin` para el panel.

## 📦 Despliegue en Producción

Este proyecto está preconfigurado para **Netlify**.

1.  Sube el código a GitHub.
2.  Importa el proyecto en Netlify.
3.  Activa **Identity** y **Git Gateway** en la configuración del sitio.
4.  **Importante:** Asegúrate de que en `config.yml` la línea `local_backend: true` esté **comentada** o borrada.

## 📂 Estructura del Proyecto

```text
/
├── public/
│   ├── admin/       # Configuración del CMS (config.yml)
│   └── uploads/     # Aquí se guardan las fotos y PDFs subidos
├── src/
│   ├── components/  # Header, Footer, BaseHead
│   ├── content/     # Esquemas de datos (config.ts) y Posts (.md)
│   ├── layouts/     # Plantilla del Blog (BlogPost.astro)
│   └── pages/       # Página principal (index.astro)
└── astro.config.mjs
