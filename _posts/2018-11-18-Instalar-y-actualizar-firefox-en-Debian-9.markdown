---
layout: post
title:  "Instalar y Actualizar Firefox en Debian 9 (Stretch)"
date:   2018-11-18 16:34:24 -0300
categories: Linux
permalink: /:categories/:title.html
---
## Firefox por defecto en Debian 9 (Stretch)

Hace poco me decidí por instalar Debian luego de un par de años de utilizar ArchLinux y noté que la versión de firefox que tenía instalada no era la más reciente, de hecho, ni siquiera era el Firefox que conocía.

![Firefox esr](/assets/images/firefox-esr.jpg)

**firefox-esr** es lo que decía el navegador. Investigando un poco descubrí que esta versión de firefox de soporte extendido que sirve bien para empresas pero no tanto para un entusiasta que le gusta disfrutar de las novedades de sus programas favoritos cuando apenas salen...

Ahora sí a lo que vinimos, la instalación de la última versión de Firefox.

### Instalar la versión más reciente de Firefox

*  Primero debemos Descargar la versión más reciente del navegador desde la página oficial de [Firefox](https://www.mozilla.org/) o bien haciendo click [aquí](https://www.mozilla.org/firefox/download/thanks/).

*  Desinstalar la versión actual de Firefor-esr ya que no lo vamos a necesitar y puede causar conflictos.

```
$ sudo apt remove firefox-esr
```


*  Teniendo ya descargado nuestro nuevo firefox, procedemos por descomprimir el archivo. Esto lo haremos por medio de la terminal con el comando

```
$ tar xjf firefox-*.tar.bz2
```


*  El resultado del comando anterior será una carpeta llamada "firefox". Esta carpeta debemos copiarla en el directorio /opt

```
$ sudo cp -rf firefox /opt/
```


*  Ahora para que se reconozca a firefox como un comando interno debemos copiar un link del ejecutable en el directorio /usr/bin/

```
$ sudo ln -s /opt/firefox/firefox /usr/bin/firefox
```


Con esto ya tenemos instaldo la versión más reciente del navegador Firefox en nuestro querido Debian. Si se quiere hacer un acceso directo, los iconos se encuentran en el directiorio /opt/firefox/browser/chrome/icons/default/ .

### Actualizar Firefox.

Para actualizar el navegador debemos seguir los mismos pasos que seguimos para instalarlo, con la omisión del 5to paso. Esto es, descargar la última versión del navegador, descomprimirlo y por último copiar la carpeta en el directorio /opt.

Esto nos tocará hacer cada vez que salga una nueva versión del navegador.
