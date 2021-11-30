# Ecuaciones diferenciales clase XII

## Transformada de Laplace

- Las transformadas de Laplace se definen como un cambio de una función de variable $t$ en una función de variable $s$ que denotamos con una letra mayuscula $F$

- Es decir:

$$
L \left\{ f(t)\right\} = \int_0^\infty e^{-st} f(t) dt = F(s) = F
$$

- La ves pasada lo que hicimos fue hacer unas cuantas transformaciones de unas funciones elementales.

- No es necesario usar esta formula debido a que siempre dara este mismo resultado.

- Por este motivo un matemático se encargo de de realizar unas tablas que indican como será el resultado de la ecuación.

- La transformada es una integral, la cual a su vez es un operador lineal.

- Esto quiere decir dos cosas:

  - La integral de una suma es la suma de integrales

    $\int ax^2 + bx = \int ax^2 + \int bx$

  - Una constante multiplicada por el integrando es igual a la constante multiplicada por la integral

    $\int ax^2 = a \cdot \int x^2$

## Ejemplos

1. 

$$
f(t) = 2t^4
$$

**Solución**
$$
L\left\{2t^4\right\} = 2 \cdot L \left\{t^4\right\}\\
Resultado:\\
2\frac{4!}{s^5} = \frac{48}{s^5}
$$

- Si queremos transformar una suma como esta:

$$
L \left\{t^2 + 6t - 3\right\} = \frac{2!}{s^3} + 6 \frac{1}{s^2} - 3 \frac{1}{s}
$$

- Algunas transformaciones son mas latosas por ejemplo:

$$
L \{(t + 1)^3\}
$$

En este caso no existe una regla general para binomios potenciados, por este motivo primero deberiamos desarrollar el binomio al cubo:
$$
\frac{3!}{s^4} + 3 \frac{2!}{s^3} + 3 \frac{1}{s^2} + \frac{1}{s}
$$

## Ejercicios transformadas

Estos ejercicios se haran con las formulas 3, 7 y 11 de las tablas de Laplace.                                                                                                                                                                                                                                                                                                                                                                                       

1. 

$$
L \{(1 + e^{2t})^2\}
$$

**Solución**



**Respuesta**

$\frac{1}{s} + \frac{2}{s-2} + \frac{1}{s-4}$



2. 

$$
L \{ 1 + e^{4t}\}
$$

**Solución**



**Respuesta**

$\frac{1}{s} + \frac{1}{s-4}$

3. 

$$
L \{ 4t^2 - 5 \sin 3t\}
$$

**Solución**



**Respuesta**

$\frac{8}{s^3} - \frac{15}{s^2 + 4}$



4. 

$$
L \{ \sin 2t \cos 2t\}
$$

- Para esto necesitaremos la identidad trigonometrica:

  $\sin 2\alpha = 2 \sin \alpha \cos \alpha$

**Solución**



**Respuesta**

$\frac{2}{s^2 + 16}$



## Anti-transformaciones 

La anti transformación requiere una transformación en si.
$$
L^{-1} \{\frac{1}{s^5}\}\\
L \{t^4\} = \frac{4!}{s^5}
$$

- Pasamos el cuatro factorial que esta multiplicando del otro lado para dejar únicamente lo que tiene s como resultado:

$$
\frac{1}{24} L\{t^4\} = \frac{1}{s^5}\\
L \{\frac{t^4}{24}\} = \frac{1}{s^5}
$$

- Esto lo haremos siempre porque no necesariamente tendremos las constantes que aparecen en la formula.

**Ejemplo**

Buscamos la anti-transformada de:
$$
L^{-1} \{\frac{5}{s^2 + 4}\} 
$$

- Para esto podemos utilizar la transformada de:

$$
L \{\sin 2t\} = \frac{2}{s^2 + 4}
$$

Resultado:
$$
L \left\{ \frac{5 \sin 2t}{2}\right\} = \frac{5}{s^2 + 4}
$$

## Ejercicios Anti transformadas

1. 

$$
L^{-1} \left\{\frac{1}{s^2 + 7}\right\}
$$

**Solución**



2. 

$$
L^{-1} \left\{\frac{-2s + 6}{s^2 + 4}\right\}
$$

**Solución**



3. 

$$
L^{-1} \left\{ \frac{2 + s}{s^2 - 3s + 2}\right\}
$$

**Solución**

Esta anti-transformada no esta en ninguna formula de las tablas.

- Tenemos que factorizar el denominador.
- Separamos todo.

$$
L^{-1}\left\{\frac{2 + s}{(s - 2)(s - 1)} - \frac{2}{(s-2)(s-1)} + \frac{s}{(s-2)(s-1)}\right\}
$$

**Respuesta**
$$
= 2 \left( e^{2t} - e^{t}\right) + 2e^{2t} - e^{t}\\
4e^{2t} - 3e^t
$$

4. 

$$
L^{-1} \left\{\frac{1}{s^2} - \frac{48}{s^5}\right\}
$$

**Solución**



5. 

$$
L^{-1} \left\{ \frac{(s + 1)^3}{s^4}\right\}
$$

**Solución**



- No tenemos formula que nos permita anti-transformar esto.
- Pero tenemos un binomio al cubo, entonces debemos desarrollarlo.

$$
L^{-1} \left\{ \frac{s^3 + 3s^2 + 3s + 1}{s^4} \right\}\\
L^{-1} \left\{ \frac{1}{s} + \frac{3}{s^2} + \frac{3}{s^3} + \frac{1}{s^4} \right\}\\
$$

- Podemos ver que faltan y sobran cosas
- Seguramente es una tranformada que incluya a:
- Antitransformamos por partes iniciando con $\frac{3}{s^3}$

$$
L^{-1} \left\{ \frac{1}{t^2} \right\} = \frac{2!}{s^3}\\
\frac{3}{2} L \left\{ \frac{1}{t^2} \right\} = \frac{3}{s^3}
$$

- Ahora pasamos a transformar $\frac{1}{s^4}$

$$
L\left\{ \frac{1}{t^3}\right\} = \frac{3!}{s^4}
$$

Tras construir la ecuación nos queda:

$1 + 3t + \frac{3}{2} \frac{1}{t^2} + \frac{1}{6}t^3$



6. 

$$
L^{-1} \left\{ \frac{1}{4s + 1}\right\}
$$

**Solución**



7. 

$$
L^{-1} \left\{\frac{5}{s^2 + 49}\right\}
$$

**Solución**



8. 

$$
L^{-1} \left\{ \frac{4s}{4s^2 + 1} \right\}
$$

**Solución**



9. 

$$
L^{-1} \left\{ \frac{1}{s^3 + 3s} \right\}
$$

**Solución**



10.
$$
L^{-1} \left\{ \frac{s}{s^2 + 2s - 3} \right\}
$$
**Solución**



En clase resolvimos el 3 y el 5, por lo que el resto de los ejercicios queda de tarea.

## Ecuaciones diferenciales

$$
\frac{d^2y}{dt^2} - 3 \frac{dy}{dt} + 2 y = e^{-4t}\\
y(0) = 1 \\
\frac{dy}{dt}(0) = 5
$$

- Esta ecuación la vamos a transformar, luego la vamos a resolver y finalmente la vamos a anti-transformar.
- Utilizamos la formula de la tabla.

Transformamos la 2da derivada: $s^2 Y - s -5$

Transformamos la 1ra derivada: $-3sY - 1$

Los terminos de y se cambian por Y: $2Y$

Transformamos la exponencial: $\frac{1}{s + 4}$

Entonces tenemos toda la expresión transformada:
$$
s^2 Y - s -5 -3sY - 1 + 2Y = \frac{1}{s + 4}
$$
Factorizamos la Y:
$$
s^2Y - 3sY + 2Y = \frac{1}{s + 4} + s + 2\\
Y(s^2 - 3s + 2) = \frac{1}{s + 4} + s + 2\\
Entonces:\\
Y(s-2)(s-1) = \frac{1}{s + 4} + s + 2\\
Despejamos:\\
Y = \frac{1}{(s+4)(s-2)(s-1)} + \frac{s}{s-1} + \frac{2}{(s-2)(s-1)}
$$
Ahora estamos en un proceso en el que tenemos la Y despejada.

- Pero esta Y no es una solución por que esta en función de s y nosotros la queremos en función de t.
- Para resolver este problema debemos de anti transformar la expresión que tenemos.
- Lo vamos a anti transformar con las formulas 28 y 29. El que no tiene formula le cambiaremos la forma.

$$
\frac{1}{(s + 4)(s - 2)(s - 1)} = \frac{A}{s + 4} + \frac{B}{s-2} + \frac{C}{s-1}
$$

Entonces colocamos todo en una misma fracción:
$$
\frac{A(s-2)(s-1) + B(s+4)(s-1) + C(s+4)(s-2)}{(s+4)(s-2)(s-1)}
$$
Evaluamos con los valores de s y despejamos A,B,C:
$$
s = 2 \ \ \ \ \ \ \ 6B = 1 \ \ \ \ \ \ \ B = \frac{1}{6}\\
s = 1 \ \ \ \ \ \ \ -5C = 1 \ \ \ \ \ \ \ C = - \frac{1}{5}\\
s = -4 \ \ \ \ \ \ \ 30A = 1 \ \ \ \ \ \ \ A = \frac{1}{30}
$$
Ya que tenemos los valores de A,B,C. Podemos decir que:
$$
\frac{1}{30} \left(\frac{1}{s + 4}\right) + \frac{1}{6} \left(\frac{1}{s - 2}\right) - \frac{1}{5} \left(\frac{1}{s - 1}\right)
$$
Ahora que tenemos de esta forma la expresión podemos aplicar las formulas 28 y 29 de nuestras tablas para anti-tranformarla:

Sabemos entonces que y es igual a:
$$
y = L^{-1}\left\{\frac{1}{30} \left(\frac{1}{s + 4}\right) + \frac{1}{6} \left(\frac{1}{s - 2}\right) - \frac{1}{5} \left(\frac{1}{s - 1}\right)\right\}
$$
Por lo tanto, al anti-transformar a partir de las formulas 28 y 29 nos queda:
$$
y = \frac{1}{30}e^{-4t} + \frac{1}{6}e^{2t} - \frac{1}{5}e^{t} + 4e^{3t} + 3e^t
$$

- Esta ya es una solución explicita que incluye los valores iniciales

### Aclaración fórmulas 28 y 29

- La A puede valer 0
- La A y la B no pueden ser iguales
- Si son iguales usamos la 16

## Ejercicios

1. 

$$
\frac{dy}{dt} - y = 1 \ \ \ \ y(0) = 0
$$

**Solución**



**Respuesta**

$y = -1 + e^{t}$

2. 

$$
\frac{dy}{dt} + 6y = e^{4t} \ \ \ \ \ \ y(0) = 2
$$

**Solución**



**Respuesta**

$y = \frac{19}{10}e^{-6t} + \frac{1}{10}e^{4t} $

3. 

$$
\frac{d^2y}{dt^2} + 5 \frac{dy}{dt} + 4y = 0
$$

**Solución**



**Respuesta**

$y = - \frac{1}{3}e^{-4t} + \frac{4}{3}e^{t}$

4. 

$$
\frac{d^2y}{dt^2} + y = (2 \sin \sqrt{2}t)\\
y(0) = 10\\
\frac{dy}{dx}(0) = 0
$$

- En este ejercicio se hace directamente con las formulas 8 y 32 para anti-transformar, no hay que hacer cambios algebraicos.

**Solución**



**Respuesta**

$y = 10 \cos t + 2 \sin t - \sqrt{2} \sin \sqrt2 t $

5. 

$$
\frac{d^2y}{dt^2} - 6 \frac{dy}{dt} + 9y = t^2e^{3t}\\
y(0) = 2\\
\frac{dy}{dt}(0) = 6
$$



**Solución**



**Respuesta**

$y = 2e^{3t} + \frac{1}{12}t^4e^{3t^3}$