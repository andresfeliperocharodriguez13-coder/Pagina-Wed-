URL:spectacular-lamington-c70867.netlify.app/﻿
📦 Catálogo Web con Modales Interactivos (CSS-Only)
Un catálogo de productos moderno, limpio y altamente eficiente diseñado para dispositivos móviles y de escritorio. El aspecto más destacado de este proyecto es que cuenta con modales interactivos (ventanas emergentes) funcionales sin utilizar una sola línea de JavaScript, logrando la interacción puramente a través de la técnica de Checkbox Hack en HTML5 y CSS3.

✨ Características Destacadas
🚫 Zero JavaScript: Apertura y cierre de modales dinámicos utilizando únicamente <input type="checkbox"> y selectores CSS (:checked y +).

📱 Enfoque Mobile-First: Diseñado a la perfección para pantallas móviles con un contenedor centralizado y adaptable de máximo 500px.

🎨 Interfaz Atractiva e Intuitiva:

Tarjetas de producto ordenadas y compactas.

Formulario de contacto integrado con un esquema cálido de color amarillo/ámbar.

Efectos suaves de transición (transition: transform/opacity) en tarjetas y modales.

📐 Diseño Modular: Código semántico fácil de escalar para agregar más productos o campos de manera sencilla.

🛠️ Tecnologías Utilizadas
HTML5 — Marcado estructurado, semántico y accesible utilizando etiquetas como <article>, <main> y <section>.

CSS3 — Grid, Flexbox, selectores avanzados de combinación, transiciones y variables de diseño responsivo.

⚙️ ¿Cómo funciona la interacción CSS-Only?
La magia detrás de los modales detallados de este catálogo radica en el uso de los elementos <input type="checkbox"> combinados con sus etiquetas asociadas <label>.

Cada botón "Detalle" y "Cerrar" es en realidad un <label> vinculado al id de un checkbox oculto (display: none;).

Al hacer clic en el label, el checkbox cambia de estado a :checked.

El selector CSS adyacente detecta este cambio y altera la visibilidad del modal de forma instantánea:

CSS
/* Cuando el checkbox está activo, muestra su overlay correspondiente */
.modal-checkbox:checked + .modal-overlay {
  opacity: 1;
  pointer-events: auto; 
}

/* Escala suavemente el contenido del modal para darle un efecto premium */
.modal-checkbox:checked + .modal-overlay .modal-content {
  transform: scale(1);
}
📂 Estructura de Archivos
Bash
├── index.html       # Estructura del catálogo, formulario y ventanas modales
├── styles.css       # Estilos visuales, animaciones y control de estados CSS
└── README.md        # Documentación del proyecto
🚀 Cómo Visualizar el Proyecto
No requieres de compiladores ni servidores backend para ver este catálogo en acción:

Clona o descarga este repositorio:

Bash
git clone https://github.com/tu-usuario/tu-repositorio.git
Abre el archivo principal:
Haz doble clic sobre index.html para abrirlo directamente en tu navegador web (Chrome, Edge, Firefox, Safari, etc.).

🎨 Personalización
Puedes modificar fácilmente el comportamiento y la estética editando el archivo styles.css. Por ejemplo:

Si deseas cambiar la velocidad de apertura del modal, edita los valores de transition: opacity 0.3s ease; y transform 0.3s ease;.

Puedes cambiar el ancho máximo de la aplicación modificando el .container { max-width: 500px; } a tu gusto si buscas un diseño para pantallas ultra anchas.
