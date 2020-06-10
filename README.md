<style TYPE="text/css">
code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;}
</style>
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
    tex2jax: {
        inlineMath: [['$','$'], ['\\(','\\)']],
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'] // removed 'code' entry
    }
});
MathJax.Hub.Queue(function() {
    var all = MathJax.Hub.getAllJax(), i;
    for(i = 0; i < all.length; i += 1) {
        all[i].SourceElement().parentNode.className += ' has-jax';
    }
});
</script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-AMS_HTML-full"></script>

# Galería de Fractales

## Geometría fractal

También llamada "geometría de la naturaleza" 

### ¿Qué es un Fractal?

Un fractal es un conjunto que tiene una o
varias de las siguientes propiedades:
• Tiene detalles a todas las escalas.
• Es autosemejante.
• Tiene una definición algorítmica sencilla.
• Tiene dimensión topológica menor que su dimensión de Hausdorff.

# FRACTALES 

## Fractales de Newton 

###  Flor de cinco pétalos

![Flor de 5 pétalos](https://github.com/NicolleMurcia/Fractals-Galery-/blob/master/1%20fractal%20de%20newton.png)

Función con la que se generó $z**5-1$

Para generar este fractal se implemento el siguiente código: 

```
import matplotlib.pyplot as plt
import numpy as np 
from PIL import Image

imgx=800
imgy=800
image=Image.new("RGB",(imgx,imgy))
image.putpixel((100,100),(255,255,255))
image

xa=-1
xb=1
ya=-1
yb=1
maxit=202
h=1e-6
eps=1e-3

def f(z):
    return z**5-1
for y in range (imgy):
    zy=y*(yb-ya)/(imgy-1)+ya
    for x in range (imgx):
        zx=x*(xb-xa)/(imgx-1)+xa
        z=complex(zx,zy)
        for i in range (maxit):
            dz=(f(z+complex(h,h))-f(z))/complex(h,h)
            z0=z-f(z)/dz
            if abs (z0-z)<eps:
                break
            z=z0
            r=i*50
            g=i*70
            b=i*8
            image.putpixel((x,y),(r,g,b))
 
 image


![Trebol morado](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/2%20fractal%20de%20Newton.png)


```

```

