# Flexbox

## 01.Introducción a Flexbox y haciendo el encabezado

### Utilizando la propiedad Flex

Tenemos el siguiente código
```html
<section class="padre">
  <div class="hijo">Primer hijo</div>
  <div class="hijo">Segundo hijo</div>
</section>
```
¿Cómo podemos hacer con flex para que los elementos hijos estén uno al lado del otro?
```css
.padre {
    display: flex;
}
```
### Agregando espacio con Flexbox

```html
<header class="encabezado">
  <a class="logo" href="#">
    <img src="img/logo.png">
  </a>

  <ul class="menu">
    <li class="menu-item">Item 1 del menu</li>
    <li class="menu-item">Item 2 del menu</li>
    <li class="menu-item">Item 3 del menu</li>
    <li class="menu-item">Item 4 del menu</li>
  </ul>
</header>
```
¿Cómo podemos hacer para que el menú se ponga al lado derecho y el logo al lado izquierdo?

Primer debemos poner `display:flex` en el padre, para eso hacemos:

```css
.encabezado {
  display: flex;
}
```
Ahora automáticamente el `.logo` y el `.menu` están uno al lado del otro.

De esta manera debe sobrar mucho espacio a su derecha. Para poner todo ese espacio entre ellos debemos poner la propiedad `justify-content: space-between` en el `.encabezado`, o sea, en el padre.

El código se quedaría así:
```css
.encabezado {
  display: flex;
  justify-content: space-between;
}
```