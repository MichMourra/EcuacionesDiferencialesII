# Ecuaciones diferenciales 2

# Clase V



## Variación de parámetros con factor integrante

$$
\frac{dy(x)}{dx} = f(x) \\
y = f(x)dx \\
 \frac{dzy}{dx} = f(x) \\
dzy = f(x)dx \\
\int dzy = f(x)dx \\
zy = \int f(x)dx \\
y = \frac{\int f(x)dx}{z}\\
esto \ no \ siempre \ ocurrira \\
z\frac{dy}{dx} + \frac{dz}{dx} y = f(x) \\
por \ lo  \ que \ la \ ecuacion \ mas \ general \ tendra \ la \ forma: \\
\frac{dy}{dx} + P(x)y = Q(x) \\
Z\frac{dy}{dx} + zP(x)y = zQ(x)\\

\frac{dz}{z} = p(x)dx\\
\int \frac{dz}{z} = \int P(x)dx\\
\ln z = \int P(x) dx \\
e^{\ln z} = e^{\int P(x) dx} \\
obtenemos \ el \ factor \ integrante: \\
I = z = e^{\int P(x)dx}
$$



### Ejercicio 

Tenemos un ejercicio respecto al cambio de glucosa en la sangre respecto al tiempo:

a = tasa constante de ingreso de glucosa

K = tasa de eliminación proporcional a la glucosa presente

De este modo planteamos la ecuación:
$$
\frac{dG(t)}{dt} = a - KG \\
\frac{dG}{dt} + KG = a \\
\frac{dG}{dt} + PG = Q \\
I = e^{\int Kdt} = e^{Kt}
$$
La ecuación diferencial que queremos resolver es 
$$
\frac{dG}{dt} + KG = a \\
$$
Por este motivo debemos multiplicarla por el factor integrante:
$$
e^{Kt}\frac{dG}{dt} + Ke^{Kt}G = e^{Kt}a \\
\frac{de^{Kt}G}{dt} = ae^{Kt} \\
Despejamos \\
de^{Kt}G = ae^{Kt}dt \\
Integramos \\
\int de^{Kt}G = \int ae^{Kt}dt \\
Despejamos \ Glucosa: \\
G = \frac{\frac{a}{k} e^{kt} + C}{e^{kt}}
$$

### Ejercicio

$$
x \frac{dy}{dx} + 6y + 2x^4 = 0 \\
\frac{dy}{dx} + P(x)y = Q(x) \\
x \frac{dy}{dx} + 6y = -2x^4 \\
\frac{dy}{dx} + \frac{6}{x}y = -2x^3
$$

Ahora podemos resolverla multiplicando por el factor integrante:
$$
I = e^{\int P(x) dx} = e^{\frac{6}{x}dx} = e^{6\int \frac{dx}{x}} = e^{6 \ln x} = e^{\ln x^{6}} = x^6
$$
Multiplicamos:
$$
x^6 \cdot \frac{dy}{dx} + x^6 \cdot \frac{6}{x}y = x^6 \cdot -2x^3 \\
x^6  \frac{dy}{dx} + x^6 \frac{6}{x}y =  -2x^9
$$
Despejamos y:

.

.

.

### Integral necesaria para el ejercicio 4

$$
\int \sec \theta d \theta = \\
\int \frac{du}{u} = \ln u \\
conocemos \ que: \\
\frac{d \sec \theta}{d \theta} = \sec \theta \tan \theta \\
\frac{d \tan \theta}{d \theta} = \sec^2 \theta \\
\int \frac{(tan \theta + \sec \theta) \sec \theta d \theta}{(\tan \theta + \sec \theta)} \\
\int \frac{\sec^2 \theta + \sec \theta \tan \theta}{(\tan \theta + \sec \theta)} d\theta \\
resultado: \\
\ln(\tan \theta + \sec \theta) + C
$$





### Ejercicios

1. $$
   x \frac{dy}{dx} + 5y = x^2
   $$

Respuesta:

Dividimos entre x
$$
\frac{dy}{dx} + \frac{5}{x}y = x \\
$$
obtenemos el factor de integración:
$$
I = e^{\int P(x) dx} = e^{\frac{5}{x}dx} = e^{5\int \frac{dx}{x}} = e^{5 \ln x} = e^{\ln x^{5}} = x^5
$$
multiplicamos:
$$
x^5 \cdot \frac{dy}{dx} + x^5 \cdot \frac{5}{x}y = x^5 \cdot x \\
x^5  \frac{dy}{dx} + x^5 \frac{5}{x}y = x^6 \\
x^5  \frac{dy}{dx} + 5x^4y = x^6 \\
$$
Despejamos y:





-------------------------------------------------------------

2. $$
   \cos x \frac{dy}{dx} + (\sin x)y = 1
   $$

Respuesta:

dividimos todo entre coseno
$$
\frac{dy}{dx} + \frac{\sin x}{\cos x} y = \frac{1}{\cos x} \\
P(x) = \cos x \\
u = \cos x \ \ \ \ du = -\sin dx \\
I = e^{\int P(x) dx} = e^{\int \frac{\sin x}{\cos x}dx} = e^{\int -\frac{du}{u}} = e^{-\ln u} = e^{- \ln (\cos)} = e^{- \ln (\cos)^{-1}} = \sec x = \frac{1}{\cos x}
$$
Multiplicamos por el factor integral:
$$
\frac{1}{\cos x} \cdot\frac{dy}{dx} + \frac{1}{\cos x} \cdot \frac{\sin x}{\cos x} y =  \frac{1}{\cos^2 x} \\
\sec x\frac{dy}{dx} + \sec x \tan x \ y =  \sec^2 x \\
Tenemos \ que: \\
\frac{d(\sec x) y}{dx} = \sec^2 x \\
Integramos: \\
\int d(\sec x) y = \int \sec^2 x dx \\
y = \frac{\tan x + C}{\sec x} = \frac{\frac{\sin x}{\cos x}}{\frac{1}{\cos x} + \frac{C}{\frac{1}{\cos x}}}
$$




-------------------------------------------------------------------------------------------------------------------------------------

3. $$
   \frac{dy}{dx} + 2xy - e^{-x^2} = 0
   $$

   





------------------------------------------------------------------------------------------------------------------

4. $$
   \frac{dr}{d\theta} + r\sec \theta = \cos \theta
   $$

Respuesta:

Factor integrante:
$$
I = e^{\int \sec \theta d \theta} = e^{\ln (\sec \theta + \tan \theta)} = (\sec \theta + \tan \theta) \\
$$
Resolución:
$$
(\sec \theta + \tan \theta) \frac{dr}{d\theta} + (\sec^2 \theta + \sec \theta\tan \theta) r\\
 d(\sec \theta + \tan \theta) = \cos \theta (\sec \theta + \tan \theta) \\
 (\sec \theta + \tan \theta)r = \int (1 + \sin \theta)d \theta = \\
 resultado: \\
 \theta - \cos \theta + C
$$

$$

$$




---------------------------------------------------------------------------