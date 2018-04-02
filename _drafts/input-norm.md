---
title: Input normalization
---


para datasets grandes y variados
la gente calcula la media (mean) y desviacion standard (std)
y normalizan (img - MEAN) / STD


Pasarle los input a pelo a la red puede ser una mala idea, ya que la red convergerá más ráppido si le pasamos **una entrada con valores cercanos a cero**
