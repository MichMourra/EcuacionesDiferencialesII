# Ecuaciones diferenciales II

# Clase I

## Primer repaso

### Eigen valores y eigen vectores

Repasaremos 2 temas:

1. Eigen valores y Eigen vectores
2. Solución de sistemas de ecuaciones

Estos dos temas seran utilizados para resolver ecuaciones diferenciales.

Los eigen vectores, también se llaman vectores característicos.

**¿Qué son los eigen vectores y eigen valores?**

Suponiendo que tenemos una matriz "M", entonces esa matriz actúa como una transformación. Es decir, si esa matriz la multiplico por un vector, voy a obtener otro vector. Por lo que lo transforma

**Ejemplo**

- El numero de columnas de la matriz debe coincidir con el numero de renglones del vector. 
- El efecto de la matriz sobre el vector es que lo transforma en un vector nuevo.

$$
\left( \begin{equation} \begin{matrix} 2 & 3\\ 3 & -6 \end{matrix} \end{equation} \right) \cdot \begin{pmatrix}x\\ y\end{pmatrix} = \begin{pmatrix}2x + 3y\\ 3x - 6y\end{pmatrix}
$$

- También puede haber escalares que actúan sobre un vector, estos escalares están denotados por la letra lambda.

$$
\lambda \overline{X} = 3 \cdot \begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}3x\\3y\end{pmatrix}
$$

- Los vectores se pueden transformar al ser multiplicados por una matriz o por una constante.

- Los eigen vectores son vectores especiales a los cuales transforma una matriz y se obtiene el mismo resultado que si se multiplicara por una constante.



- Si yo tengo una matriz M, entonces se cumple la siguiente propiedad.

$$
M \overline{X} = \lambda \overline{X} = \lambda I \overline{X}
$$

- Debemos resolver esta ecuación ya que queremos encontrar los eigen vectores $\overline{X}$ y los eigen valores $\lambda$ que hagan posible que la accion de la matriz de el mismo resultado que multiplicar por una constante.

Resolvemos:

$M\overline{X} - \lambda I\overline{X} = 0$

Queremos encontrar la lambda y la x que hacen posible esta expresión

$(M - \lambda I)\overline{X} = 0$

Una solución trivial es que la x valga 0, por lo que esta solución no aporta ninguna información.

- Para encontrar soluciones no triviales debemos calcular el determinante, ya que si este es igual a 0 entonce podemos buscar los eigen vectores y eigen valores.

Se tiene que cumplir que:

$\det (M - \lambda I) = 0$ 

Ya que si el determinante es diferente de 0, significa que no es una solución única.

**Ejemplo**
$$
M = \left( \begin{matrix} 2 & 3\\ 3 & -6 \end{matrix} \right) \\
\det (M - \lambda I) = \left( \left( \begin{matrix} 2 & 3\\ 3 & -6 \end{matrix} \right) - \lambda(I) \right) = 0\\
\det \left( \left(  \begin{matrix} 2 & 3\\ 3 & -6 \end{matrix} \right) - \lambda \left(  \begin{matrix} 1 & 0\\ 0 & 1 \end{matrix} \right)\right) = \left(  \begin{matrix} 2 - \lambda & 3\\ 3 & -6-\lambda \end{matrix} \right) = 0
$$
**Resolvemos el determinante**
$$
(2 - \lambda)(-6-\lambda)  - 9 = 0\\
-12 - 2\lambda + 6\lambda + \lambda^2 - 9 = 0 \\
\lambda^2 + 4\lambda - 21 = 0\\
(\lambda + 7)(\lambda - 3) = 0\\
$$
**Eigen valores**

$\lambda = -7\\ \lambda = 3$

Ahora tenemos que encontrar los eigen vectores:
$$
Si \ \ \lambda = -7:\\
\left(  \begin{matrix} 2 - (-7) & 3\\ 3 & -6- (-7) \end{matrix} \right) = \left(  \begin{matrix} 9 & 3 & | & 0\\ 3 & 1 & | & 0 \end{matrix} \right)\\
\left(  \begin{matrix} 9 & 3 & | & 0\\ 3 & 1 & | & 0 \end{matrix} \right) = \left(  \begin{matrix} 3 & 1 & | & 0\\ 3 & 1 & | & 0 \end{matrix} \right) = \left(  \begin{matrix} 3 & 1 & | & 0\\ 0 & 0 & | & 0 \end{matrix} \right)
$$
Esto quiere decir que:

$3x + y = 0$

$-3x = y$

Entonces nuestro eigen vector es:

$\begin{pmatrix}c_1\\-3c_1\end{pmatrix}$

Ahora debemos obtener nuestro otro eigen vector con $\lambda = 3$
$$
Si \ \ \lambda = 3:\\
\left(  \begin{matrix} 2 - (3) & 3\\ 3 & -6- (3) \end{matrix} \right) = \left(  \begin{matrix} -1 & 3 & | & 0\\ 3 & -9 & | & 0 \end{matrix} \right)\\
\left(  \begin{matrix} -1 & 3 & | & 0\\ 3 & -9 & | & 0 \end{matrix} \right) = \left(  \begin{matrix} -1 & 1 & | & 0\\ 3 & -3 & | & 0 \end{matrix} \right) = \left(  \begin{matrix} -1 & 3 & | & 0\\ 0 & 0 & | & 0 \end{matrix} \right)
$$
Entonces tenemos que:

$-x + 3y = 0$

$3y = x$

Eigen vector:

$\begin{pmatrix}3c_2\\c_2\end{pmatrix}$



## Segundo paso

### Resolución de sistemas de ecuaciones diferenciales

$$
\frac{dx}{dt} -2x - 3y = 0\\
\frac{dy}{dt} - 3x + 6y = 0
$$

Esto se resolvia con un operador diferencial, es decir en lugar de poner la diferencial se ponia una D.

$D = \frac{d}{dt}$

Por lo que podemos reescribirlo de la siguiente manera:
$$
Dx - 2x - 3y = 0\\
Dy - 3x + 6y = 0
$$
Por lo que factorizando:
$$
(D-2)x - 3y = 0\\
-3x + (D+6)y = 0
$$
Resolvemos multiplicando por 3 la expresión de arriba para desaparecer las x y el de abajo por D - 2.
$$
3 (D-2)x - 9y = 0\\
-3(D-2)x + (D+6)(D-2)y = 0
$$
Eliminamos y tenemos la expresión final:

$\left( (D+6)(D-2)-9\right)y = 0$

$\left( D^2 + 4D  - 21\right)y = 0$

$D^2 + 4D - 21 = 0$

$(D + 7)(D - 3) = 0$

$D = -7 \ \ \ \ D = 3$

$y = C_1e^{-7t} + C_2e^{3t}$

Ya tenemos el valor de la y, ahora debemos obtener el valor de la x.

$\frac{dy}{dt} = -7C_1e^{-7t} + 3C_2e^{3t}$

Derivamos debido a que haremos un despeje de la ecuación inicial para obtener la x.

$3x = -7C_1e^{-7t} + 3C_2e^{3t} + 6 \cdot (C_1e^{-7t} + C_2e^{3t})$

$3x = -7C_1e^{-7t} + 3C_2e^{3t} + 6C_1e^{-7t} + 6C_2e^{3t}$

$3x = -C_1e^{-7t} + 9C_2e^{3t}$

Resultado de x:

$x = \frac{-1}{3}C_1e^{-7t} + 3C_2e^{3t}$



Con esto ya tenemos una solución:

- $x = \frac{-1}{3}C_1e^{-7t} + 3C_2e^{3t}$
- $y = C_1e^{-7t} + C_2e^{3t}$

Invertimos los signos de las ecuaciones originales y las igualamos al operador diferencial. Esto lo logramos con un despeje:
$$
Dx = 2x + 3y\\
Dy = 3x - 6y
$$
De este modo lo podemos ver como el producto de la multiplicación de un vector por una matriz:
$$
D\begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}2 & 3\\3 & -6\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix}
$$
Esto quiere decir que las ecuaciones diferenciales siempre las puedo escribir como el producto de una matriz
$$
\begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}-\frac{1}{3}C_1 & 3 C_2\\C_1 & C_2\end{pmatrix}\begin{pmatrix}e^{-7t}\\e^{3t}\end{pmatrix}
$$

## Ejemplo

1. 

- $\frac{dx}{dt} = 2x + 3y$

- $\frac{dy}{dt} = 2x + y$

**Respuesta**
$$
D \begin{pmatrix}x\\y\end{pmatrix} = \begin{pmatrix}2 & 3\\2 & 1\end{pmatrix} \begin{pmatrix}x\\y\end{pmatrix}\\
\det \begin{pmatrix}2 - \lambda & 3\\2 & 1 - \lambda\end{pmatrix} = 0\\
(2 - \lambda)(1 - \lambda) - 6 = 2 - 2\lambda - \lambda + \lambda^2 = 6\\
\lambda^2 - 3 \lambda - 4 = 0\\
(\lambda - 4)(\lambda + 1) = 0\\
\lambda = 4 \ \ \ \lambda = 1
$$
**Obtenemos los eigen vectores**
$$
si \ \ \ \lambda = 4 \\
\begin{pmatrix}-2 & 3 & | & 0\\3 & -3 & | & 0\end{pmatrix} = \begin{pmatrix}-2 & 3 & | & 0\\0 & 0 & | & 0\end{pmatrix}
$$
Entonces:

$-2x + 3y = 0$

$2x = 3y$

$x = \frac{3}{2}y$
$$
\lambda = - 1 \begin{pmatrix}3 & 3 & | & 0\\2 & 2 & | & 0\end{pmatrix} = \begin{pmatrix}1 & 1 & | & 0\\1 & 1 & | & 0\end{pmatrix} = \begin{pmatrix}1 & 1 & | & 0\\0 & 0 & | & 0\end{pmatrix}
$$
$x + y = 0$

$x = - y$
$$
\begin{pmatrix}x \\y \end{pmatrix} = \begin{pmatrix} \frac{3}{2}C_1 & -C_2 \\C_1 & C_2 \end{pmatrix}\begin{pmatrix}e^{4t} \\e^{-t} \end{pmatrix}
$$
**Solución por multiplicación de matrices**

$x = \frac{3}{2}C_1e^{4t} - C_2e^{-t}$

$y = C_1e^{4t} + C_2e^{-t}$



## Ejercicio Final

- $\frac{dx}{dt} = 3x - 2y$
- $\frac{dy}{dt} = x$

