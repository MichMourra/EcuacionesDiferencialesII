# Ecuaciones diferenciales 2

# Clase V

## Variación de parámetros con factor integrante

El método Bernoulli lo que hace es que es una ecuación que depende de este método, es decir es una variante. El método Bernoulli tiene una potencia de la x del lado derecho de la ecuación, lo cual, es una característica especial.




$$
\frac{dy(x)}{dx} = f(x) \\
Despejamos \ \ para \ \ encontrar \ \ y:\\
y = f(x)dx \\
Integramos \ \ de \ \ ambos \ \ lados \ \ para \ \ encontrar \ \ y:\\
\int dy(x) = \int f(x) dx\\
y = f(x) dx\\
$$



- Este resultado lo usamos la vez pasada para estudiar la derivada de un producto como: $z \cdot y$

$$
\frac{dzy}{dx} = f(x) \\
dzy = f(x)dx \\
Integramos \ \ para \ \ obtener \ \ el \ \ valor \ \ del \ \ producto:\\
\int dzy = f(x)dx \\
zy = \int f(x)dx \\
Despejamos \ \ y:\\
y = \frac{\int f(x)dx}{z}\\
$$

Pero por otro lado tenemos que la derivada de un producto es igual a $z\frac{dy}{dx} + \frac{dz}{dx}y = f(x)$

- Por lo que si tenemos una ecuación diferencial de esta forma, la podemos escribir como la derivada de un producto y resolverlo con la formula del valor de y que sacamos anteriormente.
- Pero estas ecuaciones diferenciales no serian practicas, por lo que necesitamos una forma mas general, mas practica en donde $P(x)$ y $Q(x)$  pueden ser cualquier función y no tenemos ninguna derivada de un producto.

$$
por \ lo  \ que \ la \ ecuacion \ mas \ general \ tendra \ la \ forma: \\
\frac{dy}{dx} + P(x)y = Q(x) \\
Pero \ \ no \ \ es \ \ la \ \ misma\\
si \ \ multiplico \ \ todo \ \ por \ \  z \ \ tendria \ \ la \ \ misma:\\
Z\frac{dy}{dx} + zP(x)y = zQ(x)\\
Entonces:\\
\frac{dz}{dx} = zP(x)
$$

- Pero, no todas las formulas las puedo escribir como la derivada de un producto.
- Por lo que para poder escribir las ecuaciones de la forma: $\frac{dy}{dx} + P(x)y = Q(x)$
- Se necesitaria tener algo que multiplicara todo, lo cual es el factor integrante.
- Entonces debemos encontrar la z que es el factor integrante.

$$
Divorciamos \ \ variables:\\
\frac{dz}{z} = p(x)dx\\
Integramos \ \ de \ \ los \ \ dos \ \ lados:\\
\int \frac{dz}{z} = \int P(x)dx\\
\ln z = \int P(x) dx \\
e^{\ln z} = e^{\int P(x) dx} \\
obtenemos \ el \ factor \ integrante: \\
I = z = e^{\int P(x)dx}
$$

- Teniendo esta derivada del producto, puedo aprovechar que ya se como encontrar la respuesta:
- $y = \frac{\int f(x)dx}{z}$
- Pero $f(x)$ ya no es la que teniamos inicialmente, ahora es 

### Ejercicio Glucosa

Tenemos un ejercicio respecto al cambio de glucosa en la sangre respecto al tiempo:

a = tasa constante de ingreso de glucosa

K = tasa de eliminación proporcional a la glucosa presente

De este modo planteamos la ecuación:
$$
\frac{dG(t)}{dt} = a - KG \\
\frac{dG}{dt} + KG = a \\
Planteamos \ \ la \ \ ecuación \ \ general:\\
\frac{dG}{dt} + PG = Q \\
Obtenemos \ \ factor \ \ integrante:\\
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
G = \frac{\frac{a}{k} e^{kt} + C}{e^{kt}}\\
G = \frac{a}{k} + \frac{C}{e^{kt}}
$$

### Ejercicio

$$
x \frac{dy}{dx} + 6y + 2x^4 = 0 \\
El \ \ modelo:\\
\frac{dy}{dx} + P(x)y = Q(x) \\
Tenemos \ \ que \ \ transformarlo \ \ al \ \ modelo\\
x \frac{dy}{dx} + 6y = -2x^4 \\
Dividimos \ \ entre \ \ x \ \ para \ \ que \ \ tenga \ \ la \ \ forma:\\
\frac{dy}{dx} + \frac{6}{x}y = -2x^3
$$

Ahora podemos resolverla multiplicando por el factor integrante:
$$
I = e^{\int P(x) dx} = e^{\frac{6}{x}dx} = e^{6\int \frac{dx}{x}} = e^{6 \ln x} = e^{\ln x^{6}} = x^6
$$
Multiplicamos:
$$
x^6 \cdot \frac{dy}{dx} + x^6 \cdot \frac{6}{x}y = x^6 \cdot -2x^3 \\
x^6  \frac{dy}{dx} + x^6 \frac{6}{x}y =  -2x^9\\
x^6  \frac{dy}{dx} +  6x^5y =  -2x^9
$$
Despejamos y:

$$
Reducimos:\\
\frac{dx^6y}{dx} = -2x^9\\
Integramos:\\
\int \frac{dx^6y}{dx} = \int -2x^9\\
x^6y = \frac{-2x^{10}}{10} + C\\
y = \frac{-2x^{10}}{10x^6} + \frac{C}{x^6}\\
y = \frac{-2x^4}{10} + \frac{C}{x^6}
$$


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
$$
Simplificamos:\\
\frac{dx^5y}{dx} = x^6\\
integramos \ \ a \ \ ambos \ \ lados:\\
\int \frac{dx^5y}{dx} = \int x^6\\
x^5y = \frac{x^7}{7} + C\\
Despejamos:\\
y = \frac{x^7}{7x^5} + \frac{C}{x^5}\\
Resultado\\
y = \frac{x^2}{7} + \frac{C}{x^5}
$$

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

