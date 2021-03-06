# Ecuaciones diferenciales clase IV

El trabajo de hoy ya lo han hecho 15 generaciones antes y consiste en que los alumnos descubren el método haciendo estos 16 ejercicios de modo que el alumno desarrolle una forma de resolverlo.

**¿Qué es el factor integrante?**

El **factor integrador**, también conocido como *factor de integración* o *factor integrante* de una [ecuación diferencial](https://es.wikipedia.org/wiki/Ecuación_diferencial)*,* se define como una [función](https://es.wikipedia.org/wiki/Función_matemática) (usualmente representada por la letra griega μ) que al multiplicarse por una ecuación diferencial no exacta, puede convertirla en una ecuación diferencial exacta.

Usar el factor integrador como un método de resolución de ecuaciones diferenciales requiere de algunos aspectos a tomar en cuenta.

![image-20211114135427675](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211114135427675.png)

## Resuelve para Y

### Problema 1

1. $\frac{dy}{dx} = \cos x$

- Respuesta

$y = \sin x$

----------------------------------------------------------

### Problema 2

2. $\frac{dzy}{dx} = \cos x$

- Respuesta

$y = \sin x$

$zy = \sin x$

**$y = \frac{\sin x}{z}$**

--------------------------------------------------------------------

### Problema 3

3. $z \frac{dy}{dx} + y \frac{dz}{dx} = \cos x$

- Respuesta

  Esta expresion es lo mismo que:

$\frac{dzy}{dx} = \cos x$

Por lo que:

$zy = \sin x$

$y = \frac{\sin x}{z}$

-------------------------------------------------------

### Problema 4

4. $\sec x \cdot y' + \sec x \cdot\tan x \cdot y = \cos x$

- Respuesta

Esta expresión es lo mismo que una derivada de un producto, por lo que $z = \sec x$

$\frac{d (\sec x) y }{dx} = \cos x$

$(\sec x) y = \sin x$

$y = \frac{\sin x}{\sec x}$

----------------------------------------------------------------------

### Problema 5

5. $\frac{1}{\cos x} \cdot \frac{dy}{dx} + \frac{1}{\cos x} (\tan x) \cdot y = \cos x$

- Respuesta 

como $\frac{1}{cos x} = \sec x$

Entonces igual es un producto de la secante:

$\frac{d (\sec x) y }{dx} = \cos x$

$(\sec x) y = \sin x$

$y = \frac{\sin x}{\sec x}$

------------------------------------------------------------------------------------------

### Problema 6

6. $\frac{1}{\cos x} \cdot \frac{dy}{dx} + \frac{\sin x}{\cos ^{2}x} \cdot y = \cos x $

- Respuesta

Sabemos que $\tan x \sec x = \frac{\sin x}{\ cos^2 x}$

por lo tanto es igual a la derivada de la secante, entonces es lo mismo que el ejercicio anterior.

$\frac{d (\sec x) y }{dx} = \cos x$

$(\sec x) y = \sin x$

$y = \frac{\sin x}{\sec x}$

+++++++++++++++++++++++++++++

### Problema 7

7. $\frac{dy}{dx} + \frac{\sin x}{\cos x} \cdot y = \cos ^2 x$

- Respuesta

Si despejamos coseno al separar el cuadrado, entonces nos queda :

$\frac{1}{\cos x} \cdot \frac{dy}{dx} + \frac{\sin x}{\cos ^{2}x} \cdot y = \cos x $

Lo cual es el ejercicio anterior por lo tanto su respuesta es la misma:

Sabemos que $\tan x \sec x = \frac{\sin x}{\ cos^2 x}$

por lo tanto es igual a la derivada de la secante, entonces es lo mismo que el ejercicio anterior.

$\frac{d (\sec x) y }{dx} = \cos x$

$(\sec x) y = \sin x$

$y = \frac{\sin x}{\sec x}$

+++++++++++++++++++++++++++++++++++++++++++

### Problema 8

8. $\frac{dy}{dx} + (tan x) \cdot y = \cos ^2 x$

- Respuesta

Si despejamos coseno al separar el cuadrado, entonces nos queda :

$\frac{1}{\cos x} \cdot \frac{dy}{dx} + \frac{\sin x}{\cos ^{2}x} \cdot y = \cos x $

Lo cual es el ejercicio anterior por lo tanto su respuesta es la misma:

Sabemos que $\tan x \sec x = \frac{\sin x}{\ cos^2 x}$

por lo tanto es igual a la derivada de la secante, entonces es lo mismo que el ejercicio anterior.

$\frac{d (\sec x) y }{dx} = \cos x$

$(\sec x) y = \sin x$

$y = \frac{\sin x}{\sec x}$

--------------------------------------------------------------

### Problema 9

9. $\sec x \cdot \frac{dy}{dx} + (\sec x \tan x) \cdot y = x^2$

- Respuesta 

$\frac{d (\sec x) y }{dx} = x^2$

$(\sec x) y = \frac{x^3}{3}$

$y = \frac{x^3}{3\sec x}$

--------------------------------------------------------------------

### Problema 10

10. $\frac{dy}{dx} + (\tan x) \cdot y = x^2 \cos x$

Despejamos el coseno hacia el otro lado y es lo mismo que el anterior

- Respuesta 

$\frac{d (\sec x) y }{dx} = x^2$

$(\sec x) y = \frac{x^3}{3}$

$y = \frac{x^3}{3\sec x}$

---------------------------------------------------------

### Problema 11

11. $\frac{dy}{dx} + (\tan x) \cdot y = \cos x$

Despejamos el coseno al otro lado de la igualdad y nos queda

- Respuesta 

$\frac{d (\sec x) y }{dx} = 1$

$(\sec x) y = x$

$y = \frac{x}{\sec x}$

---------------------------------------

### Problema 12

12. $\frac{dy}{dx} + (\tan x) \cdot y = \sec x$

- Respuesta

Multiplicamos toda la ecuación por la secante, por lo que nos queda:

$\sec x\frac{dy}{dx} + \sec x(\tan x) \cdot y = \sec^2 x$

$\frac{d}{dy} (\sec x) y = \sec^2$

Sabemos que secante cueadrada es la derivada de la tangente, por lo tanto:

$(\sec x) y = \tan x$

$y = \frac{\tan x}{\sec x}$

--------------------------------------------------

### Problema 13

13. $\frac{dy}{dx} + (tan x) y = \cos x e^x$

- Respuesta

Despejamos el coseno al otro lado de la igualdad y nos queda:

$\sec x \frac{dy}{dx} + \sec x(tan x) y = e^x$

Entonces:

$\frac{d}{dy} (\sec x) y = e^x$

$(\sec x) y = e^x$

$y = \frac{e^x}{\sec x}$

----------------------------------------------------------

### Problema 14

14. $\frac{dy}{dx} + \frac{6}{x}y = 1$

- Respuesta

$I\frac{dy}{dx} + I \frac{6}{x}y = I$

Sacamos el 6

$I\frac{dy}{dx} + 6 \frac{I}{x}y = I$

$\frac{d}{dx} x^6 = 6x^5$

$\frac{d}{dx} x^n = nx^{n-1}$

------------------------------------------------------------

### Problema 15

15. $\frac{dy}{dx} + \frac{2}{x}y = x + 3$

**Respuesta**

$x^2 \frac{dy}{dx} + 2xy = x^3 + 3x^2$

$\frac{dx^2y}{dx} = x^3 + 3x^2$

$x^2y = \frac{x^4}{4} + \frac{3x^3}{3} + C$

$y = \frac{1}{4}x^2 + x + C$

$e^{2 \log x} = e^{\log x^2} = x^2$

------------------------------------------------------

### Problema 16

16. $\frac{dy}{dx} + P(x)y = Q(x)$

- Respuesta

$I\frac{dy}{dx} + IPy = IQ$

$\frac{dI}{dx} = IP$

$\frac{dI}{I} = Pdx$

$e^{\int P(x) dx} \frac{dy}{dx} + e^{\int P(x) dx} P(x)y = e^{\int P(x) dx} Q(x)$

$\int \frac{dI}{I} = \int Pdx$

$ln I = \int Pdx$

$I = e^{\int Pdx}$

$I = e^{5P(x) dx}$

-----------------------------------------



