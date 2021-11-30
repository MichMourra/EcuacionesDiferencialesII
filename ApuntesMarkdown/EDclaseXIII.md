# Ejercicios de transformadas de Laplace





1. 

$$
\frac{dy}{dt} + 4y = e^{-4t}\\
y(0) = 2
$$

**Solución**

Debemos pasarle a una función de variable s con la transformada de Laplace.

$L \{  f \} = F$

$L \{ y \} = Y$

$L \{ x \} = X$

Sabemos que la transformada de Laplace es de la siguiente forma:

$L \{ f (t)\} = \int e^{-st} f(x) dt$

- Primero debemos sacar la transformada de la segunda derivada

- La transformada de la derivada es:

$sy - 2 + 4y = \frac{1}{s+4}$

En términos de resolver una ecuación diferencial esta ya esta resuelta, únicamente debemos sustituir y despejar.

$sy + 4y = 2 + \frac{1}{s + 4}$

$(s + 4) y = 2 + \frac{1}{s + 4}$

$y = \frac{2}{s+4} + \frac{1}{(s + 4)^{2}}$

**Resultado final**

$y = 2e^{-4t} + te^{-4t}$



2. 

$$
\frac{d^{2}y}{dt^2} + 2\frac{dy}{dt} + y = 0\\
y(0) = 1\\
\frac{dy}{dt}(0) = 1
$$

- Para resolver este ejercicio necesitamos obtener la transformación de la segunda derivada:

$$
s^2y - s - 1 + 2sy - 2 + y = 0\\
(s^2 + 2s + 1) y = s + 3\\
(s + 1)^2 y = s + 3\\
y = \frac{s + 1 - 1}{(s + 1)^2} + \frac{3}{(s + 1)^2} = \frac{s + 1}{(s+1)^2} - \frac{1}{(s+1)^2} + \frac{3}{(s+1)^2}\\
$$





3. 

$$
\frac{d^2y}{dt^2} - 6\frac{dy}{dt} + 13y = 0\\
y(0) = 0\\
\frac{dy}{dt}(0) = -3
$$

**Solución**

- Usamos la formula 18 de las transformadas de Laplace

$$
s^2Y + 3 - 6sY + 13Y = 0\\
(s^2 - 6s + 13)Y = -3\\
Y = \frac{-3}{s^2 - 6s + 13}\\
y = \frac{-3}{(s-3)^2 + 4} = \frac{-3}{2} \frac{2}{(s-3)^2 + 4}\\
y = \frac{-3}{2} \left( e^{st} \sin 2t\right)
$$

## Sistemas de ecuaciones con transformadas de Laplace

**Ejemplo**

En este caso utilizaremos las transformadas de Laplace para resolver sistemas de ecuaciones diferenciales.
$$
\frac{d^2x}{dt^2} + 10x - 4y = 0\\
-4x + \frac{d^2y}{dt^2} + 4y = 0\\
x(0) = 0 \ \ \ \ \frac{dx}{dt}(0) = 1 \ \ \ \  y(0) = 0 \ \ \ \ \frac{dy}{dt}(0) = - 1\\
s^2 x - 1
$$
De tarea hay que encontrar la X y desaparecer la y

.

.

.

### Ejercicio

$$
\frac{dx}{dt} = -x + y \ \ \ \ \ \ x(0)\\
\frac{dy}{dt} = 2x \ \ \ \ \ \ y(0) = 1
$$

- Usaremos las formulas 28 y 29 de las tablas de las transformadas de Laplace.

**Lo hacemos para x**
$$
sx + x - y = 0\\
sy - 1 - 2x = 0\\
Generamos \ \ el \ \ sistema:\\
(s + 1) x - y = 0\\
-2x + sy = 1\\
Resolvemos \ \ el \ \ sistema:\\
(s^2 + s - 2)x = 1\\
x = \frac{1}{s^2 + s -2}\\
Obtenemos \ \ X:\\
x = \frac{1}{(s + 2)(s-1)}\\
x = \frac{e^{-2t} - e^t}{-3}
$$

- Si ya tenemos el valor de la $x$, podemos volver a hacer todo el procedimiento o podemos simplemente sustituirla y derivarla para sacar la $y$

$$
\frac{dx}{dt} = \frac{-2e^{-2t} - e^{t}}{-3}
$$

- Entonces la $y$ es la suma de estas dos cosas.

$$
y = \frac{e^{-2t} + 2e^t}{3}
$$

