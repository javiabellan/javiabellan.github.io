---
title: "Perceptrón"
---

Las neuronas de nuestro cerebro son las responsables de nuestra inteligencia, una nerona por si sola no es capaz de mucho pero cuando se conectan muchas, unas con otras, es cuando la magia de la inteligencia aparece.

---

Las neronas son células nerviosas que están conectadas unas con otras y se cominican entre ellas a traves de impulsos elécctricos.

Cuando una neurona recive un impulso electrico por alguno de sus sensores emite otro impulso electrico como respesta de salida.

Los sensores de la neurona se llaman dentritas, y la salida que emite impulsos electricos se llama axon, por lo tanto para que una neurona reciva impulsos elctricos por sus dentritas debe estar conectado al axón de otra neurona

Piensa en las neuronas como gente haciendo la ola. Cuando alguien al lado tuyo levanta las manos (que sería el impulso electrico) a tí te toca levantar las manos también, es como si parasra un mensaje.

Losimpulsos nerviosos viajan por toda la neurona comenzando por las dendritas hasta llegar al final del axon, que se pueden conectar con otra neurona, fibras musculares o glándulas. La conexión entre una neurona y otra se denomina sinapsis.

Las neuronas pueden recibir por las dentritas muchos impulsos electricos pero solo cuande reciba un impluso lo suficientemete grande la neurona se activará y emitira su impulso por su axón esto es lo que se conoce como potencial de acción.

Por lo tanto resumiendo una neurona tiene dos partes: Unas entradas 

Neurona matemática
---

(plano medio)

Ahora que conocemos como funcionan las neuronas podemos hacer nuestra propia neurona. Las dentritas serán las entradas y el axon será la salida. Y los impulsos electricos que viajan los representaremos con un número entre 0 y 1. 0 significa que no hay impulso electrico y 1 que si hay. Si tenemos un numero como 0,2 significa que tenemos un impulso muy debil. Vamos a ver como represnetaríamos nuestra neurona

(modo animacion)

Cada entrada de la neurona podra recibir algun número que representa un poquito de información, como nuestra neurona es inteligente sabrá distiguir que entradas de iformación son importantes y cuales son poco relevanes, esta evaluacón la haremos con otro número llamado peso que multiplica el valor de entrada para hacerlo más o menos impornante, finalemte todos estos valores llegan al centro de la neurona donde se juntan, esto lo representaremos con una suma, y finalemte toca saber si debemos emitir el impulso electrico o no, es decir si la suma que obtenemos es muy pequeña no mandaremos ninguna señal pero si la suma es grande si emitiremos la señal esto lo representarmos con una función que diga si la suma es pequeña la salida es cero pero si la suma es grande la salida es 1. Y ya tendríamos nuestra neurona inteligente.

Y esta neurona sola, ya sería capaz de reconcer cosas es decir, es capaz de recibir informacion por las entradas y contestar si o no.

Por ejemplo podriamos hecer una neurona capaz saber si lloverá dentro de un rato o no, con la información que le llega como llovió ayer, hay nubes, hace sol, cuanto hay de presión atmosférica, etc.

Si podemos hacer todo esto con una neurona, imaginaros toda la inteligencia que tendríamos cuando conectásemos muchas nueronas. Así que os animo a ver el siguiente video sobre redes neuronales!! 


Explicación matemática
---

Antes de irme, La neurona que acabo de explicar se llama perceptrón y es un clasificador bastante simple para decidir segun la impfrmacion que tengamos activar o no una salida. La definición matemática es

$$Perceptrón(x)=\sigma \bigg(b+\sum_{i=0}^n x_i w_i \bigg)$$

Por lo tanto tenemos que ajustar los pesos para que la nuerona sea inteligente, este proceso de dar con los pesos adecuados se conoce como entrenamiento

El problema del percptrón es que es un clasificador LINEAL esto quiere decir si tenemos dos entradas la clasificación será una línea para separar el sí del no, y si tenemos tres entradas será un plano, y si tenemos mas de tres entradas no podemos representrslo pero sería un hiperplano, es decir que seguiíra siendo lineal, No podremos hacer divisiones más complejas, y significa que las clasificaciones son muy simples

Concetando las salidas de nueronas con las entradas de otras neurona resolvemos este problema y es lo que se conoce como red neuronal. Que te las explico en el siguiente video. Hasta pronto!
