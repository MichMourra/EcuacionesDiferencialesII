# Ecuaciones diferenciales VI



# Ecuaciones de Bernoulli


$$
\frac{dzy}{dx} = f(x)\\
z\frac{dy}{dx} + \frac{dz}{dx}y = f(x)\\
\frac{dy}{dx} + P(x)y = Q(x)\\
z\frac{dy}{dx} + zP(x)y = zQ(x)\\
\frac{dz}{dx} = zP(x)\\
\frac{}{}\\
$$
Este metodo de bernoulli lo que hara es utilizar el metodo anterior
$$
\frac{dy}{dx} + P(x)y = Q_1(x)y^{n}\\
y^{-n} \frac{dy}{x} + P_1(x)yy^{-n} = Q_1(x)\\
y^{-n} = \frac{1}{y^{n}}\\
y^{-n}\frac{dy}{dx} + P_1(x)y^{1-n} = Q_1(x)\\
u = y^{1-n}\\
u^{\frac{1}{1-n}} = y
$$
Resolvemos derivando y por regla de la cadena:
$$
\frac{dy}{dx} = \frac{1}{1-n}u^{\frac{1}{1-n} - 1} \cdot \frac{du}{dx}
$$
Al realizar la resta de fracciones nos queda el exponente:
$$
\frac{dy}{dx} = \frac{1}{1-n}u^{\frac{n}{1-n}} \cdot \frac{du}{dx}
$$

### Resolver la ecuación:

Sustituimos todo por los valores que obtuvimos con anterioridad
$$
y^{-n}\frac{dy}{dx} + P_1(x)y^{1-n} = Q_1(x)\\
u^{-\frac{n}{1-n}} \cdot \frac{1}{1-n}u^{\frac{n}{1-n}} \cdot \frac{du}{dx} + P(x)u = Q_1(x)\\
\frac{1}{1-n} \cdot \frac{du}{dx} + P_1(x)u = Q_1(x)
$$

$$
\frac{dy}{dx} + \frac{1}{x} y = xy^2\\
-u^2 \frac{du}{dx} + \frac{1}{x}u^{-1} = xu^{-2}\\
-\frac{du}{dx} - \frac{1}{x}u = -x\\
\frac{du}{dx} + P(x)u = Q(x)\\
$$
Debemos encontrar el factor integral:
$$
\frac{du}{dx} - \frac{1}{x}u = -x\\
I=Z=e^{\int P(x)dx}\\
z = e^{\int - \frac{1}{x} dx} = e^{-\int \frac{1}{x} dx} = e^{-\ln x} = e^{\ln x^{-1}} = x^{-1} = \frac{1}{x}\\
x^{-1}\frac{}{}
$$


## Ejercicios

1. $$
   \frac{dy}{dx} + \frac{1}{x}y = \frac{2}{x}y^{-2}
   $$



Obtener factor integrante:
$$
I = e^{\int P(x)dx} = e^{3\int \frac{dx}{x}} = e^{3 \ln x} = e^{\ln x^3} = x^3
$$


Respuesta:
$$
\frac{1}{3}u^{-\frac{2}{3}}\frac{du}{dx} + \frac{1}{x}u^{\frac{1}{3}} = \frac{2}{x} u ^{-\frac{2}{3}}\\
x3u^{\frac{2}{3}}\\
\frac{du}{dx} + \frac{3}{x}u = \frac{6}{x}\\
x^3 \frac{du}{dx} + 3x^2u = 6x^2\\
\frac{dx^3u}{dx} = 6x^2\\
dx^3u = 6x^2dx\\
x^3u = 2x^3 + C
$$






-----------------------------------------------------------------------------

2. $$
   \frac{dy}{dx} + y = xy^4
   $$

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

Respuesta:
$$
\frac{dy}{dx} - \frac{1}{x}y = -\frac{1}{x}y^{2}\\
- u^{2}\frac{dy}{dx} - \frac{1}{x}u^{-1} = -\frac{1}{x^2}u^{-2}\\
\frac{du}{dx} + \frac{1}{x}u = \frac{1}{x^2}\\
I = e^{\int \frac{1}{x} dx} = e^{\ln x} = x\\
x\frac{du}{dx} + u = \frac{1}{x}
$$








