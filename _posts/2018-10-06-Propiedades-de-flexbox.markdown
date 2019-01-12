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

## Aplicación de flexbox
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

![flex image 01](/assets/images/flexbox01.jpg)

### Alcance de flexbox
Para que los elementos dentro de los hijos del contenedor compartan la misma propiedad de flexbox, se deben heredar o definir nuevamente dentro de los elementos del contenedor.

En el ejemplo anterior, los número 1, 2 y 3 déntro de los ítems no tienen la propiedad de flexbox. Si quisieramos que comparta la mísma propiedad tendríamos heredarla del contenedor.

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
  display: inherit; /*Se hereda la propiedad de flexbox definida en el contenedor*/
  height: 50px;
  width: 100px;
  border: 2px solid #75fda8;
  background-color: #d5869c;
}
```
* * *
### Propiedades de flexbox
#### 1) flex-direction:
flex-direction establece el eje principal de los elementos y el sentido de la misma.

1.1) **flex-direction: row;**

Esta propiedad es la que viene establecida por defecto y lo que hace es ordenar los elementos de manera horizontal con sentido de Izquierda a Derecha.

###### css
```css
.container
{
  display: flex;
  flex-direction: row; /* por defecto */
  background-color: #01889e;
  height: 200px;
  width: 500px;
}
```
###### Display
![flex image 02](/assets/images/flexbox02.jpg)

1.2) **flex-direction: row-reverse;**

Tiene la misma función que la propiedad anterior, pero con sentido invertido. Esto es de Derecha a Izquierda.

###### css
```css
.container
{
  display: flex;
  flex-direction: row-reverse; /* invierte el sentido de los elementos */
  background-color: #01889e;
  height: 200px;
  width: 500px;
}
```
###### Display
![flex image 03](/assets/images/flexbox03.jpg)

1.3) **flex-direction: column;**

Esta propiedad invierte el sentido del eje principal estableciendolo de manera vertical con dirección de arriba a abajo.

###### css
```css
.container
{
  display: flex;
  flex-direction: column; /* Ordena los elemento de manera vertical */
  background-color: #01889e;
  height: 200px;
  width: 500px;
}
```
###### Display
![flex image 04](/assets/images/flexbox04.jpg)

1.4) **flex-direction: column-reverse;**

De la misma manera que hicimos con la propiedad **row**, con esta propiedad invertimos la dirección dispuesta de los elemeton para que se muestren ahora de abajo hacia arriba.

###### css
```css
.container
{
  display: flex;
  flex-direction: column-reverse; /* Invierte el sentido de la columna */
  background-color: #01889e;
  height: 200px;
  width: 500px;
}
```
###### Display
![flex image 05](/assets/images/flexbox05.jpg)









































