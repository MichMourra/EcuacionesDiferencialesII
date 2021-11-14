# Ecuaciones diferenciales IX


$$
Df(x,y) = \frac{\delta f(x,y)}{\delta x} dx + \frac{\delta f(x,y)}{\delta y} dy = 0\\
M(x,y) dx + N (x,y) dy = 0\\
\frac{\delta M(x,y)}{\delta y} = \frac{\delta N(x,y)}{\delta x}\\
(x^2 + y^2) \ dx + (x^2 - xy) \ dy = 0\\
\frac{\delta}{\delta y} = 2y \ \ \ \ \ \ \ \frac{\delta}{\delta x} = 2x - 1\\
$$

## Homogeneas de grado alpha

$$
f(tx,ty) = t^\alpha f(x,y)\\
f(x,y) = x^2y + yx^2 + x^3 + y^3
$$

Como se prueba que es homogenea de grado alpha:
$$
f(tx,ty) = (tx)^2ty + (ty)^2tx + (tx)^3 + (ty)^3\\
t^3x^2y + t^3xy^2 + t^3x^3 + t^3y^3\\
t^3(x^2y + y^2x + x^3 + y^3)\\
\alpha = 3
$$

## Ejercicio

Resolver si son homogeneas y determinar de que grado son homogéneas:

1. 

$$
f(x,y) = \sqrt{x}\sqrt{y} + x + y
$$

**Respuesta**
$$
(tx)^{\frac{1}{2}} (ty)^{\frac{1}{2}} + tx + ty\\
factorizando \ la \ t:\\
$$
Para conocer el valor de alpha es mas facil sumar los exponentes


$$
(x^2 + y^2)dx + (x^2 -xy)dy = 0\\
$$
si M(x,y) y N(x,y) son las dos homogeneas de grado alpha, entonces se resuleven con sustitución 
$$
y = ux\\
dy = udx + xdu\\
x^2 dx + u^2x^2dx + x^2udx + x^3du - x^2u^2dx - x^3u du\\
(x^2 + x^2u)dx = (x^2u -x^3)du\\
(x^2 + x^2u)dx = (x^3u -x^3)du\\
x^2(1 + u)dx = x^3(u -1)du\\
\frac{dx}{x} = \frac{u-1}{u+1} du \ \ \ \ \int \frac{dx}{x} = \frac{u-1}{u+1} du\\
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
Resultado:
$$
\ln x = u - 2 \ln (u + 1) + C\\
e^{\ln x} = e^{\ln (\frac{1}{(u+1)^2})}k = k\frac{e^{u}}{(u+1)^2}\\
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

3. $$
   (y^2 + yx) \ dx - x^2 dy = 0\\
   $$

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
