# Clase 2 - 16 de agosto 

# Sístemas de ecuaciones 3x3



Podemos ver un caso como el problema de los depositos de los tinacos en donde se pasa agua de un lado a otro de tal manera que lo podemos modelar con ecuaciones diferenciales.

## Ejemplo

$$
\frac{dx}{dt} = -4x + y + z \\
\frac{dy}{dt} = x + 5y - z \\
\frac{dz}{dt} = y-z\\
$$

Transformamos todo a vectores y matrices:
$$
\lambda \begin{pmatrix} x\\ y \\ z \end{pmatrix} = \begin{pmatrix}-4 & 1 & 1\\ 1 &5 &-1\\ 0 & 1 & -3\end{pmatrix}
$$

## Obtención de eigen valores

Obtenemos el determinante multiplicando las diagonales:
$$
det = \begin{pmatrix}(-4 -\lambda) & 1 & 1\\ 1 & (5 - \lambda) &-1\\ 0 & 1 & (-3 -\lambda) \\ (-4 - \lambda) & 1 & 1 \\ 1 & (5-\lambda) & 1\end{pmatrix}
$$
Sabemos que:
$$
\lambda \overline{X} = M\overline{X} \\
M\overline{X} - \lambda I \overline{X} = \overline{0} \\
(M - \lambda I)\overline{X} = \overline{0}
$$
Para obtener el determinante multiplicamos y sumamos las diagonales en cada lado y las restamos entre si:
$$
\left[(-4 - \lambda)(5 - \lambda)(-3 - \lambda) + 1 + 0 \right] - \\ \left[1 \cdot (-4 - \lambda)(5 - \lambda) + -1 + (-3 - \lambda) \cdot 1 \cdot 1 + 1 + 0 \right] = 0
$$


Tras el procedimiento para obtener el determinante nos queda la siguiente ecuación:
$$
\lambda^3 + 2 \lambda^2 - 23\lambda - 60 = 0
$$

|      | 1    | 2    | -23  | -60  |
| ---- | ---- | ---- | ---- | ---- |
| -4   | 1    | -2   | -15  | 0    |
| 5    | 1    | 3    | 0    |      |
| -3   | 1    | 0    |      |      |
|      |      |      |      |      |

Los eigen valores obtenidos fueron : -4,5,-3

## Primer eigen vector

Entonces ahora debemos generar los eigen vectores:
$$
\begin{pmatrix}(-4-(-4)) & 1 & 1\\ 1 & (5 -(-4)) &-1\\ 0 & 1 & (-3-(-4))\end{pmatrix}
$$
Entonces:
$$
\begin{pmatrix} 0 & 1 & 1 &| & 0\\ 1 & 9 &-1 &| & 0\\ 0 & 1 & 1 &| & 0\end{pmatrix}
$$
Podemos formar las ecuaciones:
$$
y + z = 0 \\
y = -z\\
Sustituimos \ \ y  \ \ por \ \ z\\
x - 9z -z = 0 \\
x - 9C_1 - C_1 = 0 \\
x-10z = 0 \\
x = 10z \\
x = 10C_1
$$


Gracias a esto podemos obtener el primer eigen vector:
$$
\begin{pmatrix} 10C_1\\ -C_1 \\ C_1 \end{pmatrix}
$$

## Segundo eigen vector

$$
\begin{pmatrix}(-4-(5)) & 1 & 1\\ 1 & (5 -(5)) &-1\\ 0 & 1 & (-3-(5))\end{pmatrix}
$$

La matriz queda:
$$
\begin{pmatrix} -9 & 1 & 1 &| & 0\\ 1 & 0 &-1 &| & 0\\ 0 & 1 & -8 &| & 0\end{pmatrix}
$$
Teniendo nuestras ecuaciones sabemos que:
$$
x - z = 0 \\
por \ lo \ tanto: \\
x = z \\
entonces: \\
y - 8z = 0 \\
y = 8z \\

ademas\\

-9x + y + z = 0 \\
-9x + 8z + z = 0 \\
-9x + 9z = 0 \\
-9z = -9x \\
x = z
$$
Por lo que nuestro eigen vector queda:
$$
\begin{pmatrix} C_2\\ 8C_2 \\ C_2 \end{pmatrix}
$$


## Tercer eigen vector

$$
\begin{pmatrix}(-4-(-3)) & 1 & 1\\ 1 & (5 -(-3)) &-1\\ 0 & 1 & (-3-(-3))\end{pmatrix}
$$

Entonces:
$$
\begin{pmatrix} -1 & 1 & 1 &| & 0\\ 1 & 8 &-1 &| & 0\\ 0 & 1 & 0 &| & 0\end{pmatrix}
$$
Obtenemos las ecuaciones 
$$
y = 0 \\ 
-x + 0 + z = 0 \\
x = z
$$
Ya que obtuvimos los tres valores formamos nuestro terecer eigen vector
$$
\begin{pmatrix} C_3\\ 0 \\ C_3 \end{pmatrix}
$$

## Resolución

$$
-4 \begin{pmatrix} 10C_1\\ -C_1 \\ C_1 \end{pmatrix} \ \ 5 \begin{pmatrix} C_2\\ 8C_2 \\ C_2 \end{pmatrix} \ \  -3 \begin{pmatrix} C_3\\ 0 \\ C_3 \end{pmatrix}
$$

Acomodamos nuestros eigen vectores en una matriz:
$$
\begin{pmatrix} x\\ y \\ z \end{pmatrix} = \begin{pmatrix} 10C_1 & C_2 & C_3\\ -C_1 & 8C_2 & 0 \\ C_1 & C_2 & C_3 \end{pmatrix}\begin{pmatrix} e^{-4t}\\ e^{5t} \\ e^{-3t} \end{pmatrix}
$$
Ahora finalmente podemos obtener las ecuaciones que describen cada una de nuestras variables:
$$
x = 10C_1e^{-4t} + C_2e^{5t} + C_3e^{-3t} \\
y = -C_1e^{-4t} + 8C_2e^{5t} \\
z = C_1e^{-4t} + C_2e^{5t} + C_3e^{-3t}
$$
Cosas como $x - y + z = 0$ suelen ocurrir cuando una de los eigen valores esta repetido.