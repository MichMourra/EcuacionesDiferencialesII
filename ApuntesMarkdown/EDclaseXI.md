# Ecuaciones diferenciales

# Clase XI

## Ejercicio pendiente de ecuaciones no lineales


$$
\frac{d^2y}{dx^2} + (\frac{dy}{dx})^2 + 1 = 0 \\
u = \frac{dy}{dx}\\
\frac{du}{dx} = \frac{d^2y}{dx^2}\\
\frac{du}{dx} + u^2 + 1 = 0\\
\frac{du}{dx} = -1 -u^2 = -(u^2 + 1)\\
$$

- Integramos para resolver la ecuación.
- Angulo tangente es lo mismo que arco tangente.
- $u$ es la tangente del ángulo.
- La tangente es seno entre coseno.

$$
\int \frac{du}{u^2 + 1} = - \int dx\\
ang \tan u = -x + C\\
u = \tan (-x + C)\\
u = \frac{\sin (-x + C)}{\cos(-x + C)}\\
\frac{dy}{dx} = \frac{(\sin (-x + C))}{\cos (-x + C)}\\
\frac{dy}{dx} = \frac{\sin (-x + C)}{\cos (-x + C)}\\
$$

- Hacemos otro cambio de variable con $z$
- Obtenemos la derivada de $z$
- Pasamos las respectivas derivadas de un lado cada una.
- Resolvemos las integrales para obtener el valor de $y$

$$
z = \cos (-x + C)\\
\frac{dz}{dx} = -\sin (-x + C)\\
dz = - \sin (-x + C)\\
\int dy = \int \frac{\sin(-x + C)}{\cos (-x + C)} dx\\
y = -\int \frac{dz}{z} = \ln z + C\\
y = - \ln (\cos (-x + C)) + C_2
$$

- En esta clase solo se reviso este ejercicio de entre los que habían quedado pendiente.

# Transformadas de Laplace

Uno de los axiomas de la probabilidad nos dice que la suma de todas las probabilidades es igual a 1.

La transformada de La place es parte de lo que se conocen como transformadas de integrales.

- Las transformadas de Laplace son una función de una familia de funciones que se conoce como funciones integrales.
- En probabilidad vimos como la suma de las probabilidades de la función de probabilidad tenia que ser uno.
- Un ejemplo es el área bajo la curva en una normal, campana de Gauss.
- También las gamas cumplen con esta condición.
- Las transformaciones integrales tienen la forma: 

$$
\int_{-\infty}^{\infty} K(s,t) f(t) dt\\
$$

- Las transformadas de Fourier tienen un núcleo de la siguiente manera.

$$
\ Densidad \ \ de \ \ Probabilidad:\\
\int_0^\infty f(x) dx = 1\\
e^{-x}
\int K(s , t) f(t) dt\\
Transformada \ de \ Fourier\\
\frac{e^{ist}}{\sqrt{2\pi}}\\
$$
- En las funciones generadoras de momentos para distribuciones de probabilidad:

  - El primer momento es la media.
  - El segundo momento es la varianza.
  - El tercer momento es el coeficiente de sesgo.
  - El cuarto momento es el coeficiente de curtosis.

  Por medio de estas funciones puedo obtener los parámetros de la distribución probabilística por medio de una integral.

  El kernel de la función generadora de momentos es: $e^{st}$

- La característica tienen en común es que a pesar de tener una cantidad infinita de valores, la suma al final siempre debe ser uno.

- Lo que tienen en común es que hay una exponencial negativa.

- La exponencial negativa decrece tan rápido que los valores pequeños tienden a ser muy pronto, por al final la suma converge en uno.

- El kernel de la transformada de Laplace es: $e^{-st}$

- Se llaman transformadas integrales porque cuando una función yo la integro con respecto de $t$ y la evaluó la $t$ va a desaparecer y va a quedar como una función de $s$. Es decir se transformo.

- Las transformadas de Laplace no son lo único que hay en transformadas integrales.

- Todas las transformadas tienen un kernel y una función.

- ***¿Que hace una transformada integral?***

  - Convierte una función $dt$ en una función $ds$

- A esto se llama una transformada integral
- En las transformadas de Laplace van de $0$ a $\infty$
- Como vamos a resolver ecuaciones con las transformadas de Laplace debemos aprender como se transforma una derivada.

La transformada de La place es en si de esta forma:

- Las exponenciales negativas cuando se van a infinito, convergen rápidamente en 0.

$$
L\{ f(t)\} = \int_0^\infty e^{-st} f(t) dt = F(s)\\
Empezamos \ \ con:\\
f(t) = 1 \\
\int_0^\infty e^{-st} dt = \frac{e^{-st}}{-s} \\
|_0^\infty = 0 - (\frac{1}{-s}) = \frac{1}{s}\\
L\{1\} = \frac{1}{s}
$$
- Esto es una transformación de espacios vectoriales, convirtiendo una ecuación diferencial en una no diferencial para resolverla y regresarla con una anti transformada.

## Ejemplo

La transformada de Laplace transforma una función F(t) en una forma F(s).

- Si nuestra $f(t) = t$

|      | derivo |        integro        |
| :--: | :----: | :-------------------: |
|  +   |   t    |       $e^{-st}$       |
|  -   |   1    | $\frac{e^{-st}}{-s}$  |
|  +   |   0    | $\frac{e^{-st}}{s^2}$ |
|  -   |        |                       |

En lugar de aplicar el método de integración por partes con la vaca vestida de uniforme, utilizamos la tablita.

- Gracias a esta tabla ya tenemos nuestra integral
- Esta integral esta definida para los números $0$ e $\infty$
- Hay un problema, esto es con respecto de t, cuando evaluó en infinito una exponencial negativa con respecto de t, vamos a tener un infinito que multiplica un 0.
- Pero como el valor de la exponencial decrece rápidamente. Al hacer manualmente la multiplicación nos damos cuenta de que el decremento prevalece y la multiplicación se va a 0.

$$
L \{ f(t)\} = \int_0^\infty e^{-st} f(t) dt\\
f(t) = t \int e^{-st} dt\\
t\frac{e^{-st}}{-s} - \frac{e^{-st}}{s^2} |_0^\infty = (0-0) -(0-\frac{1}{s^2})\\
Entonces:\\
L\{ t \} = \frac{1}{s^2}
$$

## Transformada de la función $t^2$

- Gracias a las tablas de las transformadas de Laplace ya no tenemos que hacer las integrales horrorosas.

|      | derivo |        integro         |
| :--: | :----: | :--------------------: |
|  +   | $t^2$  |       $e^{-st}$        |
|  -   |   2t   |  $\frac{e^{-st}}{-s}$  |
|  +   |   2    | $\frac{e^{-st}}{s^2}$  |
|  -   |   0    | $\frac{e^{-st}}{-s^3}$ |
|  +   |        |                        |

$$
L\{f(t)\} = \int_0^\infty e^{-sy} f(t)dt\\
f(t) = t^2\\
\int_0^\infty e^{-st}t^2 dt\\
- t^2 \cdot \frac{e^{-st}}{s} - 2t\frac{e^{-st}}{s^2}- \frac{2e^{-st}}{s^3} |_0^\infty\\
(-0-0-0)-(-0-0-\frac{2}{s^3}) = \frac{2}{s^3}
$$

## Transformada $f(t) = e^{at}$

- Cuando tengo la misma base, las propiedades de las integrales dicen que se suman los exponentes
- Podemos factorizar la t

$$
L\{f(t)\} = \int_0^\infty e^{-st}f(t)dt\\
f(t) = e^{at}\\
\int_0^\infty e^{-st} e^{at} dt = \int_0^\infty e^{at - st}dt\\
\int_0^\infty e^{(a-s)t}dt\\
\int e^{kt} dt = \frac{e^{kt}}{k}\\
\frac{e^{(a-s)t}}{a-s} |_0^\infty = (0-\frac{}{})
$$



## Transformada de la segunda derivada

- Hacemos la tablita para ver que derivo y que integro.

$$
L\{ \frac{d^2f(t)}{dt^2}\} = \int_0^\infty e^{-st \frac{d^2 f(t)}{dt^2}}dt \\
u = e^{-st}\\
du = se^{-st}dt
dv = \frac{d^2f(t)}{dt^2}\\
v = \frac{df(t)}{dt}\\
e^{-st} \frac{df(t)}{dt} |_0^\infty  - \int_0^\infty - e^-st \frac{df(t)}{dt^2}
$$





# Tablas de transformadas de Laplace

## Archivo 1

![image-20211116134147670](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134147670.png)

![image-20211116134206636](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134206636.png)

![image-20211116134236651](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134236651.png)

![image-20211116134303515](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134303515.png)

## Archivo 2

![image-20211116134419420](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134419420.png)

![image-20211116134447873](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134447873.png)

![image-20211116134616568](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134616568.png)

![image-20211116134631902](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211116134631902.png)

