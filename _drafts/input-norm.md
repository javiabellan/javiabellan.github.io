---
title: Input normalization
---



Pasarle los input a pelo a la red puede ser una mala idea, ya que la red convergerá más ráppido si le pasamos **una entrada con valores cercanos a cero**.

Además esta herística no solo debe ser aplicada a la capa de entrada solo, sino a todas las capas.

Normalmente, para datasets grandes y variados, la gente calcula la media (mean) y desviacion standard (std)
y normalizan `(img - MEAN) / STD`. Esto lo que hace es escalar y mover la entrada cerca de 0  (media=0 y varianza=1).


## Código

```python
import numpy as np

entrada = np.random.uniform(low=0, high=10, size=(32,2))
print("Entrada:",entrada)
print("t\Media:", entrada.mean())
print("t\Varianza:", entrada.var())

entrada_normalizada = (entrada - entrada.mean()) / entrada.std()
print("Entrada:",entrada_normalizada)
print("t\Media:", entrada_normalizada.mean())
print("t\Varianza:", entrada_normalizada.var())

####### PRINT
import matplotlib.pyplot as plt

f, ((ax1, ax2), (ax3, ax4)) = plt.subplots(2, 2)
ax1.set_title('Entrada')
ax1.scatter(entrada[:,0], entrada[:,1])
ax2.set_title('Entrada normalizada')
ax2.axhline(y=0, color='k')
ax2.axvline(x=0, color='k')
#axes.set_xlim([xmin,xmax])
#axes.set_ylim([ymin,ymax])
ax2.scatter(entrada_normalizada[:,0], entrada_normalizada[:,1], color='r')

#plt.xlim(-5, 10)   # set the ylim to ymin, ymax
#plt.ylim(-5, 10)     # set the ylim to ymin, ymax
plt.axis((-5, 10, -5, 10))
plt.show()
```

Ademas, linear decorrelation/whitening/pca helps a lot.

## Referencias:
Punto 4.3 de [Efficient BackProp](http://yann.lecun.com/exdb/publis/pdf/lecun-98b.pdf)
