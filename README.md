# Plantilla LaTeX para Proyecto de Grado (Normas APA)

Plantilla de libre uso para la documentación de 
proyectos de grado bajo normas APA.

## Enlaces Importantes
* [Diapos y guia "Taller de LaTeX 2022", un completo recurso para comprender los comandos básicos de LaTeX](https://slides.com/cr0wg4n/taller-de-latex/edit)
* [Post/Artículo especial sobre este repositorio](https://cr0wg4n.medium.com/documenta-tu-proyecto-de-grado-con-latex-sin-morir-en-el-intento-ft-normas-apa-15bf50a2ee01)

## Requerimientos
> ⚠️ Es importante tener instalados todos los requerimientos.

> ⚠️ Si utilizas **MiKTeX** no olvides actualizarlo.

* Python 3 o mayor
* Pygments (paquete en pip). Ejemplo de instalación: `pip install Pygments` o `pip3 install Pygments` 
* Preparar el ambiente ([tutorial](https://cr0wg4n.medium.com/latex-y-visual-studio-code-gu%C3%ADa-de-instalaci%C3%B3n-ca8bef3935e3)).

## Estructura de archivos

Los directorios mas importantes son:
- ```configs```, directorio de las configuraciones de la plantilla. En el archivo ```dockstyle.sty``` se realiza la introducción de datos personales para la personalización de la plantilla.
- ```capitulos```, directorio contenedor de los capítulos del documento.
- ```anexos```, directorio contenedor de los anexos del documento.
- ```img```, directorio contenedor de las imagenes del documento, es recomendable manejarlos en directorios distintos por capítulos.
- ```codigo```, directorio para adjuntar archivos de código en texto plano.

## Uso 

El archivo principal es ```main.tex``` y puede ser ejecutado en cualquier editor
de LaTeX.

El archivo ```.latexmkrc``` introduce un flag o argumento denominado ```--shell-escape``` que permite externalizar la composición tipográfica, en este caso permite trabajar al paquete tikz entre otros, que comúnmente se usan para graficación o renderización de imagenes.

La compilación debe ser a través de ```pdflatex``` (la mayoria de los editores lo tienen por defecto).

Esta plantilla fue elaborada en [Visual Studio Code](https://code.visualstudio.com/) con la extensión [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), otra muy
buena alternativa es [Texmaker](https://www.xm1math.net/texmaker/).

Acá un [tutorial](https://cr0wg4n.medium.com/latex-y-visual-studio-code-gu%C3%ADa-de-instalaci%C3%B3n-ca8bef3935e3) para correr LaTeX en Visual Studio Code.

## Ejemplo

El documento ```.pdf``` resultado de la compilación es [main.pdf](https://github.com/cr0wg4n/plantilla-latex-proyecto-de-grado/blob/master/build/main.pdf) y normalmente se encuentra en el directorio build.

## Vista Previa 

![](https://github.com/cr0wg4n/plantilla-latex-proyecto-de-grado/blob/master/img/preview.jpg)

## Reducción de tamaño de archivo pdf

En muchas ocasiones el archivo alcanza logra un peso demasiado alto, eso dependerá de cuantas imágenes estas empleando en el documento, para ello puedes correr el siguiente comando, pero antes necesitas 
instalar [ghostscript](https://www.ghostscript.com/), te aconsejo correr el comando en una terminal con bash:

```bash
gswin64c -sDEVICE=pdfwrite -dDownsampleColorImages=true -dDownsampleGrayImages=true -dDownsampleMonoImages=true -dColorImageResolution=300 -dGrayImageResolution=300 -dMonoImageResolution=300 -dColorImageDownsampleThreshold=1.0 -dGrayImageDownsampleThreshold=1.0 -dMonoImageDownsampleThreshold=1.0 -dCompatibilityLevel=1.4 -dNOPAUSE -dQUIET -dBATCH -sOutputFile=build/main-compressed.pdf build/main.pdf
```

Para lograr mejores o peores resultado puedes ajustar el valor de los parámetros (`dColorImageResolution`, `dGrayImageResolution`, `dMonoImageResolution`), estos parámetros tienen que ver con la calidad en la que se procesaran las imágenes internas, LaTeX suele conservar la mejor calidad, pero modificando estos parámetros es posible cambiar la resolución de las imágenes logrando un menor tamaño en el peso del archivo pdf final.
