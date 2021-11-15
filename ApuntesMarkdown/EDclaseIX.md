# Ecuaciones diferenciales IX

Podemos resolver la ecuación buscando de que función f, provienen esas parciales.

Si tenemos una función del estilo : $M(x,y) dx + N (x,y) dy = 0\\$

- Podemos resolver la diferencial haciendo una integral parcial.
- Debemos calcular la segunda derivada.
- Las parciales deben ser iguales.
- Si yo quiero resolver una ecuación diferencial de la forma M y N, debemos averiguar si proviene de una diferencial parcial.
- Podemos averiguarla descubriendo si provienen de la misma función al derivar de forma cruzada.


$$
Df(x,y) = \frac{\delta f(x,y)}{\delta x} dx + \frac{\delta f(x,y)}{\delta y} dy = 0\\
M(x,y) dx + N (x,y) dy = 0\\
Segunda \ \ derivada:\\
\frac{\delta M(x,y)}{\delta y} = \frac{\delta N(x,y)}{\delta x}\\
$$

Debemos averiguar si esta función es una derivada total, es decir, si es una ecuación exacta.
$$
(x^2 + y^2) \ dx + (x^2 - xy) \ dy = 0\\
Las \ \ derivamos:\\
\frac{\delta}{\delta y} = 2y \ \ \ \ \ \ \ \frac{\delta}{\delta x} = 2x - 1\\
$$
Vemos que sus parciales no son iguales, por lo tanto no vienen de la misma ecuación y no es una ecuación exacta.

- Las ecuaciones no exactas se pueden resolver de una manera elegante y simple, siempre y cuando tengan una propiedad.
- Vamos a definir una propiedad de las ecuaciones que se llama Homogéneas de grado Alfa.
- Las homogéneas de grado alfa son ecuaciones que tienen la propiedad de que al cambiar las $x , y$ por  $t_x,t_y$ se puede factorizar como t a la alfa de la función original.
- $f(x,y) \rightarrow f(tx,ty) = t^{\alpha}f(x,y)$

## Homogéneas de grado Alpha

$$
f(tx,ty) = t^\alpha f(x,y)\\
f(x,y) = x^2y + yx^2 + x^3 + y^3
$$

Como se prueba que es homogénea de grado Alpha, cambiamos $x \rightarrow tx$ y $y \rightarrow ty$
$$
f(tx,ty) = (tx)^2ty + (ty)^2tx + (tx)^3 + (ty)^3\\
t^3x^2y + t^3xy^2 + t^3x^3 + t^3y^3\\
t^3(x^2y + y^2x + x^3 + y^3)\\
\alpha = 3
$$

- Como encontramos la función original multiplicada por t con un exponente alfa, entonces podemos asumir que es una homogénea de grado alfa.
- Alfa es el exponente de la t, si una función es homogénea de grado alfa significa que puedo sustituir x,y por tx,ty y al final factorizar la t.
- Se les llama homogéneas, porque homogéneamente puedo factorizar la t.

## Ejercicio

Resolver si son homogéneas y determinar de que grado son homogéneas:

1. 

$$
f(x,y) = \sqrt{x}\sqrt{y} + x + y
$$

**Respuesta**
$$
(tx)^{\frac{1}{2}} (ty)^{\frac{1}{2}} + tx + ty\\
$$
Para conocer el valor de Alpha es mas fácil sumar los exponentes

En este primer caso la suma de los exponentes es : $(\frac{1}{2} + \frac{1}{2}) + 1 + 1$

Entonces como todos los exponentes son uno, el valor de alfa para esta función será:

$\alpha = 1$

2. 

$$
f(x,y) = xy + x^2 + y^2
$$

En este caso la suma de los exponentes es: $(1+1) + 2 + 2$, en este segundo caso como todos los exponentes son 2, el valor resultante de alfa será:

$\alpha = 2$

3. 

$$
f(x,y) = \sqrt{x}y + \sqrt{y}x + x^{\frac{3}{2}}+ y^{\frac{3}{2}}
$$

Como la suma nos dice que todos valen $\frac{3}{2}$ entonces el calor de alfa será: $\alpha = \frac{3}{2}$

**Todas tienen que tener el mismo exponente, ya que de no ser así no las podemos sacar como factor y no seria homogénea de grado alfa**



## Ejercicio

Esta ecuación no es exacta, ya que si sacamos las derivadas parciales no son iguales. Pero si es homogénea de grado 2. 

$$
(x^2 + y^2)dx + (x^2 -xy)dy = 0\\
$$
Si M(x,y) y N(x,y) son las dos homogéneas de grado Alpha, entonces se resuelven con la sustitución $y = ux$
$$
y = ux\\
dy = udx + xdu\\
Sustituimos \ \ y,dy:\\
x^2 dx + u^2x^2dx + x^2udx + x^3du - x^2u^2dx - x^3u du\\
Cancelamos \ \ iguales \ \ de \ \ signo \ \ opuesto:\\
x^2 dx + x^2udx + x^3du - x^3u du\\
du \ \ de \ \ un \ \ lado \ \ y \ \ dx \ \ de \ \ otro:\\
(x^2 + x^2u)dx = (x^2u -x^3)du\\
(x^2 + x^2u)dx = (x^3u -x^3)du\\
Factorizamos:\\
x^2(1 + u)dx = x^3(u -1)du\\
Separamos \ \ variables:\\
\frac{1}{x}dx = \frac{(u - 1)}{(u + 1)} du\\
\frac{dx}{x} = \frac{u-1}{u+1} du \ \ \ \ \int \frac{dx}{x} = \frac{u-1}{u+1} du\\
$$
- Completamos arriba para simplificar abajo:

$$
\frac{u-1}{u+1} = \frac{u-1+2-2}{u + 1} = \frac{u + 1 - 2}{u + 1}\\
= \frac{u + 1}{u + 1} - \frac{2}{u+1} = 1 - \frac{2}{u + 1}
$$



Integramos:
$$
\int du - 2 \int \frac{du}{u + 1} = u - 2 \ln(u+1)\\
\int \frac{du}{u+1}\\
z = u + 1\\
dz = du\\
\int \frac{dz}{z} = \\
\ln z = \ln (u + 1)
$$
$y = ux\\u = \frac{x}{y}$

Resultado:

- Lo elevamos a la exponencial para que se vea mas bonito.
- Se elevo para quitar logaritmos.
- $e^{C}$ es una constante $K$

$$
\ln x = u - 2 \ln (u + 1) + C\\
e^{\ln x} = e^{u} \cdot e^{\ln (u + 1)} \cdot e^{c}\\
x = e^{u} \cdot e^{\ln x} = e^{\ln (\frac{1}{(u+1)^2})}k = k\frac{e^{u}}{(u+1)^2}\\
x = k \frac{e^{\frac{x}{y}}}{(\frac{y}{x} + 1)^2}
$$

# Ejercicios

1. $$
   (x-y)dx + xdy = 0
   $$

**Respuesta**
$$
(x - ux)dx + x (u \ dx + x \ du)\\
x \ dx - ux \ dx + ux \ dx + x^2 \ du\\
Simplificando:\\
x \ dx + x^2 \ du = 0\\
x \ dx = -x^2 \ du\\
pasamos \ x^2 \ del \ otro \ lado: \\
- \int \frac{1}{x} dx = \int du\\
\ln x = -u + C\\
Resultado\\
\ln x = -\frac{y}{x} + C
$$

3. 
   $$
   (y^2 + yx) \ dx - x^2 dy = 0\\
   $$

4. 

**Respuesta**
$$
((ux)^2 + (ux)x) dx - x^2 (u \ dx + x \ du)\\
u^2x^2 \ dx + ux^2 \ dx - ux^2 \ dx + x^3 \ du\\
u^2x^2 \ dx + x^3 \ du\\
Entonces:\\
u^2x^2 \ dx = -x^3 du\\
\frac{x^2 \ dx }{x^3} = \frac{du}{u^2}\\
\frac{dx}{x} = \frac{du}{u^2} \\
\frac{dx}{x}u^{-2}du\\
\int \frac{dx}{x} = \int u^{-2}du\\
\ln x = - \frac{1}{u} + C\\
Resultado:\\
\ln x = -\frac{x}{y} + C
$$


4. $$
   xy^2 \ dy = (y^3 - x^3)dx
   $$

**Respuesta**
$$
x (ux)^2 \ (u \ dx + x \ du) = ((ux^3 - x^3))dx\\
u^2x^3 \ (u \ dx + x \ du) = ux^3 \ dx - x^3 dx\\
u^3x^3 \ dx + u^2x^4 \ du = ux^3 \ dx - x^3 dx\\
$$
Pasamos los dx de un lado:
$$
u^2x^4 \ du = ux^3 \ dx - u^3x^3 \ dx - x^3 dx\\
Pasamos \ la \ x \ de \ un \ lado:\\
u^2 \ du = \frac{ux^3 \ dx - u^3x^3 \ dx - x^3 dx}{x^4}\\
simplificamos:\\
u^2 \ du = \frac{u \ dx - u^3 \ dx - dx}{x}\\
Integramos:\\
\int u^2 \ du = \int \frac{u \ dx}{x} - \int \frac{u^3\ dx}{x} - \int \frac{dx}{x}\\
\frac{u^3}{3} = u \ln x - u^3 \ln x - \ln x\\
\frac{u^3}{3} = (u - u^3 - 1) \ln x\\
despejamos:\\
\frac{u^3}{u - u^3 - 1} = 3 \ln x
$$

2. $$
   xdx + (y - 2x)dy = 0
   $$

**Resultado**

- Para realizar el ejercicio 2 debemos llegar a la expresión $\frac{(2-u)}{(u-1)^2}$
- Sera bastante complicado de integrar.
- Servirá de entrenamiento para las transformadas de *Laplace*

$$
\frac{(2-u)}{(u-1)^2} = \frac{-(u-2)}{(u-1)^2}\\
Separación:\\
-\frac{(u-1-1)}{(u-1)^2} = - \frac{u-1}{(u-1)^2} + \frac{1}{(u-1)^2} \\
Simplificamos:\\
- \frac{1}{(u-1)} + \frac{1}{(u-1)^2}\\
Cambio \ \ de \ \ variable:\\
z = u -1\\
$$

- El cambio de variable permitirá resolverlo muy rápidamente, la integral con respecto de u no se puede resolver fácilmente.

$$
xdx + (ux - 2x)(udx + xdu)\\
xdx + u^2xdx + ux^2du - 2uxdx - 2x^2du = 0\\
Separamos:\\
(x + u^2x - 2ux)dx = (2x^2 - ux^2) du\\
x(1 + u^2 - 2u)dx = x^2(2-u)du\\
x(u-1)^2 dx = x^2 (2-u)du\\
\frac{dx}{x} = \frac{(2-u)}{(u-1)^2} du= - \frac{(u-1-1)}{(u-1)^2}du =  \left(- \frac{(u-1)}{(u-1)^2} + \frac{1}{(u-1)^2}\right)\\
= \left( - \frac{1}{u-1} + \frac{1}{(u-1)^2} \right) du
$$

- Ahora hay que integrar

$$
\left( \frac{-1}{u-1} + \frac{1}{(u-1)^2}\right)du\\
z = u-1\\
\int -\frac{dz}{z} + \int z^{-2} dz =\\
\ln z = z^{-1} + C\\
\ln \frac{1}{z} - \frac{1}{z} + C \\
\ln \frac{1}{u-1} - \frac{1}{u-1} + C
$$

Finalmente cambiamos la u por y entre x:
$$
\ln \frac{1}{\frac{y}{x}-1} - \frac{1}{\frac{y}{x}-1} + C
$$


![image-20211114215601031](C:\Users\10\AppData\Roaming\Typora\typora-user-images\image-20211114215601031.png)

