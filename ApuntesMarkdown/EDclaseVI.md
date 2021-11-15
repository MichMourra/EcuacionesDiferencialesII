# Ecuaciones diferenciales VI

# Ecuaciones de Bernoulli

Si tenemos la derivada de un producto igual a una función de x, esa es una función diferencial que puedo resolver por variables separables pasando el x del otro lado e integrando de los dos lados.
$$
\frac{dzy}{dx} = f(x)\\
y = \frac{\int f(x)dx}{z}
$$


- Pero esta ecuación diferencial tambien se podria desarrollar de la siguiente manera


$$
\frac{dzy}{dx} = f(x)\\
z\frac{dy}{dx} + \frac{dz}{dx}y = f(x)\\
$$
- Por lo que esta ecuación tambien nos serviria para resolver las ecuaciones de esta forma:

$$
\frac{dy}{dx} + P(x)y = Q(x)\\
Deberdiamos \ \ multiplicar \ \ por \ \ z:\\
z\frac{dy}{dx} + zP(x)y = zQ(x)\\
Entonces:\\
\frac{dz}{dx} = zP(x)\\
\frac{dz}{z} = P(x)dx\\
\ln z \int P(x) dx z = e^{\int P(x) dx}\\
$$

- Esto quiere decir que si yo quiero resolver la ecuación, la tengo que multiplicar por un factor integrante. Una vez que la multiplico por un factor integrante, me queda la derivada de un producto que resuelvo con esta forma: $y = \frac{\int f(x)dx}{z}$

- Es lo que vimos en las dos clases anteriores
- El factor integrante es: $e^{\int P(x) dx}$
- No se puede simplificar la ecuación porque primero se tiene que encontrar la z.

Vamos a resolver las ecuaciones de Bernoulli convirtiéndolas en el tipo de ecuaciones que vimos anteriormente y resolverlas con el factor integrante.

**Ecuaciones Bernoulli**

$\frac{dy}{dx} + P_1(x)y = Q(x)y^n$

A diferencia de las ecuaciones que vimos, las ecuaciones Bernoulli tienen una potencia de y multiplicando al final de la igualdad. Esta propiedad las vuelve muy diferentes, por lo que ya no podemos aplicar el método directamente.

- Es una complicación muy grande

Para resolverlas tenemos que convertirla a la forma que conocemos: $\frac{dy}{dx} + P(x)y = Q(x)$

Para lograr convertirlas, debemos dividir toda la expresión entre $y^n$

Por lo que vamos a pasar el problema del otro lado.

- Dividir entre $y^n$ es lo mismo que multiplicar por $y^{-n}$, esto debido a que: $y^{-n} = \frac{1}{y^{n}}$
- Cuando tengo un producto donde hay exponentes con la misma base, se suman los exponentes.
- Al hacer el cambio creamos dos problemas en la parte izquierda de la ecuación.
- Para resolver este problema necesitamos hacer un cambio de variable: $u = y^{1-n}$
- ¿Cómo podemos despejar la y?
- Utilizamos la función inversa que es sacar raiz de $1-n$
- 

Este método de Bernoulli lo que hará es utilizar el método anterior. 
$$
\frac{dy}{dx} + P(x)y = Q_1(x)y^{n}\\
y^{-n} \cdot \frac{dy}{x} + P_1(x)y \cdot y^{-n} = Q_1(x)\\
y^{-n}\frac{dy}{dx} + P_1(x)y^{1-n} = Q_1(x)\\
Cambio \ \ de \ \ variable:\\
u = y^{1-n}\\
Raiz:\\
u^{\frac{1}{1-n}} = y
$$
Sustituimos las y por u
$$
u^{\frac{1}{1-n}} \cdot \frac{dy}{dx} + P_1(x) u = Q_1(x)
$$


Resolvemos derivando el valor de y en terminos de u por regla de la cadena, de modo que podamos obtener el valor de $\frac{dy}{dx}$:
$$
\frac{dy}{dx} = \frac{1}{1-n}u^{\frac{1}{1-n} - 1} \cdot \frac{du}{dx}
$$
Para realizar la resta de fracciones igualamos los denominadores:
$$
\frac{1}{1-n} - 1 = \frac{1}{1-n} - \left( \frac{1-n}{1-n}\right)\\
\frac{1-1-(-n)}{1-n} = \frac{n}{1-n}
$$

- Como tenemos la y, entonces necesitamos su derivada y sustituirla en la ecuación principal

Al realizar la resta de fracciones nos queda el exponente:
$$
\frac{dy}{dx} = \frac{1}{1-n}u^{\frac{n}{1-n}} \cdot \frac{du}{dx}
$$

Tenemos que : $y^{-n} = u^{-\frac{n}{1-n}}$

### Resolver la ecuación:

Sustituimos todo por los valores que obtuvimos con anterioridad
$$
y^{-n}\frac{dy}{dx} + P_1(x)y^{1-n} = Q_1(x)\\
\frac{1}{1-n} \cdot u^{-\frac{n}{1-n}} \cdot u^{\frac{n}{1-n}} \cdot \frac{du}{dx} + P_1(x)u = Q_1(x)\\
$$

- Al sumar los exponentes nos da 0, por lo tanto se eliminan las u con exponente:
  $$
  \frac{1}{1-n} \cdot \frac{du}{dx} + P_1(x)u = Q_1(x)
  $$

- Ahora multiplicamos todo por $1-n$ para eliminar la fracción $\frac{1}{1-n}$

$$
\frac{du}{dx} + (1-n)P_1(x)u = (1-n)Q_1(x)
$$

- De este modo ya tenemos la forma de la ecuación que sabemos resolver por medio del factor integrante.
- Con esto ya sabemos resolver ecuaciones de Bernoulli

## Ejemplo

1. $\frac{dy}{dx} + \frac{1}{x} y = xy^2$

Este es un tipo de ecuación que no sabríamos resolver, pero al ver que hay una potencia de y multiplicando al final, sabemos que es una ecuación de Bernoulli.

- Hacemos nuestro cambio de variable sabiendo que n vale 2

$$
Sabemos \ \ que:\\
u = y^{1-n}\\
Entonces:\\
u = y^{1-2} = y^{-1} = \frac{1}{y}\\
y = \frac{1}{u} = u^{-1}
$$

- Obtenemos el valor de la derivada de la y, ya que tambien lo necesitaremos

$$
\frac{dy}{dx} = - u^{-2} \frac{du}{dx}
$$

- Ya que calculamos el cambio de variable que vamos a emplear y su respectiva derivada. Entonces procedemos a sustituir los valores en la ecuación.

$$
\frac{dy}{dx} + \frac{1}{x} y = xy^2\\
-u^2 \frac{du}{dx} + \frac{1}{x}u^{-1} = xu^{-2}\\
Dividimos \ \ entre \ \ u^{-2}\\
-\frac{du}{dx} - \frac{1}{x}u = -x\\
Ya \ \ tenemos \ \ la \ \ forma:\\
\frac{du}{dx} + P(x)u = Q(x)\\
$$
Ahora que ya tenemos la forma general que sabemos resolver, entonces buscamos un factor integrante.

Debemos encontrar el factor integrante:
$$
\frac{du}{dx} - \frac{1}{x}u = -x\\
I=Z=e^{\int P(x)dx}\\
z = e^{\int - \frac{1}{x} dx} = e^{-\int \frac{1}{x} dx} = e^{-\ln x} = e^{\ln x^{-1}} = x^{-1} = \frac{1}{x}\\
$$

- Una vez que tenemos el factor integrante, multiplicamos la expresión por el y la resolvemos.

$$
x^{-1} \cdot \frac{du}{dx} - x^{-2}u = -1\\
\frac{dx^{-1}u}{dx} = -1\\
Integro \ \ de \ \ los \ \ dos \ \ lados:\\
\int dx^{-1}u = -\int dx = -x + C\\
x^{-1}u = -x + C\\
u = -x^{2} + Cx\\
$$

Sustituimos con y:
$$
\frac{1}{y} = -x^{2} + Cx\\
Entonces:\\
y = \frac{1}{Cx-x^2}
$$

## Ejercicios

1. $$
   \frac{dy}{dx} + \frac{1}{x}y = \frac{2}{x}y^{-2}
   $$



Obtener factor integrante:
$$
I = e^{\int P(x)dx} = e^{3\int \frac{dx}{x}} = e^{3 \ln x} = e^{\ln x^3} = x^3
$$

Hacemos el cambio de variable:
$$
u = y^{1-n}\\
u = y^{1-(-2)} = y^{3}\\
y = u^{\frac{1}{3}}\\
y^{-2} = u^{-\frac{2}{3}}\\
\frac{dy}{dx} = \frac{1}{3}u^{-\frac{2}{3}} \frac{du}{dx}
$$
Factor Integrante:
$$
I = e^{3\ln x} = e^{\ln x^3} = x^3
$$


Respuesta:
$$
\frac{1}{3}u^{-\frac{2}{3}}\frac{du}{dx} + \frac{1}{x}u^{\frac{1}{3}} = \frac{2}{x} u ^{-\frac{2}{3}}\\
 Multiplicamos \ \ todo \ \ por \ \ x3u^{\frac{2}{3}}\\
\frac{du}{dx} + \frac{3}{x}u = \frac{6}{x}\\
Multiplicamos \ \ por \ \ el \ \ factor \ \ integrante:\\
x^3 \frac{du}{dx} + 3x^2u = 6x^2\\
\frac{dx^3u}{dx} = 6x^2\\
dx^3u = 6x^2dx\\
Integramos:\\
\int dx^3u = \int 6x^2dx\\
x^3u = 2x^3 + C\\
despejamos:\\
u = \frac{2x^3}{x^3} + \frac{C}{x^3}
u = 2 + \frac{C}{x^3}
$$

Sustituimos el valor de u por lo que vale en y:

$y^3 = 2 + \frac{C}{x^3}$


-----------------------------------------------------------------------------

2. $$
   \frac{dy}{dx} + y = xy^4
   $$

Hacemos el cambio de variable:
$$
u = y^{1-n} = y^{-3} = \frac{1}{y^3}\\
y = u^{-\frac{1}{3}}\\
y^{4} = u^{-\frac{4}{3}}\\
\frac{dy}{dx} = -\frac{1}{3}u^{-\frac{4}{3}} \frac{du}{dx}\\
\frac{du}{dx} - 3u = -3x
$$
Factor integrante:
$$
I = e^{- 3\int dx} = e^{-3x}
$$
Entonces:
$$
e^{-3x} \frac{du}{dx} -3 e^{-3x} u = -3xe^{-3x}
$$
Se hace con una integral por partes

Respuesta:
$$
u = y^{1-n} = y ^{-3} = \frac{1}{y^3}\\
y = u^{-\frac{1}{3}}\\
y^{4} = u^{-\frac{4}{3}}\\
\frac{dy}{dx} = - \frac{1}{3}u^{\frac{4}{3}}\frac{du}{dx}\\
-\frac{1}{3}u^{-\frac{4}{3}} \frac{du}{dx} - 3 u = -3x\\
e^{-3x} \frac{du}{dx} - 3e^{-3x}u = -3x^{-3x}\\
$$




-------------------------------------------------------------------------------------

3. $$
   \frac{dy}{dx} - \frac{1}{x}y = \frac{1}{x^2} 
   $$

Hacemos el cambio de variable:
$$
u = y^{1-n}\\
u = \frac{1}{y} = y^{-1}\\
y = \frac{1}{u} = u^{-1}\\
\frac{dy}{dx} = -u^{-2} \cdot \frac{du}{dx}
$$


Respuesta:
$$
\frac{dy}{dx} - \frac{1}{x}y = -\frac{1}{x}y^{2}\\
Sustituimos \ \ con \ \ u:\\
- u^{2}\frac{dy}{dx} - \frac{1}{x}u^{-1} = -\frac{1}{x^2}u^{-2}\\
Dividimos \ \ entre \ \ u^{-2}\\
\frac{du}{dx} + \frac{1}{x}u = \frac{1}{x^2}\\
La \ \ ecuación \ \ ya \ \ es \ \ de \ \ la \ \ forma\\
Obtenemos \ \ factor \ \ integrante:\\
I = e^{\int \frac{1}{x} dx} = e^{\ln x} = x\\
x\frac{du}{dx} + u = \frac{1}{x}
$$

Esto quiere decir que:
$$
\frac{dxu}{dx} = \frac{1}{x}\\
dxu = \frac{dx}{x}\\
Integramos:\\
\int dxu = \int \frac{dx}{x}\\
xu = \ln x + C\\
u = \frac{\ln x}{x} + \frac{C}{x}\\
$$
Sustituimos el valor de u en y:
$$
\frac{1}{y} = \frac{\ln x}{x} + \frac{C}{x}\\
y = \frac{x}{\ln x} + \frac{x}{C}
$$
o tambien:

$\frac{x}{y} = \ln x + C$





