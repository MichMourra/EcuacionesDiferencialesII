# Ecuaciones diferenciales 2

# Clase IV



## Ecuaciones de Cauchy-Euler

### Introducción

Estas ecuaciones tienen una forma especifica y el grado de la derivada depende del valor del coeficiente.

- Hay funciones que se derivan y se integran dentro de su familia
  - Polinomios
  - Exponenciales
  - Senos-Cosenos

Planteamiento
$$
a \frac{d^2y}{dx^2} + b \frac{dy}{dx} + cy = 0 \\
y = e^{Dx} \\
y = e^{mx} \\
y = e^{\lambda x}
$$
Escribiremos una ecuación de Cauchy-Euler:

1. Primero proponemos nuestra ecuación
   $$
   x^2 \frac{d^2y}{dx^2} - 2x \frac{dy}{dx} - 4y = 0
   $$

2. Ahora proponemos posibles soluciones para dicha ecuación
   $$
   y = \sin x \\
   y = e^{Dx} \\
   y = x^{\lambda}
   $$
   
3. Ahora debemos ver cual de las soluciones nos conduce por el camino mas sencillo

   ### x a la lambda

   Primero trataremos sustituyendo y por x a la lambda
   $$
   x^2 \frac{d^2y}{dx^2} - 2x \frac{dy}{dx} - 4x^{\lambda} = 0\\
   primera \ \ derivada: \\
   \frac{dy}{dx} = \lambda x^{\lambda - 1}\\
   segunda \ \ derivada: \\
   \frac{d2y}{dx2} = (\lambda - 1)\lambda x^{\lambda -2} \\
   planteamos \ \ la \ \ ecuacion: \\
   \lambda(\lambda -1)x^2x^{\lambda - 2} - 2 \lambda x x^{\lambda -1} - 4 x^{\lambda} \\
   \lambda (\lambda - 1) x^{\lambda} - 2 \lambda x^{\lambda} - 4 x^{\lambda}\\
   factorizamos: \\
   (\lambda(\lambda - 1) -2 \lambda - 4)x^{\lambda}\\
   (\lambda(\lambda - 1) -2 \lambda - 4) = 0\\
   desarrollamos: \\
   \lambda^{2} - \lambda - 2\lambda - 4 = 0 \\
   \lambda^2 - 3\lambda - 4 = 0 \\
   soluciones: \\
   (\lambda - 4)(\lambda + 1) = 0\\
   \lambda_1 = 4 \ \ \ \ \lambda_2 = -1
   $$
   La característica de Cauchy-Euler es que al proponer la solución x a la lambda, la pueda factorizar.
   $$
   x^2 \frac{d^2y}{dx^2} - 2x \frac{dy}{dx} - 4x^{\lambda} = 0\\
   $$
   Cuando se derivan los valores, existe una compensación entre los exponentes de la x ya que estos exponentes coinciden con el orden de la derivada.
   $$
   ax^2 \frac{d^2y}{dx^2} + bx \frac{dy}{dx} + cy = 0\\
   Planteamos: \\
   ax^2 (\lambda - 1)\lambda x^{\lambda -2} + bx\lambda x^{\lambda - 1} + cx^{\lambda}\\
   resolvemos: \\
   a\lambda^2 x^{\lambda} - a\lambda x^{\lambda} + b\lambda x^{\lambda} + cx^{\lambda} \\
   factorizamos: \\
   (a\lambda(\lambda - 1) + b\lambda + c)x^{\lambda} = 0 \\
   a\lambda^2 - a\lambda + b\lambda + c = 0\\
   a\lambda^2 + (b-a) \lambda + c = 0 \\
   forma: \\
   e^{iz} = \cos z + i \sin z
   $$
   Esto nos da como resultado que lambda es compleja:
   $$
   e^{iz} = \cos z + i \sin z \\
   \lambda = \alpha + \beta i \\
   y = x^{\lambda} = x^{\alpha + \beta i} = x^{\alpha}x^{\beta i} \\
   x = e^{\ln x} \\
   x^{\beta}i = (e^{\ln x})^{\beta i} = e^{\beta \ln x i} \\
   $$

Una vez que tenemos la formula de Euler la podemos convertir en senos y cosenos

### Solución general cuando lambda es un complejo

$$
y = x^{\alpha}(C_1 \cos \beta \ln x + C_2 \sin \beta \ln x)
$$

### Si lambda son dos soluciones independientes

$$
y = C_1x^{\lambda_1} + C_2x^{\lambda_2}
$$

### Si lambda es una solución única

$$
y = C_1x^{\lambda} + C_2 \ln x X^{\lambda}
$$

## Ejercicios Ecuaciones de Cauchy - Euler

1. $$
   4x^2 \frac{d^2y}{dx^2} + 17y = 0\\
   4x^2(\lambda - 1)\lambda x^{\lambda -2} + 17x^\lambda \\
   4\lambda^2x^\lambda - 4\lambda x^{\lambda} + 17 x^{\lambda} \\
   factorizamos: \\
   (4\lambda^2 - 4\lambda + 17)x^{\lambda} = 0 \\
   (4\lambda^2 - 4\lambda + 17) = 0 \\
   formula \ \ general: \\
   \lambda = \frac {-(-4) \pm \sqrt {(-4)^2 - 4(4)(17)}}{2(4)} \\
   \lambda = \frac {+4 \pm \sqrt {16 - 272}}{8} \\
   \lambda = \frac {+4 \pm \sqrt {-256}}{8}\\
   \lambda_1 = \frac {1}{2} + \frac{\sqrt {-256}}{8}\\
   \lambda_2 = \frac {1}{2} - \frac{\sqrt {-256}}{8} \\
   \lambda_1 = \frac {1}{2} + \frac{16i}{8}\\
   \lambda_2 = \frac {1}{2} - \frac{16i}{8} \\
   \lambda_1 = \frac {1}{2} + 2i\\
   \lambda_2 = \frac {1}{2} - 2i \\
   solución: \\
   y = x^{\frac{1}{2}}(C_1 \cos 2 \ln x + C_2 \sin 2 \ln x)
   $$

2. $$
   x^3 \frac{d^3y}{dx^3} + 5x^2 \frac{d^2y}{dx^2} + 7x\frac{dy}{dx} + 8y = 0\\
   $$
   
3. $$
   x^2 \frac{d^2y}{dx^2} - 2y = 0\\
   x^2(\lambda - 1)\lambda x^{\lambda -2} - 2x^\lambda \\
   \lambda^2x^\lambda - \lambda x^{\lambda} - 2x^{\lambda} \\
   factorizamos: \\
   (\lambda^2 - \lambda - 2)x^{\lambda} = 0 \\
   (\lambda^2 - \lambda - 2) = 0 \\
   resolvemos: \\
   (\lambda + 1)(\lambda - 2) = 0\\
   \lambda_1 = -1\\
   \lambda_2 = 2\\
   solución: \\
   y = C_1x^2 + C_2x^{-1}
   $$

4. $$
   x^2 \frac{d^2y}{dx^2} + x \frac{dy}{dx} + 4y = 0\\
   x^2(\lambda - 1)\lambda x^{\lambda -2} + x\lambda x^{\lambda - 1} + 4x^\lambda \\
   \lambda^2x^\lambda - \lambda x^{\lambda} + \lambda x^{\lambda} + 4 x^{\lambda} \\
   factorizamos: \\
   (\lambda^2 - \lambda + \lambda + 4)x^{\lambda} = 0 \\
   (\lambda^2 + 4) = 0 \\
   formula \ \ general: \\
   \lambda = \frac {-(0) \pm \sqrt {(0)^2 - 4(1)(4)}}{2(1)} \\
   \lambda = \frac {0 \pm \sqrt {0 - 16}}{2} \\
   \lambda = \frac {0 \pm \sqrt {-16}}{2}\\
   \lambda_1 = \frac{\sqrt {-16}}{2}\\
   \lambda_2 = - \frac{\sqrt {-16}}{2} \\
   \lambda_1 = 2i\\
   \lambda_2 = -2i \\
   solución: \\
   y = (C_1 \cos 2 \ln x + C_2 \sin 2 \ln x)
   $$

5. $$
   x^2 \frac{d^2y}{dx^2} - 3x \frac{dy}{dx} - 2y = 0\\
   $$

   

