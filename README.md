# ApuntesLenguajeMarcas
En este github se podrá encontrar apuntes sobre el propio Github,  lenguaje HTML

## Apuntes de GitHub y sus Comandos en el CMD

### Crear un Repositorio en GitHub

1. Crear una cuenta en GitHub
2. Crear un nuevo Repositorio:
   - Haz clic en el botón "New" o "Nuevo" en tu página de inicio de GitHub.
   - Asigna un nombre a tu repositorio
   - Decide si el repositorio será público o privado.
   - Puedes agregar un archivo README para describir tu proyecto.
   - Haz clic en "Create repository".

### Comandos básicos de Git en CMD

1. **Configuración inicial:**
   - `git config --global user.name`
   - `git config --global user.email`

2. **Inicializar un repositorio**
   - `git init`

3. **Clonar un repositorio**
   - `git clone https://github.com/usuario/nombre-del-repositorio.git`

4. **Gestionar cambios**
   - `git add archivo.txt` — Añadir un archivo específico
   - `git add .` — Añadir todos los archivos
   - `git commit -m "Mensaje descriptivo del commit"`
   - `git push origin main`
   - `git branch nombre-de-rama`
   - `git pull`

---

## Lenguaje Markdown

- Para escribir código se usan tres comillas invertidas (\`\`\`)

### Encabezados

```markdown
# Encabezado 1
## Encabezado 2
### Encabezado 3
```

### Énfasis

```markdown
*Itálica* o _Itálica_
**Negrita** o __Negrita__
***Negrita y Itálica***
```

### Listas

- **Listas no ordenadas:**

```markdown
- Elemento 1
- Elemento 2
  - Sub Elemento
```

- **Listas ordenadas:**

```markdown
1. Primer ítem
2. Segundo ítem
```

### Links

```markdown
[NombreLink](LinkURL "Título opcional")
```

### Imágenes

```markdown
![NombreImagen](LinkImagen "Título opcional")
```

### Tablas

```markdown
| **Titulo 1** | **Titulo 2** | **Titulo 3** |
|:------------:|--------------:|:-------------|
```

---

## Conceptos HTML

### Estructura básica de un HTML

- El `head` contiene el título de la página.
- El `body` contiene el contenido visible en el navegador.

### Etiquetas comunes

- **Encabezados (`h1`-`h6`)**  
  Cambian de tamaño según el número.

- **Párrafos (`<p>`)**  
  Se usan para escribir texto común.

- **Enlaces (`<a>`)**  
  Sirven para enlazar con otras páginas.

- **Imágenes (`<img>`)**  
  Muestran una imagen en la web.

- **Listas**
  - `ul`: Lista no ordenada.
  - `ol`: Lista ordenada.

### Formularios

- Permiten a los usuarios introducir y enviar datos mediante inputs, selects, etc.

### Comentarios

- No se muestran en el navegador.
```html
<!-- Esto es un comentario -->
```

### Estilizar texto

- **Negrita**  
  `<b>Texto</b>` o `<strong>Texto</strong>`

- **Itálica**  
  `<i>Texto</i>` o `<em>Texto</em>`

- **Subrayado**  
  `<u>Texto</u>` o `<ins>Texto</ins>`

- **Resaltado**  
  `<mark>Texto</mark>`
  
## Formularios HTML

Los formularios permiten recolectar información del usuario a través de campos interactivos.

### Estructura Básica

```html
<form action="/enviar" method="POST">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <input type="submit" value="Enviar">
</form>
```

### Tipos de Campos Comunes

- `text`, `textarea`, `email`, `password`, `number`, `date`, `file`, `checkbox`, `radio`, `select`, `submit`, `button`.

```html
<select name="pais">
  <option value="es">España</option>
  <option value="mx">México</option>
</select>
```

---

## CSS (Cascading Style Sheets)

Permite aplicar estilos visuales a los elementos HTML.

### Sintaxis Básica

```css
selector {
  propiedad: valor;
}
```

### Ejemplo

```css
body {
  font-family: Arial;
  background-color: #f4f4f4;
}

input[type="text"] {
  border: 1px solid #ccc;
  padding: 8px;
}
```

### Selectores útiles

- `#id` — selecciona por ID
- `.clase` — selecciona por clase
- `elemento` — selecciona por etiqueta
- `div > p` — hijo directo
- `a:hover` — pseudoclase

### Aplicación del CSS

- **Inline**: `<p style="color:red">Texto</p>`
- **Interno**: dentro de `<style>` en HTML
- **Externo**: enlazado con `<link rel="stylesheet" href="estilos.css">`

---

## Diseño Responsive

Hace que el diseño se adapte a diferentes dispositivos y tamaños de pantalla.

### Recomendaciones

- Usa **unidades relativas**: `%`, `em`, `rem`
- Aplica **media queries** para adaptar estilos
- Usa diseño flexible con **Flexbox** o **Grid**

### Ejemplo con Media Query

```css
/* Estilo base */
body {
  font-size: 16px;
}

/* Móvil */
@media (max-width: 768px) {
  body {
    font-size: 14px;
  }

  .menu {
    display: none;
  }
}
```

### Ejemplo con Flexbox

```css
.contenedor {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
```

---

## Sesiones en Aplicaciones Web

Las sesiones permiten guardar información del usuario entre páginas o durante su visita.

### ¿Qué es una sesión?

Una sesión almacena datos temporales para un usuario, como si ha iniciado sesión, su carrito de compras, etc.

### Ejemplo en PHP

```php
<?php
session_start();

// Guardar datos
$_SESSION['usuario'] = 'juan123';

// Leer datos
echo $_SESSION['usuario'];

// Eliminar sesión
session_destroy();
?>
```

### Uso común

- Autenticación de usuarios
- Mostrar contenido personalizado
- Proteger rutas restringidas
