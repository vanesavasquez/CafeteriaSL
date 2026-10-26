# Cafetería Loomb | Trabajo Práctico N° 1

Proyecto desarrollado en el marco de la **Diplomatura en Fullstack con Herramientas de IA** de la **Universidad Nacional de San Luis (UNSL)**.

El desarrollo se llevó a cabo aplicando una metodología de trabajo en **Modo Plan (Plan Mode / Pair Programming con Agente de IA)**: cada etapa fue planificada, analizada técnicamente, validada para evitar errores conceptuales de maquetación y documentada bajo directivas estrictas de arquitectura de software y buenas prácticas de desarrollo web.

---

## 🔗 Acceso al Proyecto
- **Archivo local:** [Abrir index.html](./index.html) *(permite abrir y explorar el código fuente en tu editor o en GitHub)*.
- **Sitio web en vivo (GitHub Pages):** [Ver demo en línea](https://vanesavasquez.github.io/CafeteriaSL/) *(disponible al activar GitHub Pages en la rama `main`)*.

---

## 📌 Enfoque Metodológico: Desarrollo en "Modo Plan"
A lo largo de este proyecto, cada requerimiento fue implementado bajo un ciclo riguroso definido en el archivo `Agents.md`:
1. **Planificación y Delimitación de Alcance:** Definición estricta de tareas sin añadir código superfluo.
2. **Corrección Conceptual y Advertencia Temprana:** Detección previa de malas prácticas (como el uso de anchos fijos en grillas, selectores con alta especificidad, etiquetas obsoletas o desbordes por márgenes negativos).
3. **Justificación Técnica de Decisiones:** Explicación comparativa de por qué cada enfoque elegido representa la mejor opción frente a las alternativas.
4. **Construcción y Verificación Iterativa:** Integración gradual con control de versiones y pruebas de respuesta responsive en múltiples dispositivos.

---

## 🚀 Plan de Implementación Integral (Recuperación Histórica)

El proyecto se estructuró y ejecutó a lo largo de las siguientes fases planificadas:

### Fase 1: Arquitectura Base, Bootstrap 5 y Reglas del Proyecto
- **Integración de Bootstrap 5.3.3:** Inclusión mediante CDN tanto de la hoja de estilos (`bootstrap.min.css`) en el `<head>` como del paquete de JavaScript (`bootstrap.bundle.min.js`) al pie del documento para habilitar componentes dinámicos.
- **Configuración de Directivas (`Agents.md`):** Establecimiento de las 6 directivas obligatorias para guiar la interacción con el asistente de IA (alcance estricto, justificaciones técnicas, detección de errores, Bootstrap 5 permanente, mejores prácticas de grilla y análisis de especificidad en CSS).

### Fase 2: Identidad Visual, Tipografías Web y Sistema de Variables CSS
- **Paleta de Colores Centralizada (`:root`):**
  - Creación de variables CSS nativas en `estilos.css`: `--rojo-vibrante`, `--blanco-base`, `--lila-pastel`, `--amarillo-tranquilo`, `--cafe-con-leche` y `--rosa-dulce`.
  - Creación de utilidades atómicas (`.bg-rojo-vibrante`, `.text-blanco-base`, etc.) con nivel de especificidad **`(0, 1, 0)`**, evitando la mala práctica de estilos en línea o el uso de `!important`.
- **Integración Tipográfica Externa:**
  - *Títulos y destacados:* **Baloo 2** (vía Adobe Typekit).
  - *Lectura y apoyo:* **Montserrat** (vía Google Fonts).
  - *Detalles y frases:* **Sniglet** (vía Google Fonts).
  - *Optimización técnica:* Detección y unificación de llamadas HTTP duplicadas y preconnects redundantes a Google Fonts para reducir el bloqueo de renderizado (*render-blocking*).

### Fase 3: Control de Versiones con Git y Despliegue en GitHub
- **Inicialización del Repositorio:** Creación del repositorio Git local aislado para el proyecto.
- **Detección y Advertencia Crítica:** Identificación de un archivo `.git` preexistente en la raíz del disco `G:\`, aislando el entorno de trabajo para evitar el rastreo accidental de archivos ajenos al proyecto.
- **Sincronización Remota:** Configuración de la rama estándar `main`, confirmación del commit inicial y vinculación con el repositorio remoto: `https://github.com/vanesavasquez/CafeteriaSL.git`.

### Fase 4: Header y Navegación Avanzada (Navbar)
- **Barra de Navegación Responsiva:**
  - Componente `<nav class="navbar navbar-expand-lg">` con botón toggler para menú colapsable en dispositivos móviles.
  - Limpieza de etiquetas obsoletas (`<font>`) inyectadas por traductores automáticos de navegador.
  - Transformación del ítem "Menú" en un **menú desplegable (*Dropdown*)** accesible con sub-opciones ("Cafés", "Pastelería", "Bebidas").
  - Reemplazo del logo genérico por el isotipo institucional `logo blanco.png`.
  - Integración de la clase `sticky-top` para fijar el menú en el scroll conservando el flujo de la página y la altura relativa sin solapamientos.

### Fase 5: Estructuración de Secciones Full-Width y Grilla Responsiva
- **Distribución de Secciones:**
  - **Inicio (`#inicio`):** Contenedor full-width con fondo rojo vibrante, textos en blanco base y grilla adaptativa (`col-12 col-md-6 col-lg-8` para contenidos y `col-12 col-md-6 col-lg-4` para la tarjeta destacada).
  - **Cursos (`#cursos`):** Contenedor full-width con fondo lila pastel y grilla de 3 columnas iguales (`col-12 col-md-4`).
  - **Contacto (`#contacto`):** Contenedor full-width con fondo amarillo tranquilo y 2 columnas (`col-12 col-md-7 col-lg-6` para el formulario y `col-12 col-md-5 col-lg-6` para información).
- **Control de Alturas con Unidades Dinámicas (`svh`):**
  - Implementación de `min-height: 10svh` para el navbar y `min-height: 90svh` para la sección Inicio, asegurando el 100% de la pantalla visible (*viewport*) en móviles sin cortes causados por las barras del navegador.
- **Extensión de Spacers en CSS Puro:**
  - Emulación de niveles extendidos del mapa Sass `$spacers`: creación de las clases de utilidad `.p-6` (`3.5rem` / 56px) y `.p-7` (`4rem` / 64px) con especificidad `(0, 1, 0)`.

### Fase 6: Sistema de Componentes (Cards, Botones y Flexbox)
- **Botones de Llamado a la Acción:** Alineación flexible mediante `d-flex flex-wrap gap-3` bajo la descripción de Inicio.
- **Card Destacada de Inicio ("Expreso 101"):** Tarjeta con imagen de cabecera, insignia badge, título, subtítulo con fecha estilizado mediante `.card-subtitle.small` y botón de reserva.
- **Cards de Cursos:**
  - Reemplazo de marcadores placeholder por imágenes reales de la carpeta `img/` (`Barismo Inicial.jpg`, `Latte art.jpg`, `Métodos de filtrado.jpg`, `expreso101.jpg`).
  - Estandarización de dimensiones mediante la clase `.img-card` (`height: 11.25rem`) y la utilidad nativa `.object-fit-cover` para evitar deformaciones de aspecto.
  - Integración de precios destacados ($45.000, $50.000 y $38.000) alineados a los extremos opuestos del botón mediante `d-flex justify-content-between align-items-center mt-3`.

### Fase 7: Formulario de Contacto Avanzado y Floating Labels
- **Maquetación con Grilla Interna:** Uso de `<form class="row g-3">` para controlar los espaciados (*gutters*) sin márgenes manuales.
- **Campos Responsivos:** Nombre y Correo configurados con `col-12 col-md-6` (apilados en móviles, en paralelo en escritorio) con validación obligatoria (`required`).
- **Grupo de Entrada Telefónico Compuesto (`.input-group`):**
  - Desplegable de código internacional (+54 Argentina, +56 Chile, +598 Uruguay, +55 Brasil).
  - Campo numérico estricto con `inputmode="numeric"`, `pattern="[0-9]+"` y sanitización en tiempo real mediante `oninput` para bloquear letras y caracteres no numéricos sin los problemas de usabilidad de `type="number"`.
- **Checkboxes en Línea:** Selección múltiple de cursos de interés (`.form-check-inline`).
- **Área de Texto Abierta:** Campo para mensajes (`<textarea>`) con altura controlada desde CSS (`.textarea-contacto`).
- **Etiquetas Flotantes (`.form-floating`):**
  - Implementación respetando la sintaxis estricta de Bootstrap 5 (el control va antes del `<label>` y con atributo `placeholder` obligatorio).

### Fase 8: Pie de Página (Footer) y Modal de Confirmación
- **Footer Semántico:** Estructurado en dos columnas (`col-12 col-md-6`) con información legal y enlaces a redes sociales (WhatsApp, Facebook, Instagram) protegidos con `rel="noopener noreferrer"`.
- **Modal de Confirmación Interactivo:**
  - Componente modal centrado (`modal-dialog-centered`) con transición suave (`fade`).
  - Lógica JavaScript vinculada al evento `submit`: valida la integridad de los datos (`checkValidity()`), previene la recarga de página (`event.preventDefault()`), despliega el modal y resetea el formulario de forma limpia.

---

## 🛠️ Tecnologías y Herramientas Utilizadas
- **HTML5:** Marcado semántico, accesible y estructurado.
- **CSS3:** Variables nativas (`:root`), flexbox, selectores de baja especificidad y tipografías web.
- **Bootstrap 5.3.3:**
  - Sistema de grillas responsivo de 12 columnas (*Mobile-First*).
  - Componentes: Navbar, Dropdowns, Cards, Badges, Input Groups, Floating Labels, Modals.
  - Utilidades: Flexbox (`d-flex`, `justify-content-*`, `align-items-*`), espaciados (`g-*`, `p-*`, `m-*`), tipografía y colores.
- **JavaScript (ES6):** Control de eventos de formulario y manipulación de la API de Bootstrap Modal.
- **Git & GitHub:** Control de versiones distribuido.

---

## 📁 Estructura del Repositorio
```
├── img/                               # Fotografías de cursos y productos
│   ├── Barismo Inicial.jpg
│   ├── expreso101.jpg
│   ├── Latte art.jpg
│   └── Métodos de filtrado.jpg
├── logo blanco.png                    # Isotipo de la marca
├── index.html                         # Maquetación y estructura principal
├── estilos.css                        # Variables de color, fuentes y extensiones CSS
├── README.md                          # Documentación del proyecto y plan de trabajo
└── Agents.md                          # Directivas y reglas técnicas de desarrollo
```

---

## 👩‍💻 Autora
- **Estudiante:** Vanesa Ledesma
- **Carrera/Programa:** Diplomatura en Fullstack con Herramientas de IA
- **Institución:** Universidad Nacional de San Luis (UNSL)
- **Repositorio:** [github.com/vanesavasquez/CafeteriaSL](https://github.com/vanesavasquez/CafeteriaSL)
