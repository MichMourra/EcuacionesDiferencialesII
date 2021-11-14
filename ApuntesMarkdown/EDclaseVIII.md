# Ecuaciones Diferenciales VIII

Para que tenga la forma de la derivada de un producto es claro que le falta un factor integrante por lo que este factor lo encontraremos integrando. La constante de integración no es necesaria, lo que sea que sirva es lo que utilizaremos.

**No quiero todos los posibles casos, solo uno que sirva**
$$
\frac{dyz}{dx} = f(x)\\
y = \frac{\int f(x)dx}{z}\\
z\frac{dy}{dx} + \frac{dz}{dx}y = f(x)\\
\frac{dy}{dx} + P(x)y = Q(x)
$$
Queremos convertir esta expresión:
$$
\frac{dy}{dx} + P(x)y = Q(x)
$$
En esta otra:
$$
z\frac{dy}{dx} + \frac{dz}{dx}y = f(x)\\
$$
Por lo que la constante de integración no nos sirve.

La clase pasada vimos como obtener la diferencial total:
$$
df(x,y) = \frac{\delta f}{\delta x} dx + \frac{\delta f}{\delta y} dy
$$
Planteamos el problema y vemos como resolverlo.

Este método requiere de 15 pasos.

Supongamos que tenemos una función:
$$
C = f(x,y) = 3x^2y^2 + 2xy + 7x + 6y + 32\\
df(x,y) = (6xy^2 + 2y + 7) dx + (6x^2y + 2x + 6) dy = 0\\
(6x^2y + 2 x + 6) dy = -(6xy^2 + 2y + 7) dx\\
\frac{dy}{dx} = \frac{-(6xy^2 + 2y + 7)}{(6xy + 2x + 6)}
$$
Sabemos como llegar desde la diferencial total hasta el cociente, pero, ¿Acaso seremos capaces de llegar a la diferencial total si tenemos el cociente y resolver la ecuación?

Vamos a partir desde el cociente y tratar de obtener el resultado original a partir de esto:
$$
\frac{dy}{dx} = \frac{-(6xy^2 + 2y + 7)}{(6x^2y + 2x + 6)}\\
Despejamos \ los \ divisores:\\
(6x^2y + 2x + 6) dy = - (6xy^2 + 2y + 7) dx\\
Integramos \ cada \ lado \ de \ la \ igualdad:\\
\int (6x^2y + 2x + 6) dy = - \int (6xy^2 + 2y + 7) dx\\
Resultado:\\
\frac{6x^2y^2}{2} + 2xy + 6y = - (\frac{6x^2y^2}{2} + 2xy + 7x)\\
simplificamos:\\
3x^2y^2 + 2xy + 6y = -(3x^2y^2 + 2xy + 7x)\\
3x^2y^2 + 2xy + 6y = - 3x^2y^2 - 2xy - 7x\\
Entonces:\\
3x^2y^2 + 2xy + 7x + 6y + C
$$

# Ejercicios

1. $$
   2xy \ dx + (x^2 - 1) dy = 0
   $$

2. 

**Respuesta**
$$
2xy \ dx = - (x^2 - 1 ) \ dy\\
Inetgramos:\\
x^2y = -x^2y - y\\
f(x,y) = x^2y + y + C
$$

2. $$
   (e^{2y} - y \cos xy) \ dx + (2xe^{2y} - x \cos xy + 2y) \ dy = 0
   $$

3. 

**Respuesta**
$$
(e^{2y} - y \cos xy) \ dx = - (2xe^{2y} - x \cos xy + 2y) \ dy\\
derivamos \ sobre \ y \ para \ comprobar:\\
2e^{2y} - (xy \sin xy + \cos xy)\\
derivamos \ sobre \ x \ para \ comprobar:\\
xe^{2y} - (-xy \sin xy + \cos xy)\\
si \ es \ la \ misma, entonces, \ integramos:\\
\int (e^{2y} - y \cos xy) dx = xe^{2y} - y \frac{\sin xy}{y} + h(y)\\
\int (2xe^{2y} x \cos xy + 2y) \ dy = \frac{2xe^{2y}}{2} - x \frac{\sin xy}{x} + y^2 + g(x)\\
Entonces:
xe^{2y} - \sin xy + y^2 + C
$$




3. $$
   (5x + 4y)dx + (4x - 8y^3)dy = 0
   $$

**Respuesta**
$$
(5x + 4y)dx   = - (4x - 8y^3)dy\\
\int (5x + 4y)dx  = - \int (4x - 8y^3)dy\\
\frac{5x^2}{2} + 4yx = - 4xy + 2y^4\\
Entonces:\\
\frac{5x^2}{2} - 2y^4 + 4xy = C
$$


4. 

$$
(\tan x - \sin x \sin y ) \ dx + \cos x \cos y \ dy
$$







