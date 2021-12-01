# Ecuaciones diferenciales clase 14

### Como funcionan los cambios de variable con las transformadas

$$
L\{f(t)\} =\int_{-\infty}^{\infty} e^{st} f(t) dt = F(0) = F\\
L\{x(t)\} =\int_{-\infty}^{\infty} e^{st} x(t) dt = X(0) = X\\
L\{y(t)\} =\int_{-\infty}^{\infty} e^{st} y(t) dt = Y(0) = Y\\
$$

- Al ser transformadas se convierten en su forma mayúscula.

## Ejemplo sistemas de ecuaciones diferenciales

Vamos a resolver el ejercicio que vimos la clase pasada. Es decir ejercicios con sistemas de dos ecuaciones diferenciales.

Vamos a resolver un sistema no homogéneo. 

- Estos sistemas no los resolvemos con frecuencia

$$
\left\{ 2 \frac{dx}{dt} + \frac{dy}{dt} - 2x = 1 \atop
\frac{dx}{dt} + \frac{dy}{dt} - 3x - 3y = 2 \right.
$$

**Condiciones iniciales**
$$
x(0) = 0\\
y(0) = 0
$$

- Tenemos este sistema de dos ecuaciones con dos incognitas y queremos resolverlo
- Para resolverlo tenemos que transformarlo todo con las tablas que tenemos.
- Es decir haremos un sistema que tenga s.

$$
\left\{
2sX - sY - 2X = \frac{1}{s}\atop
sX + sY - 3x -3y = \frac{2}{s}
\right.
$$

- De este modo ya tenemos las ecuaciones transformadas.
- Agrupamos las X y las Y factorizando.

$$
\left\{
(2s - 2)X + sY = \frac{1}{s}\atop
(s-3)X + (s-3)Y = \frac{2}{s}
\right.
$$

- Este es el sistema que vamos a resolver y despues vamos a anti-transformar.
- Obtener cualquier variable esta complicado.

- Vamos a desaparecer la variable Y.

$$
\left\{
(s-3)(2s-2)X + s(s-3)Y = \frac{s-3}{s}\atop
- (s-3)X - s(s-3)Y = - 2
\right.
$$

- Al sumarlas nos queda:

$$
\left((s-3)(2s-2) - s(s-3)\right) X = \frac{s-3}{s}-2\\
\left((s-3)(2s-2-s)\right)X = \frac{s}{s} -\frac{3}{s} - 2\\
(s-3)(s-2)X = - 1 -\frac{3}{s} 
$$

- Ahora ya tenemos la X

$$
X = \frac{1}{(s-3)(s-2)} - \frac{3}{s(s-3)(s-2)}
$$

- Podemos buscar en la tabla y nos damos cuenta de que el primero tiene la forma de la formula 28 , pero el segundo es mas complicado. Por eso debemos cambiarle la forma a ese termino.

$$
\frac{3}{s(s-3)(s-2)} = \frac{A}{s} + \frac{B}{s-3} + \frac{C}{s-2}\\
Entonces:\\
\frac{A(s-3)(s-2) + Bs(s-2) + Cs(s-3)}{s(s-3)(s-2)}
$$

- Con esto tenemos una igualdad con denominadores idénticos, ahora obtenemos los valores de A,B,C evaluando los valores de s.

$$
s = 0 \ \ \ \ \ \ 6A = -3 \ \ \ \ \ \ A = - \frac{1}{2}\\
s = 3 \ \ \ \ \ \ 3B = -3 \ \ \ \ \ \ B = - 1\\
s = 2 \ \ \ \ \ \ -2C = -3 \ \ \ \ \ \ C =  \frac{3}{2}\\
$$

- Ahora el termino que no sabiamos anti-transformar se convierte en lo siguiente

$$
-\frac{1}{2} \frac{1}{s} - \frac{1}{s-3} + \frac{3}{2} \frac{1}{s-2}\\
$$

- Ahora si podemos anti-transformar:
- Formula 28

![image-20211201020234751](/Users/carlosmichelmourradiaz/Library/Application Support/typora-user-images/image-20211201020234751.png)
$$
x(t) = e^{3t} - e^{2t} 
$$


**Resultado final**
$$
x(t) = - \frac{1}{2} + \frac{1}{2}e^{2t}
$$

- Ahora resolvemos para la y, de tarea.


## Ejercicio

1. 

$$
\left\{
\frac{dx}{dt} - x + 2y  = 0 \atop
\frac{dy}{dt} - 5x + y = 0
\right.
$$

**Condiciones iniciales**
$$
x(0) = -1\\
y(0) = 2
$$


**Solución**

- Para resolver el valor de y hay que desaparecer la x. Por eso primero la transformamos.

$$
\left\{
2(s-1)x + sy = \frac{1}{s}\atop
(s-3)x + (s-3)y = \frac{2}{s} 
\right.\\
$$

- Multiplicamos por los valores correspondientes para eliminar la X

$$
\left\{
2(s-3)(s-1)x + s(s-3)y = \frac{s-3}{s}\atop
-2(s-1)(s-3)x + 2(s-1)(s-3)y = \frac{4(s-1)}{s} 
\right.\\
$$

- Realizamos la suma del sistema para eliminar la X.

$$
(s(s-3) - 2(s-1)(s-3))y = \frac{s-3}{s} -\frac{4(s-1)}{s}\\
(s-3)(s-2s+2)y = \frac{s-3-4s+4}{s} = \frac{-3s}{s} + \frac{1}{s} = -3 + \frac{1}{s}\\
(s-3)(-s+2)y = - 3 + \frac{1}{s}\\
$$

- Despejamos y

$$
y = \frac{3}{(s-3)(s-2)} + \frac{1}{s(s-3)(s-2)}
$$

- El primero se hace con la formula 28 y el segundo se hace con fracciones parciales como el que resolvimos hace rato.

**Fracciones parciales**
$$
\frac{1}{s(s-3)(s-2)} = \frac{A}{s} + \frac{B}{s-3} + \frac{C}{s-2}
$$
Entonces:
$$
\frac{a(s-3)(s-2) + Bs(s-2) + Cs(s-3)}{s(s-3)(s-2)}
$$

- Evaluamos los posibles valores de s:

$$
s = 0 \ \ \ \ \ \ 6A = 1  \ \ \ \ \ \ A = \frac{1}{6}\\
s = 3 \ \ \ \ \ \ 3B = 1  \ \ \ \ \ \ B = \frac{1}{3}  \\
s = 2 \ \ \ \ \ \ 2C = 1  \ \ \ \ \ \ C = - \frac{1}{2}
$$

- Con esto ya podemos colocar el valor de y, en una forma que lo podamos anti-transformar.

$$
y = \frac{3}{(s-3)(s-2)} + \frac{1}{6} \cdot \frac{1}{s} + \frac{1}{3} \cdot \frac{1}{s-3} - \frac{1}{2} \cdot \frac{1}{s-2}
$$

**Resultado anti-transformando**
$$
y(t) = 3^{3t} - 3e^{2t} - \frac{1}{6} - \frac{1}{3}e^{3t} + \frac{1}{2} e^{2t} =  \frac{8}{3}e^{3t} - \frac{5}{2}e^{3t} - \frac{1}{6}
$$


2. 

$$
\left\{
\frac{d^2x}{dt^2} + \frac{d^2y}{dt^2} = t^2 \atop
\frac{d^2x}{dt^2} - \frac{d^2y}{dt^2} = 4t
\right.
$$

$x(0) = 8 \ \ \ \ \ \frac{dx}{dt}(0) = 0\\y(0) = 0 \ \ \ \ \ \frac{dy}{dt}(0) = 0$





