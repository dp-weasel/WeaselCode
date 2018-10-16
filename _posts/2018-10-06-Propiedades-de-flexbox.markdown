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
#### flex-direction:
flex-direction establece el eje principal de los elementos y el sentido de la misma.

Para defectos los elementos se ordenan de en el eje horizontal de derecha a izquierda, esto es porque por defecto viene con **flex-direction: row;**

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

Para invertir el sentido y ordenar los elementos de Derecha a Izquierda se utiliza la propiedad **flex-direction: row-reverse;**

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

Para establecer el eje principal de manera vertical se establece la propiedad **flex-direction: column;**.

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

En este caso los elementos se ordenaron de arriba hacia abajo, de la misma manera que hicimos con la propiedad **row**, podemos invertir este orden para que los items se muestren de abajo hacia arriba con la propiedad **flex-direction: column-reverse;**

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









































