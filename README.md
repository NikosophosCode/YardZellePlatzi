# Yard Sale (Práctica Curso Frontend Developer Platzi)

Proyecto estático (HTML + CSS) que replica la interfaz base de una tienda de productos de segunda mano. Forma parte de la práctica del curso de Frontend Developer de Platzi y sirve como base para incorporar posteriormente JavaScript (estado, carrito, consumo de APIs, autenticación, etc.).

## 📂 Estructura del Proyecto

```
.
├── index.html
├── login.html
├── create-account.html
├── edit-account.html
├── recovery.html
├── enviado.html
├── CSS/
│   ├── styles.css
│   └── desktop.css
├── assets/
│   ├── icons/
│   └── logos/
└── package.json
```

Archivos principales:
- Página principal catálogo: [index.html](index.html)
- Login: [login.html](login.html)
- Crear cuenta: [create-account.html](create-account.html)
- Editar cuenta (vista estática): [edit-account.html](edit-account.html)
- Recuperar contraseña (form reset): [recovery.html](recovery.html)
- Confirmación de envío email: [enviado.html](enviado.html)
- Estilos base mobile-first: [CSS/styles.css](CSS/styles.css)
- Estilos desktop (media query ≥1024px): [CSS/desktop.css](CSS/desktop.css)
- Configuración Live Server (puerto): [.vscode/settings.json](.vscode/settings.json)
- Metadata npm (no se usa aún para build): [package.json](package.json)

## 🎨 Diseño y UX

- Tipografía: Quicksand (Google Fonts).
- Sistema de colores centralizado mediante variables CSS (paleta neutros + verde marca).
- Enfoque mobile-first: `styles.css` define base móvil y `desktop.css` ajusta layout en pantallas grandes.
- Componentes reutilizables: botones primarios / secundarios, grid de productos, pills de categorías.
- Semántica y accesibilidad mejoradas en [index.html](index.html): roles (`role="menubar"`, `aria-label`, `aria-labelledby`), clase `sr-only`.

## 🧩 Características Implementadas

- Barra de navegación responsiva (menú simplificado en móviles).
- Grid de productos con tarjetas estáticas.
- Estados de botón de carrito (añadido vs no añadido) con clases (`.added`).
- Formularios básicos: login, creación de cuenta, recuperación y actualización (estáticos).
- Estilos adaptativos mediante `clamp()` y `aspect-ratio`.
- Iconografía SVG/PNG localizada en `/assets/icons`.

## 🚀 Cómo Ejecutar

Opción 1 (rápido):
- Abrir directamente `index.html` en el navegador.

Opción 2 (recomendada con Live Server en VS Code):
1. Abrir carpeta del proyecto en VS Code.
2. Extensión Live Server instalada.
3. Click derecho sobre `index.html` → "Open with Live Server".
4. Se servirá en `http://localhost:5501` (configurado en [.vscode/settings.json](.vscode/settings.json)).

## 📱 Responsividad

Breakpoints clave:
- Base móvil <= 960px (oculta menú principal y pills activas).
- ≥ 960px: muestra menú completo y oculta `category-pills`.
- Ajustes adicionales <= 560px para densidad de la grilla.

## ♿ Accesibilidad

Implementado:
- Texto oculto accesible (`.sr-only`).
- Etiquetas y `aria-label` descriptivos.
- Botones con propósitos claros.
Pendiente:
- Estados de foco visibles en todas las páginas (actualmente solo en `index.html` inline).
- Navegación por teclado validada en formularios.

## 🛠 Tecnologías

- HTML5 semántico
- CSS3 (flexbox, grid, variables, aspect-ratio, media queries)
- Sin JS todavía (ideal para siguiente iteración)

## 🔧 Próximas Mejoras Sugeridas

| Categoría | Mejora |
|-----------|--------|
| Accesibilidad | Añadir `landmark roles` en todas las páginas secundarias |
| Componentización | Extraer estilos inline de páginas a un `CSS/components.css` |
| Performance | Optimizar imágenes locales y añadir `preload` de fuentes |
| Interactividad | Implementar filtrado real, búsqueda y estado del carrito con JS |
| Build | Añadir tooling (Vite o Parcel) si se escala a SPA |
| Form UX | Validaciones visuales y mensajes de error accesibles |
| Diseño | Añadir modal de carrito y menú móvil desplegable |

## 🗂 Convenciones

- Nombres de clases en inglés (consistencia).
- BEM podría adoptarse si escala la complejidad (aún no necesario).
- Variables CSS centralizadas (evitar "magic numbers" repetidos).

## 🧪 Testing (Futuro)

Ideas:
- Pruebas de accesibilidad con Lighthouse / axe.
- Validación HTML (`npm create @html-validate` en futuro).
- Visual regression (Percy / Chromatic si se migra a componentes).

## 📄 Licencia

Proyecto educativo. Añade una licencia (ej. MIT) si lo publicas.

## 🙌 Créditos

- Curso Frontend Developer (Platzi).
- Imágenes temporales: Pexels (usadas como placeholders).

## 💡 Siguientes Pasos para mejorar

1. Centralizar estilos de navegación reutilizable.
2. Extraer estilos inline de `index.html` y `recovery.html` a archivo dedicado.
3. Añadir `script.js` para:
   - Toggle menú móvil.
   - Añadir/Quitar del carrito (cambiar icono dinámico).
   - Filtrar productos.
4. Simular datos desde un JSON local (mock API).
5. Preparar migración a framework (React / Vue) si se requiere escalabilidad.
