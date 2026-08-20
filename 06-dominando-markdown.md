# 06. Dominando Markdown y Estructura Esencial

[⬅️ Módulo Anterior: Chuleta de Comandos](./05-chuleta-comandos-git.md) | [🏠 Volver al Índice](./README.md) | [Siguiente Módulo: GFM, Mermaid y Avanzado ➡️](./07-gfm-mermaid-y-avanzado.md)


## 🖋️ ¿Qué es Markdown y por qué es tan popular?

Creado en 2004 por John Gruber y Aaron Swartz, **Markdown** es el lenguaje de formato estándar del mundo del desarrollo. Su filosofía es simple: **permitirte escribir texto estructurado y legible usando caracteres sencillos del teclado**, sin la complejidad de escribir etiquetas HTML pesadas.

Es el formato oficial de los archivos **`README.md`**, la documentación técnica, los blogs de programación y herramientas de productividad como Notion u Obsidian.


## 📑 1. Encabezados y Jerarquía

Los encabezados estructuran tu documento desde el nivel principal (`#`) hasta el menor nivel de detalle (`######`):

### A. Encabezados con Sintaxis Markdown

<table border="0">
  <tr>
    <th width="50%">Código Markdown</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
  # Título Principal (H1)
  ## Sección (H2)
  ### Subsección (H3)
  #### Sub-subsección (H4)
  ##### Detalle (H5)
  ###### Nota Menor (H6)
```

</td>
<td>

# Título Principal (H1)
## Sección (H2)
### Subsección (H3)
#### Sub-subsección (H4)
##### Detalle (H5)
###### Nota Menor (H6)

</td>
</tr>
</table>

### B. Encabezados con Etiquetas HTML

<table border="0">
  <tr>
    <th width="50%">Código HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```html
<h1>Título Principal (H1)</h1>
<h2>Sección (H2)</h2>
<h3>Subsección (H3)</h3>
<h4>Sub-subsección (H4)</h4>
<h5>Detalle (H5)</h5>
<h6>Nota Menor (H6)</h6>
```

</td>
<td>

<h1>Título Principal (H1)</h1>
<h2>Sección (H2)</h2>
<h3>Subsección (H3)</h3>
<h4>Sub-subsección (H4)</h4>
<h5>Detalle (H5)</h5>
<h6>Nota Menor (H6)</h6>

</td>
</tr>
</table>

> [!TIP]
> Por accesibilidad y buenas prácticas SEO/documentación, utiliza un único `# H1` por archivo y mantén una jerarquía descendente lógica sin saltarte niveles.


## ✍️ 2. Formato de Texto y Tipografía

En Markdown y HTML puedes aplicar estilos al texto para enfatizar ideas:

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
**Texto en negrita**
*Texto en cursiva*
***Texto en negrita y cursiva***
~~Texto tachado~~
`Código inline`

<!-- También con etiquetas HTML: -->
<strong>Texto en negrita con strong</strong>
<em>Texto en cursiva con em</em>
<u>Texto subrayado</u>
<mark>Texto resaltado con marca</mark>

<!-- Subíndices y Superíndices: -->
H<sub>2</sub>O (Fórmula del agua)
E = mc<sup>2</sup> (Teoría de la relatividad)
```

</td>
<td>

**Texto en negrita**  
*Texto en cursiva*  
***Texto en negrita y cursiva***  
~~Texto tachado~~  
`Código inline`  

<strong>Texto en negrita con strong</strong>  
<em>Texto en cursiva con em</em>  
<u>Texto subrayado</u>  
<mark>Texto resaltado con marca</mark>  

H<sub>2</sub>O (Fórmula del agua)  
E = mc<sup>2</sup> (Teoría de la relatividad)

</td>
</tr>
</table>


## 📋 3. Listas en Markdown y HTML

### A. Listas Desordenadas (Viñetas)

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
<!-- En Markdown (- , * o +) -->
- Lenguajes Frontend
  - JavaScript
  - TypeScript
- Lenguajes Backend
  - Python
  - Go

<!-- En HTML -->
<ul>
  <li>Bases de Datos
    <ul>
      <li>PostgreSQL</li>
      <li>MongoDB</li>
    </ul>
  </li>
  <li>DevOps & Cloud</li>
</ul>
```

</td>
<td>

- Lenguajes Frontend
  - JavaScript
  - TypeScript
- Lenguajes Backend
  - Python
  - Go

<ul>
  <li>Bases de Datos
    <ul>
      <li>PostgreSQL</li>
      <li>MongoDB</li>
    </ul>
  </li>
  <li>DevOps & Cloud</li>
</ul>

</td>
</tr>
</table>

### B. Listas Ordenadas y Estilos de Numeración

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
<!-- Lista ordenada estándar en Markdown -->
1. Instalar dependencias
2. Configurar variables de entorno
   1. Crear archivo .env
   2. Asignar claves API
3. Iniciar el servidor local

<!-- Lista HTML con números romanos (type="I") -->
<ol type="I">
  <li>Fase de Análisis</li>
  <li>Fase de Desarrollo</li>
  <li>Fase de Despliegue</li>
</ol>

<!-- Lista HTML alfabética empezando en letra E (start="5") -->
<ol type="A" start="5">
  <li>Módulo E</li>
  <li>Módulo F</li>
</ol>
```

</td>
<td>

1. Instalar dependencias
2. Configurar variables de entorno
   1. Crear archivo .env
   2. Asignar claves API
3. Iniciar el servidor local

<ol type="I">
  <li>Fase de Análisis</li>
  <li>Fase de Desarrollo</li>
  <li>Fase de Despliegue</li>
</ol>

<ol type="A" start="5">
  <li>Módulo E</li>
  <li>Módulo F</li>
</ol>

</td>
</tr>
</table>

### C. Listas de Descripción y Definición (Markdown vs HTML)

> [!NOTE]
> En algunas variantes de Markdown (como Pandoc o PHP Markdown Extra) existe la sintaxis `Término\n: Definición`, pero **GitHub (GFM) no la soporta**. En GitHub tienes dos formas de lograrlo:

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
<!-- Opción 1: En Markdown nativo (con sangría de 2 a 4 espacios) -->
- **Git**
  Sistema de control de versiones distribuido local.
- **GitHub**
  Plataforma en la nube para alojar repositorios Git.
  
  Permite colaborar con desarrolladores de todo el mundo.

<!-- Opción 2: En HTML semántico (<dl>, <dt>, <dd>) -->
<dl>
  <dt><strong>Git</strong></dt>
  <dd>Sistema de control de versiones distribuido local.</dd>
  <dt><strong>GitHub</strong></dt>
  <dd>Plataforma en la nube para alojar repositorios Git.</dd>
  <dd>Incluye herramientas de CI/CD, gestión de proyectos y colaboración.</dd>
</dl>
```

</td>
<td>

- **Git**  
  Sistema de control de versiones distribuido local.
- **GitHub**  
  Plataforma en la nube para alojar repositorios Git.  
  
  Permite colaborar con desarrolladores de todo el mundo.

<dl>
  <dt><strong>Git</strong></dt>
  <dd>Sistema de control de versiones distribuido local.</dd>
  <dt><strong>GitHub</strong></dt>
  <dd>Plataforma en la nube para alojar repositorios Git.</dd>
  <dd>Incluye herramientas de CI/CD, gestión de proyectos y colaboración.</dd>
</dl>

</td>
</tr>
</table>


## 🔗 4. Enlaces y Multimedia

### A. Enlaces en Markdown y HTML

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
<!-- Enlace estándar -->
[Sitio Oficial de GitHub](https://github.com)

<!-- Enlace con tooltip al pasar el cursor -->
[Documentación de Git](https://git-scm.com "Sitio oficial de Git")

<!-- Enlace automático por URL -->
<https://github.com>

<!-- Enlace a otro archivo del repositorio -->
[Ver Chuleta de Comandos](./05-chuleta-comandos-git.md)

<!-- Enlace en HTML (abre en nueva pestaña) -->
<a href="https://github.com" target="_blank">Abrir GitHub ↗</a>
```

</td>
<td>

[Sitio Oficial de GitHub](https://github.com)  

[Documentación de Git](https://git-scm.com "Sitio oficial de Git")  

<https://github.com>  

[Ver Chuleta de Comandos](./05-chuleta-comandos-git.md)  

<a href="https://github.com" target="_blank">Abrir GitHub ↗</a>

</td>
</tr>
</table>

### B. Inserción de Imágenes

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
<!-- Imagen con enlace clicable (Badge) -->
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com)

<!-- Imagen centrada con tamaño personalizado en HTML -->
<div align="center">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub Logo" width="80">
</div>
```

</td>
<td>

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com)

<div align="center">
  <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub Logo" width="80">
</div>

</td>
</tr>
</table>

### C. Inserción de Videos

Markdown no permite reproductores `<iframe>` externos por seguridad. Se utilizan dos métodos oficiales:

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
<!-- 1. Miniatura interactiva de YouTube -->
[![Ver Tutorial de Git en YouTube](https://img.youtube.com/vi/HiXLkL42tMU/hqdefault.jpg)](https://www.youtube.com/watch?v=HiXLkL42tMU)

<!-- 2. Video HTML5 nativo (para archivos .mp4) -->
<video src="video.mp4" controls width="100%">
  Tu navegador no soporta video.
</video>
```

</td>
<td>

<div align="center">
  <a href="https://www.youtube.com/watch?v=HiXLkL42tMU" target="_blank">
    <img src="https://img.youtube.com/vi/HiXLkL42tMU/hqdefault.jpg" alt="Ver Tutorial de Git en YouTube" width="380" style="border-radius: 8px;">
  </a>
</div>

</td>
</tr>
</table>


## 💬 5. Citas y Bloques de Código

### A. Citas (Blockquotes)

<table border="0">
  <tr>
    <th width="50%">Código Markdown</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
> "El software libre es una cuestión de libertad, no de precio."
> — Richard Stallman
>
> > Cita anidada de segundo nivel.
```

</td>
<td>

> "El software libre es una cuestión de libertad, no de precio."
> — Richard Stallman
>
> > Cita anidada de segundo nivel.

</td>
</tr>
</table>

### B. Bloques de Código con Sintaxis Resaltada

<table border="0">
  <tr>
    <th width="50%">Código Markdown</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

````markdown
```javascript
function calcularTotal(precio, cantidad) {
  return precio * cantidad;
}
console.log(calcularTotal(50, 3));
```

```python
def saludar(nombre: str) -> str:
    return f"¡Hola, {nombre}!"

print(saludar("Mundo"))
```

```diff
- function suma(a, b) { return a - b; }
+ function suma(a, b) { return a + b; }
```
````

</td>
<td>

```javascript
function calcularTotal(precio, cantidad) {
  return precio * cantidad;
}
console.log(calcularTotal(50, 3));
```

```python
def saludar(nombre: str) -> str:
    return f"¡Hola, {nombre}!"

print(saludar("Mundo"))
```

```diff
- function suma(a, b) { return a - b; }
+ function suma(a, b) { return a + b; }
```

</td>
</tr>
</table>


## 📊 6. Tablas en Markdown y HTML: Guía Definitiva

### A. Anatomía y Reglas de Alineación en Markdown

La posición de los dos puntos (`:`) en la fila divisoria define la alineación:

| Sintaxis en la Fila Divisoria | Tipo de Alineación | Uso Recomendado |
| :--- | :---: | :--- |
| `---` o `:---` | **Izquierda** (Por defecto) | Nombres, textos largos, descripciones. |
| `:---:` | **Centrado** | Iconos, fechas, estados, versiones, insignias. |
| `---:` | **Derecha** | Números, cantidades, precios, porcentajes. |

<table border="0">
  <tr>
    <th width="50%">Código Markdown</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown
| Herramienta | Categoría | Estado | Popularidad | Versión |
| :--- | :--- | :---: | ---: | :--- |
| React | Frontend | 🟢 Activo | 220k ⭐ | v18.3 |
| Node.js | Backend | 🟢 Activo | 105k ⭐ | v20.14 |
| Tailwind | Estilos | 🟢 Activo | 80k ⭐ | v3.4 |
```

</td>
<td>

| Herramienta | Categoría | Estado | Popularidad | Versión |
| :--- | :--- | :---: | ---: | :--- |
| React | Frontend | 🟢 Activo | 220k ⭐ | v18.3 |
| Node.js | Backend | 🟢 Activo | 105k ⭐ | v20.14 |
| Tailwind | Estilos | 🟢 Activo | 80k ⭐ | v3.4 |

</td>
</tr>
</table>

### B. Tablas sin Encabezado (Evitar el Resaltado de la Primera Fila)

En Markdown, la primera fila siempre se convierte en encabezado (`<th>`). Para evitar ese resaltado:

<table border="0">
  <tr>
    <th width="50%">Método en Código</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```html
<!-- Opción 1: HTML con <table> y <td> (Recomendado) -->
<table>
  <tr>
    <td>Frontend</td>
    <td>React, Vue, Angular</td>
  </tr>
  <tr>
    <td>Backend</td>
    <td>Node.js, Python, Go</td>
  </tr>
</table>
```

```markdown
<!-- Opción 2: Fila fantasma en Markdown (&nbsp;) -->
| &nbsp; | &nbsp; |
| :--- | :--- |
| Frontend | React, Vue, Angular |
| Backend | Node.js, Python, Go |
```

</td>
<td>

<table>
  <tr>
    <td>Frontend</td>
    <td>React, Vue, Angular</td>
  </tr>
  <tr>
    <td>Backend</td>
    <td>Node.js, Python, Go</td>
  </tr>
</table>

| &nbsp; | &nbsp; |
| :--- | :--- |
| Frontend | React, Vue, Angular |
| Backend | Node.js, Python, Go |

</td>
  </tr>
</table>

### C. Combinar Celdas (Colspan y Rowspan en HTML)

> [!IMPORTANT]
> **Markdown puro NO permite combinar celdas.** Si necesitas fusionar celdas horizontalmente o verticalmente, debes utilizar **HTML**.

<table border="0">
  <tr>
    <th width="50%">Código HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```html
<table>
  <thead>
    <tr>
      <th>Área</th>
      <th>Tecnología</th>
      <th>Nivel</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2"><strong>Desarrollo Web</strong></td>
      <td>React.js</td>
      <td>Avanzado</td>
    </tr>
    <tr>
      <td>Node.js</td>
      <td>Intermedio</td>
    </tr>
    <tr>
      <td colspan="3" align="center"><em>Total: 2 tecnologías clave</em></td>
    </tr>
  </tbody>
</table>
```

</td>
<td>

<table>
  <thead>
    <tr>
      <th>Área</th>
      <th>Tecnología</th>
      <th>Nivel</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2"><strong>Desarrollo Web</strong></td>
      <td>React.js</td>
      <td>Avanzado</td>
    </tr>
    <tr>
      <td>Node.js</td>
      <td>Intermedio</td>
    </tr>
    <tr>
      <td colspan="3" align="center"><em>Total: 2 tecnologías clave</em></td>
    </tr>
  </tbody>
</table>

</td>
</tr>
</table>


## 🧱 7. Espaciadores, Saltos de Línea y Comentarios Ocultos

<table border="0">
  <tr>
    <th width="50%">Código Markdown / HTML</th>
    <th width="50%">Renderizado Visual</th>
  </tr>
  <tr>
    <td>

```markdown

<!-- 1. Salto de línea desaparece -->
Línea 1 sin espacios al final
Línea 2 inemdiatamente despues

<!-- 2. Espacio extra -->
Línea 1 normal

Línea 2 separada por salto de linea

<!-- 3. Salto de línea con doble espacio al final -->
Línea 1 con dos espacios al final  
Línea 2 inmediatamente abajo

<!-- 4. Salto de línea forzado con HTML -->
Primera línea<br/>Segunda línea

<!-- 5. Espacios en blanco adicionales con &nbsp; -->
Palabra&nbsp;&nbsp;&nbsp;&nbsp;Separada (con 4 espacios)
&nbsp;&nbsp;&nbsp;&nbsp;Texto con sangría manual

<!-- 6. Línea divisoria horizontal -->
Texto superior
---
Texto inferior

<!-- 7. Comentario invisible en el documento -->
<!-- Recordatorio: Actualizar versión en 2026 -->
```

</td>
<td>

Línea 1 sin espacios al final
Línea 2 inemdiatamente despues

Línea 1 normal

Línea 2 separada por salto de linea

Línea 1 con dos espacios al final  
Línea 2 inmediatamente abajo

Primera línea<br/>Segunda línea

Palabra&nbsp;&nbsp;&nbsp;&nbsp;Separada (con 4 espacios)  
&nbsp;&nbsp;&nbsp;&nbsp;Texto con sangría manual

Texto superior
---
Texto inferior

*(El comentario permanece oculto en la vista renderizada)*

</td>
</tr>
</table>

## 🌐 8. Tutoriales y Referencias Recomendadas

- 📖 **[Tutorial Markdown](https://tutorialmarkdown.com/)** — Guía interactiva y completa paso a paso para dominar la sintaxis.
- 🎓 **[Curso de Markdown por Luis Llamas](https://www.luisllamas.es/curso-markdown/)** — Tutorial detallado con trucos avanzados y buenas prácticas.
- 🖼️ **[Guía de Inserción de Imágenes en Markdown (Denshub)](https://denshub.com/es/hugo-post-insert-image/)** — Explicación profunda sobre gestión, formatos y ajuste de imágenes.
- 📑 **[Especificación Oficial de GFM (GitHub)](https://github.github.com/gfm/)** — Documentación técnica oficial de GitHub Flavored Markdown.
- 📘 **[The Markdown Guide](https://www.markdownguide.org/)** — Referencia global y completa de sintaxis Markdown.

---

[⬅️ Módulo Anterior: Chuleta de Comandos](./05-chuleta-comandos-git.md) | [🏠 Volver al Índice](./README.md) | [Siguiente Módulo: GFM, Mermaid y Avanzado ➡️](./07-gfm-mermaid-y-avanzado.md)
