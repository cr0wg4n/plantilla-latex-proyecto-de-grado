# Plantilla LaTeX para Proyecto de Grado (Normas APA)

Plantilla de libre uso para la documentación de 
proyectos de grado bajo normas APA.

[Enlace](https://cr0wg4n.medium.com/documenta-tu-proyecto-de-grado-con-latex-sin-morir-en-el-intento-ft-normas-apa-15bf50a2ee01) al artículo de este repositorio.

## Estructura

Los directorios mas importantes son:
- ```configs```, directorio de las configuraciones de la plantilla. En el archivo ```dockstyle.sty``` se realiza la introducción de datos personales para la personalización de la plantilla.
- ```capitulos```, directorio contenedor de los capítulos del documento.
- ```anexos```, directorio contenedor de los anexos del documento.
- ```img```, directorio contenedor de las imagenes del documento, es recomendable manejarlos en directorios distintos por capítulos.

## Uso 

El archivo principal es ```main.tex``` y puede ser ejecutado en cualquier editor
de LaTeX.

El archivo ```.latexmkrc``` introduce un flag o argumento denominado ```--shell-escape``` que permite externalizar la composición tipográfica, en este caso permite trabajar al paquete tikz entre otros, que comúnmente se usan para graficación o renderización de imagenes.

La compilación debe ser a través de ```pdflatex``` (la mayoria de los editores lo tienen por defecto).

Esta plantilla fue elaborada en [Visual Studio Code](https://code.visualstudio.com/) con la extensión [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), otra alternativa es [Texmaker](https://www.xm1math.net/texmaker/).

Acá un [tutorial](https://cr0wg4n.medium.com/latex-y-visual-studio-code-gu%C3%ADa-de-instalaci%C3%B3n-ca8bef3935e3) para correr LaTeX en Visual Studio Code.

## Ejemplo

El documento ```.pdf``` resultado de la compilación es [main.pdf](https://github.com/cr0wg4n/plantilla-latex-proyecto-de-grado/blob/master/build/main.pdf) y normalmente se encuentra en el directorio build.

## Vista Previa 

![](https://github.com/cr0wg4n/plantilla-latex-proyecto-de-grado/blob/master/img/preview.png)
