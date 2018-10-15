---
layout: post
title:  "Propiedades de Flexbox"
date:   2018-10-06
categories: Frontend
permalink: /:categories/:title.html
---
# Flexbox

## ¿Que es flexbox?
Flexbox es un módulo de diseño de css cuyo propósito es mejorar la manera en que diseñamos, tanto en la distribucion de los elementos como en la alineación de los mismos.

## ¿Para qué nos sirve flexbox?
Flexbox nos permite alterar el tamaño de los elementos (width/height), su orden y la separación entre cada elemento para que se adapten al tamaño de la pantalla. Puede separar los elementos para que ocupen el mayor ancho posible o los encoja para provenir un deborde.

## Usos de Flexbox
Para hacer uso de las propiedades de flexbox primero debemos definirlo en el contenedor de nuestros elementos, esto nos permitirá hacer uso de flexbox en sus hijos directos pero nó en los elementos contenidos en ellos.

###### html
```html
<div class="container">
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
    <div class="item"></div>
</div>
```

###### css
```css
.container
{
  display: flex;
  background-color: #01889e;
  height: 200px;
  width: 500px;
}

.item
{
  height: 50px;
  width: 100px;
  border: 2px solid #75fda8;
  background-color: #d5869c;
}
```
###### Display

![My helpful screenshot](/assets/images/flexbox01.jpg)

### Alcance de flexbox
Para que los elementos dentro de los hijos del contenedor compartan la misma propiedad de flexbox, se deben heredar o definir nuevamente dentro de los elementos del contenedor.

```css
.container
{
  display: flex;
  background-color: #01889e;
  height: 200px;
  width: 500px;
}

.item
{
  display: inherit; /*Se hereda la propiedad de flexbox definida en el contenedor*/
  height: 50px;
  width: 100px;
  border: 2px solid #75fda8;
  background-color: #d5869c;
}
```
