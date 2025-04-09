# Apuntes Lenguaje de Marcas

En este repositorio encontrarás apuntes relacionados con GitHub, Git y también sobre HTML (Lenguaje de Marcas).

---

## Apuntes de GitHub y comandos Git en la terminal (CMD)

---

### Crear un Repositorio en GitHub

1. Crear una cuenta en [GitHub](https://github.com)
2. Crear un nuevo repositorio:
   - Haz clic en el botón "New" o "Nuevo".
   - Asigna un nombre a tu repositorio.
   - Elige si será público o privado.
   - (Opcional) Agrega un archivo README.
   - Haz clic en "Create repository".

---

### Configuración Inicial

```bash
git config --global user.name "TuNombre"
```
> Configura tu nombre de usuario global para que Git lo use en todos tus commits.

```bash
git config --global user.email "tucorreo@ejemplo.com"
```
> Configura el correo electrónico asociado a tu cuenta de GitHub.

---

### Inicializar un Repositorio

```bash
git init
```
> Crea un nuevo repositorio Git en el directorio actual. Útil para comenzar a versionar un proyecto desde cero.

---

### Clonar un Repositorio Existente

```bash
git clone https://github.com/usuario/nombre-del-repositorio.git
```
> Descarga una copia local de un repositorio remoto.

---

### Gestión de Cambios

```bash
git add archivo.txt
```
> Añade un archivo específico al área de preparación (staging area) para ser incluido en el próximo commit.

```bash
git add .
```
> Añade **todos los archivos modificados o nuevos** al staging area.

```bash
git commit -m "Mensaje descriptivo del commit"
```
> Registra los cambios añadidos al staging area en el historial del proyecto. El mensaje debe describir brevemente lo que hiciste.

```bash
git push origin main
```
> Envía tus commits locales al repositorio remoto, específicamente a la rama `main`.

```bash
git pull
```
> Descarga y fusiona los cambios más recientes del repositorio remoto en tu rama actual.

```bash
git branch nombre-de-rama
```
> Crea una nueva rama con el nombre especificado. Útil para trabajar en funcionalidades sin afectar la rama principal (`main`).

---

## Lenguaje Markdown

- Para escribir código se usan tres comillas invertidas (```)

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
La estructura básica de un documento HTML está compuesta por:

- `<!DOCTYPE html>`: Define que el documento es HTML5.
- `<html>`: Raíz del documento HTML.
- `<head>`: Contiene metadatos como el título, codificación, enlaces a estilos, scripts, etc.
- `<body>`: Contiene todo el contenido visible que el navegador mostrará.

Ejemplo:
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi página</title>
</head>
<body>
  <!-- Contenido visible -->
</body>
</html>
```

### Etiquetas comunes
- **Encabezados (`<h1>` a `<h6>`)**: Títulos jerárquicos.
- **Párrafos (`<p>`)**: Para texto general.
- **Enlaces (`<a>`)**: Para redirigir a otras páginas.
- **Imágenes (`<img>`)**: Muestra imágenes en la web.
- **Listas**:
  - `<ul>`: Lista no ordenada.
  - `<ol>`: Lista ordenada.
  - `<li>`: Elemento de lista.

### Formularios
Permiten a los usuarios enviar datos al servidor.
```html
<form action="/enviar" method="POST">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>
  <input type="submit" value="Enviar">
</form>
```

### Comentarios
No visibles en el navegador.
```html
<!-- Esto es un comentario -->
```

### Estilizar texto
- **Negrita**: `<b>` o `<strong>`
- **Itálica**: `<i>` o `<em>`
- **Subrayado**: `<u>` o `<ins>`
- **Resaltado**: `<mark>Texto</mark>`

---

## Atributos en HTML

- **id**: Identificador único del elemento.
- **class**: Clase para aplicar estilos CSS.
- **src**: Fuente de la imagen o script.
- **href**: Dirección a la que apunta un enlace.
- **alt**: Texto alternativo para imágenes.
- **value**: Valor de un campo.
- **placeholder**: Texto de ayuda en un input.
- **required**: Campo obligatorio.

### Tipos de rutas

- **Ruta absoluta**: Incluye dominio completo.
```html
<a href="https://ejemplo.com">Enlace externo</a>
```
- **Ruta relativa**: Basada en la ubicación del archivo actual.
```html
<a href="/carpeta/pagina.html">Interna</a>
```

---

## Campos comunes en formularios
- `text`, `email`, `password`, `number`, `date`, `file`, `checkbox`, `radio`, `submit`, `button`, `select`, `textarea`

```html
<select name="pais">
  <option value="es">España</option>
  <option value="mx">México</option>
</select>
```

---

## CSS (Cascading Style Sheets)

Permite aplicar estilos visuales a los elementos HTML y separar el contenido de su presentación.

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

- `#id` — selecciona un elemento por su atributo `id`
- `.clase` — selecciona todos los elementos con la clase especificada
- `elemento` — selecciona todos los elementos de ese tipo
- `div > p` — selecciona párrafos que sean hijos directos de un `div`
- `a:hover` — aplica estilo cuando el cursor pasa sobre un enlace (pseudoclase)

### Aplicación del CSS

- **Inline**: Estilo aplicado directamente al elemento  
  ```html
  <p style="color:red">Texto</p>
  ```
- **Interno**: Dentro de una etiqueta `<style>` en el `<head>` del HTML  
  ```html
  <style>
    body { background-color: lightblue; }
  </style>
  ```
- **Externo**: En un archivo separado `.css` enlazado con  
  ```html
  <link rel="stylesheet" href="estilos.css">
  ```

---

## Diseño Responsive

Hace que el diseño se adapte a diferentes dispositivos y tamaños de pantalla, mejorando la experiencia del usuario.

### Recomendaciones

- Usa **unidades relativas** como `%`, `em`, `rem` para mejor escalado
- Aplica **media queries** para cambiar estilos según el tamaño de pantalla
- Usa sistemas de diseño flexibles como **Flexbox** y **Grid**

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

Las sesiones permiten guardar información del usuario entre páginas durante su navegación, como su nombre, rol o estado de inicio de sesión.

### ¿Qué es una sesión?

Una sesión es un espacio de almacenamiento temporal en el servidor que contiene datos específicos del usuario mientras navega por un sitio web.

### ¿Para qué se usan?

- Autenticación de usuarios (login/logout)
- Mostrar contenido personalizado
- Proteger rutas restringidas
- Guardar datos como un carrito de compras

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

> Nota: `session_start()` debe ejecutarse siempre antes de cualquier salida HTML para que funcione correctamente.
