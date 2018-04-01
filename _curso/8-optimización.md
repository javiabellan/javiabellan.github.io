---
title: "Optimización"
---

Desafortunadamente, nuestros ordenadores tienen una capacidad de cómputo limitada.
Por lo tanto es necesario necesario usar algunos truquillos para aligerar la cosa.
En este capítulo veremos como podemos hacer el proceso de **entrenamiento más rápido**.


* Stochastic Gradient Descent
* Momentum
* Nesterov Momentum
* Inicialización de parámetros
* Cambiar el lerning rate
  * AdaGrad
  * RMSProp
  * [Adam](https://arxiv.org/abs/1412.6980)
  * Choosing the Right Optimization Algorithm
* Approximación de segundo orden
  * Método de Newtown
  * Conjugate Gradients
  * BFGS
* Otras estrategias
  * Batch Normalization
  * Coordinate Descent
  * Polyak Averaging
  * Supervised Pretraining

* ReLU


# 8.1 Batch

Los problemas de optimización usan todo el conjunto de entrenamiento (**batch**) para actualizar una función de error. Pero podemos conseguir también buenos resultados si solo usamos parte (**minibatch**), y así nos ahorraremos tiempo de computación. El otro extremo sería usar solo 1 muestra (stochastic). Lo normal es usar un minibatch (de 100 más o menos).

| Batch              | Stochastic | Minibatch  |
|--------------------|------------|------------|
| Todas las muestras | 1 muestra  | N muestras |

> Consejo:
>
> Si usas stochastic, o un minibatch muy pequeño, acuerdate de poner un learning rate pequeño
> para compensar la alta variazanza que tienen tus mustras.

> Ojo!
>
> La mayoría de frameworks aprovechan para calcular cada muestra del batch en paralelo, esto supene una limitiación para poner batches muy altos porque no caben en memoria.




### Stochastic gradient descent (SGD)
Se actualiza el modelo por cada muestra que ve (batchSize=1)

### Batch gradient descent
Se ven todos los datos, pero solo se actuliza el modelo al final de la epoch (batchSize=todo)

### Mini-batch gradient descent
Se cogen solo un grupo de muestras (batch) y se actualiza el modelo cuando se han visto esas muestras (batchSize=parte).

Se hacen varias interaciones por cada batch hasta que se vean todas las mustras (completar una epoch).
el tamaño del últomo bach creo que debe ser mas pequeño para poder así compleatar la epoch.

## Referencias

* [un blog](https://blog.acolyer.org/2017/03/01/optimisation-and-training-techniques-for-deep-learning/)
* [Adam](https://machinelearningmastery.com/adam-optimization-algorithm-for-deep-learning/)
