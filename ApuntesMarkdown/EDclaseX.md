# Ecuaciones diferenciales 

# clase X

# Demostración de las homogéneas de grado Alpha

Habíamos planteado este ejercicio:
$$
xdx + (y - 2x)dy = 0
$$

- Lo primero que habíamos planteado para resolver estas ecuaciones, es un método para solución de ecuaciones exactas lo cual se comprobaba con derivadas parciales.
- Al ver que no es una ecuación exacta, entonces tratamos de resolverla como una homogénea de grado Alpha con grado 1.
- Lo haremos con la siguiente formula.

$$
\alpha = 1\\
M(x,y)\\
M(tx,ty) = t^{\alpha}M(x,y)\\
$$

- Hacemos un cabio de variable

$$
y = ux\\
dy = udx + xdu\\
Sustituimos \ \ con \ \ u:\\
xdx + (ux - 2x)(udx + xdu) = 0\\
Desarrollamos:\\
xdx + u^2xdx + ux^2du - 2xudx - 2x^2du = 0\\
Pasamos \ \ dx \ \ y \ \ du \ \ de \ \ cada \ \ lado:\\
(x + u^2x -2xu)dx = (2x^2 - ux^2)du\\
x(u^2 - 2u + 1)dx = x^2(2-u)du\\
Divorciamos \ \ variables:\\
\frac{x}{x^2} dx = \frac{(2-u)}{(u-1)^2}du\\
Simplificamos:\\
\frac{dx}{x} = \frac{2-u}{(u-1)^2}du\\
integramos \ \ de \ \ los \ \ 2 \ \ lados:\\
\ln x = \int \frac{2-u}{(u-1)^2}du = - \int \frac{u-2}{(u-1)^2}du = - \int \frac{(u -1 - 1)}{(u-1)^2}du\\
= - \int \left( \frac{u - 1}{(u-1)^2} - \frac{1}{(u-1)^2}\right) du\\
- \int \frac{du}{u-1} + \int \frac{1}{(u-1)^2}du\\
$$

- Como la integral es complicada hacemos otro cambio de variable:

$$
Otro \ \ cambio \ \ de \ \ variable:\\
z = u-1\\
dz = du\\
- \int \frac{dz}{z} + \int z^{-2}dz = - \ln z + \frac{z^{-1}}{-1}
$$

- Revertimos los cambios de variable para volver a nuestra variable original

$$
\ln x = - \ln z - \frac{1}{z}\\
Volvemos \ \ a \ \ u:\\
\ln x = - \ln (u -1) - \frac{1}{u-1}\\
u = \frac{y}{x}\\
\ln x = - \ln(\frac{y}{x} - 1) - \frac{1}{\frac{y}{x} - 1}
$$

- Esta ya es una respuesta
- Pero podemos simplificar la ecuación para que se vea mas bonita.
- Nunca resolvimos homogéneas de grado 2.
- Vamos a demostrar el método y demostraremos porque funciona si es homogénea de grado Alpha.
- La demostración es fea, ya que terminas y no sientes sensación de alivio, sino que mas bien parece un final abierto jaja.

## Demostración

La demostración la haremos a partir de la ecuación general:
$$
M(x,y)dx + N(x,y)dy = 0
$$

- La podemos resolver si y solo si: $M(x,y)$ y $N(x,y)$ son homogéneas de grado Alpha.
- Es decir que si yo multiplicara las variables por t: $M(tx,ty) = t^{\alpha} M(x,y)$ y $N(tx,ty) = t^{\alpha} N(x,y)$
- Para resolver esto se planteaba el cambio de variable $y = ux$ , $dy = udx + xdu$
- Ahora cuando hacemos el cambio de variable nos queda $M(x,ux)$ y $N(x,ux)$
- Quedan expresiones de la forma $M(x \cdot1,x \cdot u)$ y $N(x \cdot1,x \cdot u)$
- Si en lugar de poner una t, hubiéramos puesto una x nos damos cuenta de que tienen la misma forma.
- Entonces podemos sacar x con un exponente Alpha al igual que t.
- Nos queda: $x^{\alpha} M(1,u)$
- Nos queda: $x^{\alpha} N(1,u)$
- Por eso es necesario que M y N sean homogéneas de grado Alpha.
- El resto es pura algebra ya que sustituiremos estos valores en la ecuación inicial.

### Parte algebraica

$$
M(x,y)dx + N(x,y)dy = 0\\
M(x,ux)dx + N(x,ux)dy = 0\\
x^{\alpha}M(1,u)dx + x^{\alpha}N(1,u)dy = 0\\
x^{\alpha}(M(1,u)dx + N(1,u)(udx + udu)) = 0\\
Dividir \ \ todo \ \ entre \ \ x^{\alpha}:\\
M(1,u)dx + N(1,u)udx + N(1,u)xdu = 0\\
(M(1,u) + N(1,u)u)dx = - N(1,u)xdu\\
Separar \ \ dx \ \ y \ \ du:\\
\frac{dx}{x} = \frac{-N(1,u)}{M(1,u) + N(1,u)u} du\\
$$

- Como la ecuación era homogénea de grado Alpha pudo ser posible convertirla en una función con du.

$$
\ln x = - \int \frac{N(1 - u)du}{N(1,u) + N(1,u)u}\\
$$

- Cuando usamos el método no necesitamos hacer la demostración porque ya esta demostrada.
- Probamos que el método sirve cuando están presentes las dos condiciones.

# Ecuaciones no lineales

- Hasta ahorita todas las ecuaciones que hemos resuelto eran de estas formas:

$$
a_1\frac{d^2y}{dx^2} + a_2 \frac{dy}{dx} + a_3y = 0\\
\frac{dy}{dx} + P(x)y = Q(x)
$$

- Todas las ecuaciones que hemos abordado son ecuaciones donde las derivadas están elevadas a la primera potencia.
- No hemos visto por ejemplo que pasaría si la derivada estuviera al cuadrado.

**Ejemplo**
$$
\left( \frac{dy}{dx} \right)^2 + P(x)y = Q(x)
$$

- Por este motivo se dice que las ecuaciones que habíamos estudiado antes eran lineales.
- Este tema es consecuencia de un examen de admisión a la unión europea.

## Resolución

- Si no hay $y$ hacemos este cambio de variable:
  - $u = \frac{dy}{dx}$
  - Desaparecer la y
  - $\frac{du}{dx} = \frac{d^2}{dx^2}$
- Si hay $y$ hacemos este cambio de variable:
  - $u = \frac{dy}{dx}$
  - Desaparecer la x
  - $\frac{du}{dx} = \frac{du}{dx} \frac{dy}{dy} = \frac{du}{dy} \frac{dy}{dx} = \frac{du}{dy}u$

### Ejercicio sin $y$

$$
\frac{d^2y}{dx^2} = 2x\left( \frac{dy}{dx}\right)^2\\
\frac{du}{dx} = 2x u^2\\
$$

Como en el ejercicio no hay una $y$ suelta, sino que todas están dentro de las diferenciales, entonces usamos el caso de no hay $y$
$$
\frac{d^2y}{dx^2} = 2x\left( \frac{dy}{dx}\right)^2\\
Cambio \ \ de \ \ variable:\\
u = \frac{dy}{dx} \frac{du}{dx} = \frac{d^2y}{dx^2}\\
\frac{du}{dx} = 2x u^2\\
separamos \ \ x \ \ , \ \ u:\\
u^{-2}du = 2xdx\\
Integramos:\\
\int u^{-2} du = \int 2x dx\\
\frac{u^{-1}}{-1} = x^2 + C\\
-\frac{1}{u} = x^2 + C\\
- \frac{1}{x^2 + C} = u = \frac{dy}{dx}\\
\int \frac{-dx}{x^2 + C} = \int dy = y\\
$$

- Tras resolver la integral nos queda:

$$
y = - \frac{1}{c} ang \tan \frac{x}{c} + C
$$



### Ejercicio con $y$

- En este caso la segunda derivada será un caso diferente al anterior.
- Utilizamos la propiedad conmutativa.
- Se multiplica por $u$ para llegar a la formula que vamos a usar. 

**Cambio de variable**
$$
u = \frac{dy}{du}\\
\frac{du}{dx} = \frac{du}{dx} \frac{dy}{dy} = \frac{du}{dy} \frac{dy}{dx} = \frac{du}{dy}u\\
\frac{du}{dx} = \frac{du}{dy}u\\
$$
**Ejercicio**
$$
y \frac{d^2y}{dx^2} = \left( \frac{dy}{dx}\right)^2
$$
**Segunda derivada**

- El problema lo resolveremos haciendo la sustitución de la derivada por la $u$
- Si la $u$ es la primera derivada, la segunda derivada es la derivada de la $u$.

$$
\frac{d^2y}{dx^2} = \frac{du}{dx} = \frac{du}{dy}u
$$

**Solución problema**


$$
y\frac{du}{dy}u = u^2\\
\frac{du \ u }{u^2} = \frac{dy}{y} \rightarrow \frac{du}{u} = \frac{dy}{y}\\
\ln u = \ln y + C\\
Despejamos \ \ u \ \ con \ \ exponencial:\\
u = e^{\ln y + C} = e^{C} e^{\ln y} = ky \\
\frac{dy}{dx} = ky\\
\frac{dy}{y} = kdx
$$

- Ahora volvemos a integrar por los dos lados y vamos a obtener la respuesta:

$$
\int \frac{dy}{y} = \int kdx\\
\ln y = kx + C
$$



## Ejercicios

- Primero debemos cuestionarnos si hay $y$ o no, de este modo sabremos que cambio de variable aplicar.

1. $\frac{d^2y}{dx^2} + \left( \frac{dy}{dx}\right)^2 + 1 = 0$

**Respuesta**

$y = \ln (ilegible)$



--------------------------------------------------------------

2. $x^2 \frac{d^2y}{dx^2} + 2y \left( \frac{dy}{dx}\right)^2 = 0$

**Respuesta**

$y = \frac{1}{C_1} \ln (C_1 x + 1) + \frac{1}{C_1}x + C_2$



-------------------------------------------------------

3. $\frac{d^2y}{dx^2} + 2y \left( \frac{dy}{dx}\right)^3 = 0$

**Respuesta**

$\frac{y^3}{3} - C_1y = x + C_2$

