# Ecuaciones diferenciales

$$
\frac{d^2y}{dx^2} + (\frac{dy}{dx})^2 + 1 = 0 \\
u = \frac{dy}{dx}\\
\frac{du}{dx} = \frac{d^2y}{dx^2}\\
\frac{du}{dx} + u^2 + 1 = 0\\
\frac{du}{dx} = -1 -u^2 = -(u^2 + 1)\\
\int \frac{du}{u^2 + 1} = - \int dx\\
ang \tan u = -x + C\\
u = \tan (-x + C)\\
u = \frac{\sin (-x + C)}{\cos(-x + C)}\\
\frac{dy}{dx} = \frac{(\sin (-x + C))}{\cos (-x + C)}\\
\frac{dy}{dx} = \frac{\sin (-x + C)}{\cos (-x + C)}\\
z = \cos (-x + C)\\
\frac{dz}{dx} = -\sin (-x + C)\\
dz = - \sin (-x + C)\\
\int dy = \int \frac{\sin(-x + C)}{\cos (-x + C)} dx\\
y = -\int \frac{dz}{z} = \ln z + C\\
y = - \ln (\cos (-x + C)) + C_2
$$

# Transformadas de Laplace

Uno de los axiomas de la probabilidad nos dice que la suma de todas las probabilidades es igual a 1.

La transformada de La place es parte de lo que se conocen como transformadas de integrales.
$$
\int_0^\infty f(x) dx = 1\\
e^{-x}
\int K(s , t) f(t) dt\\
Transformada \ de \ Fourier\\
\frac{e^{ist}}{\sqrt{2\pi}}\\
$$
La transformada de La place es en si :
$$
L\{ f(t)\} = \int_0^\infty e^{-st} f(t) dt = F(s)\\
f(t) = 1 \\
\int_0^\infty e^{-st} dt = \frac{e^{-st}}{-s} \\
|_0^\infty = 0 - (\frac{1}{-s}) = \frac{1}{s}\\
L\{1\} = \frac{1}{s}
$$
La transformada de Laplace transforma una función F(t) en una forma F(s)
$$
L \{ f(t)\} = \int_0^\infty e^{-st} f(t) dt\\
f(t) = t \int e^{-st} dt\\
t\frac{e^{-st}}{-s} - \frac{e^{-st}}{s^2} \\
$$


## Transformada de la segunda derivada

$$
L\{ \frac{d^2f(t)}{dt^2}\} = \int_0^\infty e^{-st \frac{d^2 f(t)}{dt^2}}dt \\
u = e^{-st}\\
du = se^{-st}dt
dv = \frac{d^2f(t)}{dt^2}\\
v = \frac{df(t)}{dt}\\
e^{-st} \frac{df(t)}{dt} |_0^\infty  - \int_0^\infty - e^-st \frac{df(t)}{dt^2}
$$

