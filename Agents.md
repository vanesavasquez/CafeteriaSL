# Instrucciones de Trabajo y Reglas del Proyecto

Este documento establece las directivas y pautas obligatorias que el asistente de IA debe seguir en todo momento durante el desarrollo de este proyecto.

---

## 1. Alcance Estricto de los Cambios
- **Aplica únicamente lo solicitado**: No agregues código, librerías, scripts, componentes o funcionalidades adicionales que no hayan sido expresamente pedidos por el usuario.

## 2. Justificación Técnica de Sugerencias
- Siempre que sugieras una forma particular de implementación, explica con claridad **por qué es la mejor opción técnica** frente a otras alternativas.

## 3. Corrección de Conceptos y Advertencia Temprana de Errores
- Si una instrucción dada por el usuario no es técnicamente correcta o si el concepto que se busca implementar presenta errores conceptuales:
  - Señálalo de inmediato y con claridad.
  - Explica cómo debería abordarse correctamente.
  - Detalla qué errores, bugs o efectos indeseados provocaría aplicar la idea errónea.

## 4. Uso Exclusivo de Bootstrap 5
- En este proyecto se utiliza **Bootstrap 5** de forma estándar y permanente para maquetación, componentes y utilidades. No utilices versiones anteriores ni otras librerías incompatibles salvo indicación expresa.

## 5. Mejores Prácticas en Grillas y Tamaños de Columnas
- Cada vez que se definan o ajusten tamaños de grilla:
  - Explica siempre las **mejores prácticas** de diseño responsivo de Bootstrap 5 (`container`, `row`, `col-*`, breakpoints `xs`, `sm`, `md`, `lg`, `xl`, `xxl`).
  - Explica por qué se elige esa distribución y **qué problemas o desbordes causaría** hacerlo de forma incorrecta (por ejemplo: anchos fijos en px, omisión del contenedor o fila, columnas que sumen más de 12 sin intención, etc.).

## 6. Personalización y Gestión de Colores en Bootstrap 5
- Cada vez que se toque o modifique un color:
  - Explica cómo se debe editar correctamente en Bootstrap 5 (uso de clases de utilidad, variables CSS nativas de Bootstrap `--bs-*` o CSS personalizado en `estilos.css`).
  - Menciona por qué ese método es el recomendado frente a malas prácticas (como el uso abusivo de `!important` o sobrescrituras indiscriminadas).
  - Analiza en el CSS qué nivel de **especificidad** se logra con la sentencia utilizada, cuál podría ser una mejor alternativa y el por qué técnico (evitar guerras de especificidad, mantener bajo acoplamiento y facilitar el mantenimiento).
  - Advierte qué problemas de mantenimiento, inconsistencia visual o herencia de estilos pueden generarse si no se hace de la forma adecuada.

