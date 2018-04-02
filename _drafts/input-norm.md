---
title: Input normalization
---





Pasarle los input a pelo a la red puede ser una mala idea, ya que la red convergerá más ráppido si le pasamos **una entrada con valores cercanos a cero**

Normalmente, para datasets grandes y variados, la gente calcula la media (mean) y desviacion standard (std)
y normalizan `(img - MEAN) / STD`.


```python
import numpy as np
import matplotlib.pyplot as plt

entrada = np.random.uniform(low=0, high=10, size=(32,2))

entrada_normalizada = (entrada - entrada.mean()) / entrada.std()



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
