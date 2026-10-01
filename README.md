# Proyecto colaborativo - Fundamentos WEB

**Grupo:** 4303D | **Institución:** UNICAMACHO | **Programa:** Ingeniería en Sistemas

## Integrantes

- Aslyn Zambrano
- Stiven Delgado

## Temas seleccionados

1. Tema 1: Realidad virtual y aumentada
2. Tema 2: Ciudades inteligentes

## Descripción del proyecto

Mini sitio web de dos páginas sobre temas tecnológicos actuales, con navegación entre páginas, imágenes, listas, tablas y fuentes consultadas. Se desarrolló de forma colaborativa en un único repositorio de GitHub. En esta etapa se agregó una hoja de estilos externa (CSS) compartida por ambas páginas, sin JavaScript ni frameworks CSS.

## Estructura del repositorio

```
fundamentos-web-equipo/
│-- realidad-virtual-aumentada.html
│-- tema2.html
│-- README.md
│-- css/
│   `-- styles.css
`-- img/
```

## Distribución del trabajo

| Integrante | Responsabilidad |
| --- | --- |
| Aslyn Zambrano | Tema 1 (`realidad-virtual-aumentada.html`) y estilos de su página |
| Stiven Delgado | Tema 2 (`tema2.html`) y estilos de su página |

## Convención CSS

- **Idioma de las clases:** inglés.
- **Formato:** minúsculas con palabras separadas por guion medio (kebab-case).
- **Componentes:** metodología BEM cuando aplica (`bloque__elemento--modificador`).
- **Hoja de estilos:** un único archivo `css/styles.css`, compartido por las dos páginas.
- **Estructura:** se conservan las etiquetas semánticas (`header`, `nav`, `main`, `section`, `footer`) y se agregan clases solo cuando se necesita un identificador estable.
- **Sin estilos en línea:** no se usa el atributo `style` en el código final.

| Clase | Uso |
| --- | --- |
| `.site-header` | Encabezado de cada página |
| `.site-header__title` | Título principal (h1) |
| `.site-header__intro` | Párrafo introductorio |
| `.main-nav` | Navegación entre páginas |
| `.site-main` | Contenedor del contenido principal |
| `.topic-section` | Cada sección temática |
| `.site-footer` | Pie de página |

## Paleta de color

| Variable | Código | Uso |
| --- | --- | --- |
| `--color-primary` | `#2d2a6e` | Encabezado, pie de página, títulos y cabecera de tabla |
| `--color-secondary` | `#4338ca` | Enlaces y degradado del encabezado |
| `--color-accent` | `#0f766e` | Bordes de detalle y foco del teclado |
| `--color-bg` | `#f1f2fa` | Fondo general |
| `--color-surface` | `#ffffff` | Fondo de secciones |
| `--color-text` | `#1f2937` | Texto principal |

**Justificación:** La paleta parte de un índigo profundo, apropiado para temas tecnológicos como la realidad virtual y aumentada, y combina bien con el teal, que aporta la idea de conectividad y ciudad inteligente. Los fondos son neutros y claros para favorecer la lectura. El color de acento se usa con moderación para no competir con el contenido.

**Contraste (referencia mínima WCAG 2.2 AA, 4.5:1 para texto normal):**

| Combinación | Contraste aproximado |
| --- | --- |
| Texto principal sobre blanco | 14.7:1 |
| Blanco sobre `--color-primary` | 12.6:1 |
| Enlaces (`--color-secondary`) sobre blanco | 7.9:1 |
| Teal (`--color-accent`) sobre blanco | 5.5:1 |

> Verificado con: _(escribir aquí la herramienta usada, por ejemplo WebAIM Contrast Checker)_

**Accesibilidad:** los enlaces de navegación cambian con subrayado además del color en hover y foco. El foco del teclado tiene un contorno visible. Se respeta la preferencia de reducir movimiento (`prefers-reduced-motion`).

## Prueba de cascada

Se aplicaron las siguientes reglas al mismo elemento:

```html
<h2 id="demo-title" class="demo-title">Prueba de cascada</h2>
```

```css
h2 { color: blue; }
.demo-title { color: green; }
#demo-title { color: purple; }
```

| Etapa | Regla aplicada | Color observado | Explicación |
| --- | --- | --- | --- |
| 1 | Selector de elemento `h2` | Azul | Única regla que afecta al elemento. |
| 2 | Se agrega la clase `.demo-title` | Verde | Una clase tiene mayor especificidad que un selector de elemento. |
| 3 | Se agrega el ID `#demo-title` | Morado | Un ID tiene mayor especificidad que una clase. |
| 4 | Se agrega `style="color: orange"` | Naranja | El estilo en línea prevalece sobre las reglas normales de la hoja de estilo. |

**Conclusión:** la cascada resuelve los conflictos según el origen, la especificidad y el orden de aparición. La especificidad va de menor a mayor así: elemento, clase, ID y estilo en línea. Si hay empate, gana la regla que aparece después. Por mantenibilidad, el código final usa solo clases; la prueba fue retirada y no queda ningún estilo en línea ni selector de ID de demostración.

## Revisión cruzada

- Aslyn revisó la página de Stiven: _(qué error encontró y qué mejora propuso)_.
- Stiven revisó la página de Aslyn: _(qué error encontró y qué mejora propuso)_.

## Validación

### Página 1: Realidad virtual y aumentada

Errores encontrados:

- _(completar con los resultados del validador HTML del W3C)_

Correcciones realizadas:

- _(completar)_

### Página 2: Ciudades inteligentes

Errores encontrados:

- _(completar con los resultados del validador HTML del W3C)_

Correcciones realizadas:

- _(completar)_

### Hoja de estilos (`styles.css`)

Resultado de la validación CSS del W3C: _(completar)_

## Evidencia de trabajo en Git

| Integrante | Commits en esta etapa |
| --- | --- |
| Aslyn Zambrano | _(pegar mensajes de `git log --oneline`)_ |
| Stiven Delgado | _(pegar mensajes de `git log --oneline`)_ |

## Fuentes de consulta

- W3C. [A brief history of CSS until 2016](https://www.w3.org/Style/CSS20/history.html)
- MDN Web Docs. [Introduction to the CSS cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade/Introduction)
- MDN Web Docs. [Using color wisely](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Colors/Using_color_wisely)
- W3C. [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)