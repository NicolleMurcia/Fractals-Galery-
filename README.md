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

###  Fractal número 1 

![Flor de 5 pétalos](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/1%20fractal%20newton.png)

Función con la que se generó el fractal fue $z^5-1$

Para este fractal se implemento el siguiente código: 

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
```
### Fractal número 2

![Trebol morado](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/2%20fractal%20de%20Newton.png)


La función con la cual se generó este fractal fue $z^7-z^5-z^3-1$

Y el código que se implementó para generar el fractal fue: 

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
    return z**7-z**5-z**3-1
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
            g=i*8
            b=i*70
            image.putpixel((x,y),(r,g,b))
```

### Fractal número 3

![Flor amarilla](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/3%20fractal%20de%20newton.png)

La función con la cual se generó este fractal fue $z^15-z^13-z^11-z^9-z^7-z^5-z^3-1$

Y el código que se implemento fue el siguiente: 

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
    return z**15-z**13-z**11-z**9-z**7-z**5-z**3-1
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
            r=i*80
            g=i*50
            b=i*3
            image.putpixel((x,y),(r,g,b)
```
### Fractal número 4

![Flor morada](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/4%20Fractal%20de%20newton.png)

La función con la cual se generó este fractal fue $z^7-z^6+z^5-z^4+z^3-15$

Y el código que se implementó fue el siguiente: 
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
    return z**7-z**6+z**5-z**4+z**3-15
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
            r=i*80
            g=i*10
            b=i*20
            image.putpixel((x,y),(r,g,b))
```


## Conjunto de Julia 

### Fractal número 1

![Fractal 1 Julia](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/1%20fractal%20de%20Julia.png)

La función con la cual se generó este fractal fue $z^10+i$

Y el código que se implementó fue: 

```
import matplotlib.pyplot as plt
import numpy as np 
from PIL import Image

xa=-1.2
xb=1.2
ya=-1.2
yb=1.2
maxit=30
def f(z):
    return z**10+complex(0,1)

for y in range (imgy):
    zy=y*(yb-ya)/(imgy-1)+ya
    for x in range (imgx):
        zx=x*(xb-xa)/(imgx-1)+xa
        z=complex(zx,zy)
        for i in range (maxit):
            z0=f(z)
            if abs(z)>1000:
                break
            z=z0
            r=i*70
            g=i*90
            b=i*50
            image.putpixel((x,y),(r,g,b))
```

### Fractal número 2

![Fractal 2 Julia](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/2%20fractal%20de%20Julia.png)

La función con la cual se generó este fractal fue $z^4+(0.3+0.5i)$

El código que se implementó para el fractal fue: 

```
import matplotlib.pyplot as plt
import numpy as np 
from PIL import Image

xa=-1.2
xb=1.2
ya=-1.2
yb=1.2
maxit=30
def f(z):
    return z**4+complex(0.3,0.5)

for y in range (imgy):
    zy=y*(yb-ya)/(imgy-1)+ya
    for x in range (imgx):
        zx=x*(xb-xa)/(imgx-1)+xa
        z=complex(zx,zy)
        for i in range (maxit):
            z0=f(z)
            if abs(z)>1000:
                break
            z=z0
            r=i*50
            g=i*8
            b=i*8
            image.putpixel((x,y),(r,g,b))
```

### Fractal número 3

![Fractal 3 Julia](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/3%20fractal%20de%20Julia.png)


La función con la cual se generó este fractal fue, $z^5+i$

El código que se implementó para el fractal fue: 

```
import matplotlib.pyplot as plt
import numpy as np 
from PIL import Image

xa=-1.5
xb=1.5
ya=-1.5
yb=1.5
maxit=30
def f(z):
    return z**5+complex(0,1)

for y in range (imgy):
    zy=y*(yb-ya)/(imgy-1)+ya
    for x in range (imgx):
        zx=x*(xb-xa)/(imgx-1)+xa
        z=complex(zx,zy)
        for i in range (maxit):
            z0=f(z)
            if abs(z)>1000:
                break
            z=z0
            r=i*8
            g=i*55
            b=i*50
            image.putpixel((x,y),(r,g,b))
```

### Fractal número 4

![Fractal 4 Julia](https://raw.githubusercontent.com/NicolleMurcia/Fractals-Galery-/master/4%20fractal%20de%20Julia.png)

La función con la cual se generó este fractal fue, $z^9-z^4+0.5i$

El código que se implementó para este fractal fue: 

```
import matplotlib.pyplot as plt
import numpy as np 
from PIL import Image


xa=-1.2
xb=1.2
ya=-1.2
yb=1.2
maxit=30
def f(z):
    return z**9-z**4+complex(0,0.5)

for y in range (imgy):
    zy=y*(yb-ya)/(imgy-1)+ya
    for x in range (imgx):
        zx=x*(xb-xa)/(imgx-1)+xa
        z=complex(zx,zy)
        for i in range (maxit):
            z0=f(z)
            if abs(z)>1000:
                break
            z=z0
            r=i*70
            g=i*70
            b=i*8
            image.putpixel((x,y),(r,g,b))
            
 ```







