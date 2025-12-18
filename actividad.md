# Workshop: Construcción de una "Dashboard de Cripto-Gaming" 🚀


**Tecnologías:** HTML5, Bootstrap 4, Sass (Sintaxis `@use`).

---

## 🎯 Objetivo
Construir la interfaz de una plataforma de gestión de activos digitales. No debe parecer un sitio hecho con Bootstrap estándar; debe tener una identidad visual propia (Dark Mode, colores neón y componentes personalizados) utilizando la potencia de Sass.

---

## 🛠️ Requisitos Técnicos
1. **Arquitectura Sass:** No usar `@import`. Debes utilizar `@use` para cargar los módulos de Bootstrap.
2. **Estructura de Carpetas:**
   - `/scss`
     - `main.scss` (archivo raíz)
     - `_variables.scss` (configuración de overrides)
     - `_components.scss` (estilos propios)
   - `index.html`

---

## 📝 Instrucciones del Desafío

### Fase 1: Configuración de Marca 
Antes de generar el CSS, debes configurar el "corazón" de tu diseño en Sass:
- **Colores:** Cambia el color `$primary` por un tono neón (ej. Morado eléctrico o Verde Matrix).
- **Tipografía:** Importa una fuente de Google Fonts (recomendado: *Orbitron* o *Roboto*) y asígnala como la fuente base.
- **Identidad:** Deshabilita los bordes redondeados en todo el sitio (`$enable-rounded: false`).
- **Sombras:** Activa las sombras globales de Bootstrap.

### Fase 2: Layout y Navegación 
Crea la estructura base en `index.html`:
- **Navbar:** Una barra de navegación "Sticky" que use el esquema de color oscuro.
- **Sidebar:** Crea un menú lateral responsivo usando la grilla de Bootstrap que se oculte en móviles.
- **Contenedor:** Usa un contenedor fluido para el área de contenido principal.

### Fase 3: Componentes Dinámicos (JS) 
Implementa elementos que requieran las funciones de JavaScript de Bootstrap, pero personaliza su estilo con Sass:
- **Modales:** Crea un botón "Comprar Token" que abra un Modal. El encabezado del modal debe tener un color degradado generado con la función `color.scale` de Sass.
- **Tooltips:** Agrega tooltips a los iconos de navegación lateral.
- **Alertas:** Configura una alerta que sea "dismissible" (que se pueda cerrar) para mostrar mensajes del sistema.

### Fase 4: Personalización con Sass Avanzado 
Añade el toque profesional "No-Bootstrap":
- **Efecto Glassmorphism:** Crea una clase `.glass-card` que use `rgba()` y `backdrop-filter` para aplicarla a las tarjetas de estadísticas.
- **Estado Hover:** Crea un mixin para que los botones tengan un brillo (box-shadow) de su propio color al pasar el mouse.
- **Utilidad Nueva:** Crea un bucle `@each` en Sass que genere clases de utilidad para bordes brillantes de diferentes colores (ej. `.border-glow-primary`, `.border-glow-danger`).

---

## 📋 Entregables Esperados

1. **Dashboard Funcional:** El sitio debe ser totalmente responsivo.
2. **Lógica de Colores:** Si cambio el valor de `$primary` en mi archivo de variables, el modal, los botones y las sombras deben actualizarse automáticamente.
3. **Uso de Namespace:** En el archivo `main.scss`, el acceso a las variables de Bootstrap debe hacerse mediante el namespace definido (ej. `bootstrap.$variable`).

---

## 💡 Tips
- Recuerda que para usar `@use` con configuración, debes hacerlo así: `@use "../bootstrap/scss/bootstrap" with ( $variable: valor );`.
- No toques la carpeta de `bootstrap` o los archivos fuente de Bootstrap; todo se sobreescribe desde tus propios archivos `.scss`.
- Si el JS de Bootstrap no funciona, asegúrate de haber incluido **jQuery** y **Popper.js** antes del script de Bootstrap en el HTML.

---

## 🔥 Reto Extra (Si terminas antes)
Crea un **Switch de modo oscuro/claro**. Al añadir una clase `.light-mode` al `body`, los colores deben invertirse utilizando funciones de manipulación de color de Sass (`invert()`, `lighten()`, o `darken()`).