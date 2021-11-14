# Clase 2 - 16 de agosto 

# Sistemas de ecuaciones 3x3

## Recapitulando la clase pasada

Si tenemos el siguiente sistema:

- $\frac{dx}{dt} = 3x + 2y$
- $\frac{dy}{dt} = 3x + 8y$

Esto lo podemos ver como un sistema de matrices:
$$
D \begin{pmatrix} x\\ y \end{pmatrix} = \begin{pmatrix} 3 & 2\\ 3 & 8 \end{pmatrix} \begin{pmatrix} x\\ y \end{pmatrix}\\
Entonces:\\
\lambda \overline{X} = M \overline{X}\\
Obtenemos \ \ EigenValores:\\
\begin{pmatrix} 3-\lambda & 2\\ 3 & 8-\lambda \end{pmatrix}\\
M \overline{X} - \lambda I \overline{X} = 0\\
(M - \lambda I) \overline{X} = 0\\
Formula \ \ determinante:\\
(3 - \lambda)(8 - \lambda) - 6 = 0\\
24 - 3\lambda - 8 \lambda + \lambda^2 - 6 = 0\\
\lambda^2 - 11\lambda + 18 = 0\\
(\lambda - 9)(\lambda - 2) = 0\\
Eigenvalores:\\
\lambda = 9 \ \ \ \ \lambda = 2
$$
**Obtenemos Eigenvectores**
$$
Si \ \ \lambda = 9:\\
\begin{pmatrix} 3-9 & 2\\ 3 & 8-9 \end{pmatrix} = \begin{pmatrix} -6 & 2\\ 3 & -1 \end{pmatrix} = \begin{pmatrix} -3 & 1 & | & 0\\ 3 & -1 & | & 0\end{pmatrix} =  \begin{pmatrix} -3 & 1 & | & 0\\ 0 & 0 & | & 0\end{pmatrix}\\
$$
Entonces:

$-3x + y = 0$

$y = 3x$

**Eigenvector**

$ \begin{pmatrix} C_1 \\ 3C_1 \end{pmatrix}$

### Lo hacemos para el otro eigen valor

$$
Si \ \ \lambda = 2:\\
\begin{pmatrix} 3-2 & 2\\ 3 & 8-2 \end{pmatrix} = \begin{pmatrix} 1 & 2\\ 3 & 6 \end{pmatrix} = \begin{pmatrix} 1 & 2 & | & 0\\ 1 & 2 & | & 0\end{pmatrix} =  \begin{pmatrix} 1 & 2 & | & 0\\ 0 & 0 & | & 0\end{pmatrix}\\
$$

Entonces:

$x + 2y = 0$

$x = -2y$

**Eigenvector**

$\begin{pmatrix} -2C_1 \\ C_1 \end{pmatrix}$



**Solución**
$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} C_1 & -2C_2 \\ 3C_1 & C_2 \end{pmatrix}\begin{pmatrix} e^{9t} \\ e^{2t} \end{pmatrix}
$$


## Tema de hoy



Podemos ver un caso como el problema de los depósitos de los tinacos en donde se pasa agua de un lado a otro de tal manera que lo podemos modelar con ecuaciones diferenciales.

- También se puede modelar con matrices 3x3

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

# Ejercicio

$$
d\begin{pmatrix} x \\ y \\ z\end{pmatrix} = \begin{pmatrix} 1 & -2 & 2 \\ -2 & 1 & -2 \\ 2 & -2 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix}
$$

**Respuesta**

Obtenemos el determinante
$$
\det \begin{pmatrix} 1 - \lambda & -2 & 2 \\ -2 & 1 - \lambda & -2 \\ 2 & -2 & 1 - \lambda \\ 1 - \lambda & -2 & 2\\ -2 & 1 - \lambda & -2 \end{pmatrix} = 0
$$
$(1 - \lambda)^3 + 8 + 8 - (4 -(1 -\lambda) + 4(1 - \lambda) + 4(1 - \lambda)) = $

Simplificado queda como:

$(1 - \lambda)^3 + 16 - 12(1 - \lambda) = 0$

Factorizamos el cubo:

$(1 - \lambda)^2(1 - \lambda) + 16 - 12(1 - \lambda) = 0$

$1 - 3 \lambda + 3 \lambda^2 - \lambda^3 - 12 + 12\lambda + 16 = 0$

$\lambda^3 - 3\lambda^2 - 9\lambda - 5 = 0$

Obtenemos las raíces de la expresión cubica:

|      | 1    | -3   | -9   | -5   |
| ---- | ---- | ---- | ---- | ---- |
| 5    | 1    | 2    | 1    | 0    |
| -1   | 1    | 1    | 0    |      |
| -1   | 1    | 0    |      |      |
|      |      |      |      |      |

**Eigenvalores**

$\lambda = 5 \ \ \ \ \lambda = - 1$

Hay una lambda repetida, por lo que nosotros habíamos visto que cuando tenemos raíces de multiplicidad 2 será $te^{-t}$ en lugar de $e^{-t}$

Por este motivo las tres soluciones serán:

- $e^{5t}$
- $e^{-t}$
- $te^{-t}$

Ahora a partir de la matriz inicial debemos encontrar los eigenvectores:
$$
\begin{pmatrix} 1 - \lambda & -2 & 2 \\ -2 & 1 - \lambda & -2 \\ 2 & -2 & 1 - \lambda  \end{pmatrix} = \begin{pmatrix} 2  & -2 & 2 & | & 0 \\ -2 & 2 & -2 & | & 0 \\ 2 & -2 & 2 & | & 0  \end{pmatrix} = \\
$$

$$
\begin{pmatrix} 1  & -1 & 1 & | & 0 \\ -1 & 1 & -1 & | & 0 \\ 1 & -1 & 1 & | & 0  \end{pmatrix} = \begin{pmatrix} 1  & -1 & 1 & | & 0 \\ 0 & 0 & 0 & | & 0 \\ 0 & 0 & 0 & | & 0  \end{pmatrix}
$$

$x - y + z = 0$

Nos quedan dos eigenvectores diferentes para las multiplicidades:
$$
\begin{pmatrix} 0  \\ C_2 \\ C_2 \end{pmatrix} \begin{pmatrix} C_3 \\ C_3 \\ 0 \end{pmatrix}
$$
**Resultado**
$$
5 \begin{pmatrix} C_1  \\ -C_1 \\ C_1 \end{pmatrix} - 1 \begin{pmatrix} 0  \\ C_2 \\ C_2 \end{pmatrix} \begin{pmatrix} C_3  \\ C_3 \\ 0 \end{pmatrix}
$$

$$
\begin{pmatrix} x  \\ y \\ z \end{pmatrix} = \begin{pmatrix} C_1  & 0 & C_3\\ -C_1 & C_2 & C_3 \\ C_1 & C_2 & 0 \end{pmatrix} \begin{pmatrix} e^{5t}  \\ e^{-t} \\ te^{-t} \end{pmatrix}
$$

**Solución**

$x = C_1e^{5t} + C_3te^{-t}$

$y = -C_1e^{5t} + C_2e^{-t} + C_3te^{-t}$

$z = C_1 e^{5t} + C_2e^{-t}$

