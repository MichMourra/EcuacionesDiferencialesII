# Ejercicios de transformadas de Laplace

- Hoy resolveremos tres ecuaciones diferenciales por transformadas de Laplace.

- Una ventaja de las transformadas de Laplace es que como suponen condiciones iniciales la respuesta que nos dan ya tiene integrada esas condiciones iniciales, entonces no tenemos constantes que tenemos que resolver, como si ocurre en los otros métodos.

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

- En términos de resolver una ecuación diferencial esta ya esta resuelta, únicamente debemos sustituir y despejar.

$sy + 4y = 2 + \frac{1}{s + 4}$

$(s + 4) y = 2 + \frac{1}{s + 4}$

$y = \frac{2}{s+4} + \frac{1}{(s + 4)^{2}}$

- Con esto podemos aplicar la formula 11 y anti-transformamos el resultado:

![image-20211130122902380](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130122902380.png)

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
y = \frac{s}{(s+1)^2} + \frac{3}{(s+1)^2}\\
$$

- Mejor lo escribimos de otra manera para poder aplicar las formulas:

$$
y = \frac{s + 1 - 1}{(s + 1)^2} + \frac{3}{(s + 1)^2} = \frac{s + 1}{(s+1)^2} - \frac{1}{(s+1)^2} + \frac{3}{(s+1)^2}\\
$$

- Simplificamos los que tienen un común denominador y los que podemos eliminar:

$$
y = \frac{1}{s+1} + \frac{2}{(s+1)^2}
$$

- Debemos encontrar cual es la formula que me va a permitir regresar a la ecuación inicial.

- Una es una exponencial directa y la otra es una exponencial por una t.

- Entonces tenemos que utilizar la formula 11 y 16.

  ![image-20211130124429504](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130124429504.png)

![image-20211130124532986](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130124532986.png)

**Resultado**
$$
y = e^{-t} + 2te^{-t}
$$

3. 

$$
\frac{d^2y}{dt^2} - 6\frac{dy}{dt} + 13y = 0\\
y(0) = 0\\
\frac{dy}{dt}(0) = -3
$$

**Solución**

- Usamos la formula 18 de las transformadas de Laplace:

![image-20211130122703002](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130122703002.png)
$$
s^2Y + 3 - 6sY + 13Y = 0\\
(s^2 - 6s + 13)Y = -3\\
Y = \frac{-3}{s^2 - 6s + 13}\\
y = \frac{-3}{(s-3)^2 + 4} = \frac{-3}{2} \frac{2}{(s-3)^2 + 4}\\
$$

- Sacamos la constante que esta multiplicando y ya la podemos anti-transformar con la formula.

$$
y =  \frac{-3}{2} L^{-1}\left\{\frac{2}{(s-3)^2 + 4}\right\}\\
$$

**Resultado**
$$
y = \frac{-3}{2} \left( e^{st} \sin 2t\right)
$$


## Sistemas de ecuaciones con transformadas de Laplace

**Ejemplo**

En este caso utilizaremos las transformadas de Laplace para resolver sistemas de ecuaciones diferenciales.
$$
\left\{
\frac{d^2x}{dt^2} + 10x - 4y = 0\atop
-4x + \frac{d^2y}{dt^2} + 4y = 0\right.
$$
- Tenemos que tener dos condiciones iniciales para cada variable ya que de lo contrario no podemos transformar

$$
x(0) = 0 \ \ \ \ \frac{dx}{dt}(0) = 1 \ \ \ \  y(0) = 0 \ \ \ \ \frac{dy}{dt}(0) = - 1\\
s^2 x - 1
$$

- Transformamos cada ecuación:

$$
\left\{
s^2X - 1 + 10X - 4y = 0\atop
-4X + s^2Y + 1 + 4Y = 0\right.
$$

- Ahora vamos a juntar los terminos semejantes para simplificarlo.

$$
\left\{
(s^2 + 10)X - 4Y = 1\atop
-4X + (s^2 + 4)Y = -1\right.
$$

- Con esto ya tenemos nuestro nuevo sistema de ecuaciones.
- Ahora lo resolvemos.

- Escogemos una de las variables y desaparecemos la otra.
- En este caso vamos a desaparecer la X.

$$
\left\{
4(s^2 + 10)X - 16Y = 4\atop
-4(s^2 + 10)X + (s^2+10)(s^2 + 4)Y = -(s^2+10)\right.
$$

- Ahora lo sumamos y todo nos queda en terminos de Y , s.

$$
((s^2+10)(s^2+4)-16)Y = -(s^2+10) + 4
$$

- Despejamos la Y.

$$
Y = \frac{-(s^2 + 10)}{(s^2+10)(s^2 + 4) - 16} + \frac{4}{(s^2+10)(s^2+4)-16}
$$

- Simplificamos

$$
Y = \frac{-s^2-6}{(s^2+10)(s^2+4)-16}
$$

Esto no parece tener la forma de algo que podamos usar, por lo que debemos, convertirlo a una forma en la que podamos aplicar la formula de una transformada de Laplace.

- Obtenemos el resultado del denominador y lo factorizamos:

$$
s^4 + 4s^2 + 10s^2 + 40 - 16\\
Simplificamos:\\
s^4 + 14s^2 + 24\\
Factorizamos:\\
(s^2+12)(s^2+2)
$$

- Ahora procedemos a anti-transformar.

$$
Y = L^{-1}\left\{ \frac{-s^2-6}{(s^2+12)(s^2+2)}\right\}
$$

- Para poder hacer la anti-transformada necesitamos sumar y restar un 6.

$$
Y = L^{-1}\left\{ \frac{-s^2-6 + 6 - 6}{(s^2+12)(s^2+2)}\right\}
$$

- Por lo que podemos expresarla como:

$$
Y = L^{-1}\left\{ \frac{-s^2-12}{(s^2+12)(s^2+2)} + \frac{6}{(s^2+12)(s^2+2)}\right\}
$$

- Por lo que podemos simplificar valores iguales en la primer fracción:

$$
Y = L^{-1}\left\{ \frac{-1}{(s^2+2)} + \frac{6}{(s^2+12)(s^2+2)}\right\}
$$

- De modo que lo podemos resolver usando las formulas de transformadas 7 y 32.

![image-20211130173921702](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130173921702.png)

![image-20211130173505307](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130173505307.png)

**Respuesta**

**En este caso**
$$
a = \sqrt{12}\\
b = \sqrt{2}
$$
**Por lo tanto**
$$
Y = -\frac{1}{\sqrt{2}} \sin \sqrt{2}t + \frac{\sqrt{12} \sin \sqrt{2}t - \sqrt{2} \sin \sqrt{12}t}{\sqrt{24}(10) }
$$


De tarea hay que encontrar la X al desaparecer la y



### Ejercicio

**Sistema**
$$
\left\{
\frac{dx}{dt} = -x + y \atop
\frac{dy}{dt} = 2x \right.
$$

**Condiciones iniciales**
$$
x(0) = 0\\
y(0) = 1
$$


- Usaremos las formulas 28 y 29 de las tablas de las transformadas de Laplace.

![image-20211130174828697](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130174828697.png)

![image-20211130174841780](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211130174841780.png)

**Lo hacemos para x desapareciendo la y**
$$
Generamos \ \ el \ \ sistema:\\
\left\{
sx + x - y = 0\atop
sy - 1 - 2x = 0\right.\\
Factorizamos:\\
\left\{
(s + 1) x - y = 0\atop
-2x + sy = 1 \right.\\
Resolvemos \ \ el \ \ sistema \ \ con \ \ s:\\
(s^2 + s - 2)x = 1\\
x = \frac{1}{s^2 + s -2}\\
Obtenemos \ \ X:\\
x = \frac{1}{(s + 2)(s-1)}\\
Anti-Transformamos:\\
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

