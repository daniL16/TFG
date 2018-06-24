Buenos días, soy Daniel López y voy a presentar mi trabajo "Distribución de puntos en la esfera.Competición en Kaggle."
Como se puede apreciar el trabajo consta de 2 partes, la primera de ellas, la matemática, en la que estudiaremos la obtención de distribuciones de puntos sobre la esfera que nos proporcionan buenas propiedades geométricas para aproximación. La segunda parte es la parte informática, en la que describiremos el proceso seguido durante la participación en una competición de machine learning en la plataforma Kaggle.

#Distribucion de puntos en la esfera.

## Objetivos

En esta parte, queremos determinar conjuntos de puntos sobre la esfera, que tengan buenas propiedades para interpolación,aproximación e integración sobre la esfera. La utilidad de esto reside en,...
Finalmente, realizaremos una visualización de los puntos obtenidos en el caso particular de dimensión 3.

En primer lugar, vamos a construir el espacio de polinomios armónicos esféricos. A continución obtendremos el gradiente de dichos polinomios y calcularemos sus puntos críticos. Finalmente, veremos un resultado de integración numérica del que podremos deducir que el conjunto de puntos obtenido ofrece las propiedades que buscamos.

## Esféricos Armónicos.
Para construir el espacio de armónicos esféricos necesitaremos algunas definiciones.

Vamos a considerar el espacio de los polinomios homogeneos de grado n en d dimensiones. Cabe recordar, que un polinomio homogéneo es un polinomio en que cada uno de sus términos (monomios) tienen el mismo grado; o sus elementos son de la misma dimensión. Aquí se pueden ver algunos ejemplos.

Por otro lado, se dice que una función es armónica si tiene derivadas parciales continuas de primer y segundo orden y satisfacen la ecuación de Laplace. Es decir, la suma de sus parciales de segundo orden es nula.

Uniendo estos conceptos, definimos Y_n(Rd) como el espacio de los polinomios homogeneos de grado n en Rd que son armónicos.

Finalmente, definimos el espacio de armonicos como la restriccion a la esfera del espacio Y_n.

Una vez construido el espacio el siguiente teorema nos da una base ortogonal del espacio.

##Calculo del gradiente en dimensión 3

Suponemos ahora el caso particular de dimensión tres. Tomando d=3 en la expresión anterior y realizando el cambio a coordenadas polares, obtenemos la siguiente base ortogonal del espacio.

Derivando respecto a x1,x2,x3 obtenemos la siguiente expresion de las parciales.
Ahora queremos, obtener los puntos que anulan el gradiente.Es decir, los puntos que anulan simultaneamente estas expresiones. Para ello igualamos a 0 estas expresiones, y obtenemos que debe de verificarse alguna de estas condiciones. De la  primera se obtienen el polo sur y el polo norte de la esfera. 
%aqui hay que meter bien las condiciones

Ahora os voy a mostrar una simulación que hemos realizado para mostrar los puntos que se obtienen. Vamos a tomar el espacio de grado 20 y vamos a ver los puntos que se obtienen para los distintos k (k=0,...,19).

##Integracion numerica

Finalmente, vamos a obtener un resultado sobre integración numérica. Suponiendo el caso anterior tenemos N nodos(puntos obtenidos) y una funcion f, y los valores aproximados de cada nodo. Queremos obtener la siguente intregral. Para ello haremos uso de tecnicas de integracion numerica. Así tomando una triangulación de el valor de la integral es el siguiente. Una vez obtenida, la aproximacion de la integral queremos saber cuan buena es, para ello nos valemos del siguiete resultado. Podemos observar que el error cometido en la aproximacion depende principalmente del conjunto de nodos. Es conocido que se obtienen buenos resultados tomando un conjunto en el que los puntos están bien distribuidos. Por tanto, como hemos podido observar en la simulación anterior los puntos que obtenemos tienen una buena distribución luego darán lugar a una buena aproximación de esta integral.

Punto pelota
