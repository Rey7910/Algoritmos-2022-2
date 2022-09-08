# Bisection Root Search

-----
El siguiente algoritmo implementa la búsqueda de raíces por bisección en el lenguaje Python y se presenta en un Jupiter Notebook.





## Cálculo de la complejidad
----

Para la ejecución, este algoritmo depende del intervalo [a, b] y δ, puesto que se va a obtener una raíz x±δ en el intervalo.
Luego, la única operación que se realiza es reducir el intervalo dado, entonces encontrar la respuesta b<sub>f</sub> - a<sub>f</sub> ≤ δ, esto se obtiene dividiendo repetidamente el intervalo en dos partes iguales, por lo que se puede asegurar que se realizaran iteraciones en función del intervalo inicial y un número k de iteraciones expresadasa como:

![\Small \delta\le\frac{b-a}{2^k}](https://latex.codecogs.com/svg.latex?\Large&space;\delta\le\frac{b-a}{2^k}) 

Entonces, se puede desarrollar de la siguiente forma

![\Small \delta\le\frac{b-a}{2^k}](https://latex.codecogs.com/svg.latex?\Large&space;\delta<\frac{b-a}{2^k}) 

![\Small \delta\le\frac{b-a}{2^k}](https://latex.codecogs.com/svg.latex?\Large&space;2^k<\frac{b-a}{\delta})


![\Small \delta\le\frac{b-a}{2^k}](https://latex.codecogs.com/svg.latex?\Large&space;k<\log_2\frac{b-a}{\delta})


De esta forma, se demuestra que k está acotado por arriba por los parametros de la función y que esta tiene complejidad logarítmica en relación con el intervalo y el inverso de la tolerancia. 

Se demuestra entonces que esta función es de orden _Log(n)_.


### Algunas gráficas sobre el algoritmo
----

En el Jupyter Notebook adjunto se pueden ver algunas gráficas de interés sobre el algortimo, como la variación del tiempo en función del tamaño del intervalo y la variación del tiempo en función de la tolerancia.
