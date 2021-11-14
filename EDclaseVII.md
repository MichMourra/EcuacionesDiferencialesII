# Ecuaciones diferenciales II clase  VII

$$
\frac{\delta^2 f}{\delta x} \ \ Esta \ \ expresión \ \ indica \ \ que \ \ se \ \  deriva \ \ dos \ \ veces\\
\frac{\delta^2 f}{\delta^2 x} \ \ las \ \ dos \ \ veces \ \ se \ \ deriva respecto \ \ a \ \ x
$$

# Derivadas e integrales parciales



## Derivadas parciales

Supongamos que tenemos una función de 2 variables:
$$
Derivadas \ \ Parciales: \\
f(x,y) = 4x^{2} + 9y^{2} + 10xy + 3x\\
\frac{\delta f}{\delta x} = 8x + 10y + 3\\
\frac{\delta f}{\delta y} = 18y + 10x\\
\frac{\delta^2 f}{\delta x^{2}} = 8\\
\frac{\delta^2 f}{\delta x \delta y} = 10\\
\frac{\delta^2 f}{ \delta y \delta x} = 10\\
\frac{\delta^2 f}{\delta y^{2}} = 18\\
Desarrollamos:\\
f(x,y) = (8x + 10y + 3)dx + (18y + 10x)dy
$$

### Ejercicios de derivadas parciales

De cada problema hay que hacer siete derivadas:

-----------------------------------------------------

1. $$
   f(x,y) = 2e^x - 8x^3y^2
   $$

**Respuesta**
$$
\frac{\delta f(x,y)}{\delta x} = 2e^x - 24y^2x^2\\
\frac{\delta f(x,y)}{\delta y} = - 16yx^3\\
\frac{\delta^2 f(x,y)}{\delta x^{2}} = 2e^x - 48y^2x \\
\frac{\delta^2 f(x,y)}{\delta x \delta y} = - 48yx^2\\
\frac{\delta^2 f(x,y)}{ \delta y \delta x} = -48yx^2\\
\frac{\delta^2 f(x,y)}{\delta y^{2}} = -16x^3 \\
Diferencial \ \ total: \\
df(x,y) = (2e^x - 24y^2x^2) dx + (- 16yx^3)dy
$$


----------------------------------------------------------------------------

2. $$
   12x^2 - 8xy + 3y^2
   $$

**Respuesta**
$$
\frac{\delta f(x,y)}{\delta x} = 24x - 8y\\
\frac{\delta f(x,y)}{\delta y} = 6y - 8x\\
\frac{\delta^2 f(x,y)}{\delta x^{2}} = 24 \\
\frac{\delta^2 f(x,y)}{\delta x \delta y} = -8 \\
\frac{\delta^2 f(x,y)}{ \delta y \delta x} = -8\\
\frac{\delta^2 f(x,y)}{\delta y^{2}} = 6\\
Diferencial \ \ total: \\
df(x,y) = (24x - 8y) dx + (6y - 8x)dy
$$


-----------------------------------------------------------------------------------------

3. $$
   f(x,y) = -4x^3 - 3x^2y^3 + 2y^2
   $$

4. 

**Respuesta:**







-----------------------------------------------------------------------------------------------------

4. $$
   f(x,y) = e^{x + y}
   $$

**Respuesta:**
$$
\frac{\delta f(x,y)}{\delta x} = e^{x+y}\\
\frac{\delta f(x,y)}{\delta y} = e^{x+y}\\
\frac{\delta^2 f(x,y)}{\delta x^{2}} = e^{x+y}\\
\frac{\delta^2 f(x,y)}{\delta x \delta y} = e^{x+y}\\
\frac{\delta^2 f(x,y)}{ \delta y \delta x} = e^{x+y}\\
\frac{\delta^2 f(x,y)}{\delta y^{2}} = e^{x+y}\\
Diferencial \ \ total: \\
df(x,y) = e^{x+y} dx + e^{x+y} dy
$$


------------------------------------------------------------

5. $$
   f(x,y) = -5e^{3x - 4y}
   $$

6. 

**Respuesta:**


$$
\frac{\delta f(x,y)}{\delta x} = -15e^{3x-4y}\\
\frac{\delta f(x,y)}{\delta y} = 20e^{3x-4y}\\
\frac{\delta^2 f(x,y)}{\delta x^{2}} = -45e^{3x-4y}\\
\frac{\delta^2 f(x,y)}{\delta x \delta y} = 60e^{3x-4y}\\
\frac{\delta^2 f(x,y)}{ \delta y \delta x} = 60e^{3x-4y}\\
\frac{\delta^2 f(x,y)}{\delta y^{2}} = -80e^{3x-4y}\\
Diferencial \ \ total: \\
df(x,y) = (-15e^{3x-4y}) dx + (20e^{3x-4y}) dy
$$


--------------------------------------------------------------------------------------------

6. $$
   f(x,y) = xe^{x^2y}
   $$

**Respuesta:**

En este caso empleamos la ley para las derivadas de un producto:
$$
\frac{\delta f(x,y)}{\delta x} = (2x^2y + 1)e^{x^2y}\\
\frac{\delta f(x,y)}{\delta y} = x^3e^{x^2y}\\
\frac{\delta^2 f(x,y)}{\delta x \delta y} = (2x^4y + 3x^2)e^{x^2y}\\
\frac{\delta^2 f(x,y)}{ \delta y \delta x} = (2x^4y + 3x^2)e^{x^2y}\\
\frac{\delta^2 f(x,y)}{\delta y^{2}} = x^5e^{x^2y}\\
\frac{\delta^2 f(x,y)}{\delta x^{2}} = (4x^3y^2 + 6xy)e^{x^2y}\\
Diferencial \ \ total: \\
df(x,y) = ((2x^2y + 1)e^{x^2y}) dx + (x^3e^{x^2y}) dy
$$


## Integrales parciales

Las integrales parciales siguen exactamente la misma idea que las diferenciales parciales, es decir, que las otras variables serán tomadas como constantes si se deriva respecto a una:

- Se plantea el ejercicio de que la curvatura de una sabana es representado por esa ecuación, por lo que el volumen de esta puede obtenerse mediante una integral.

$$
\int f(5x^3y^4 + 6x^3 + 3y^3 + 2xy + 7) dx
$$

**Resolución ejemplo con respecto de x:**
$$
5y^4\frac{x^4}{4} + 6\frac{x^4}{4} + 3y^3x + 2y\frac{x^2}{2} + 7x + h(y) \\
\frac{5}{4}x^4y^4 + \frac{3}{2}x^4 + 3xy^3 + x^2y + 7x + h(y) \\
h(y) + j(z) + k(y,z)
$$
**Resolución ejemplo con respecto de y:**
$$
\int f(5x^3y^4 + 6x^3 + 3y^3 + 2xy + 7) dy \\
5x^3\frac{y^5}{5} + 6x^3y + 3\frac{y^4}{4} + 2x\frac{y^2}{2} + 7y + g(x)
$$

### Ejercicios integrales parciales

1. $$
   \int (6xy^2 + 12x^2y + 4y)dx
   $$

**Respuesta:**
$$
6y^2\frac{x^2}{2} + 12y \frac{x^3}{3} + 4xy + h(y) \\
Simplificamos:\\
3x^2y^2 + 4x^3y+ 4xy + h(y)
$$


------------------------------------------------------------------------------------

2. $$
   \int (2xy^3 + 6x^2y^2 + 2y^2) dy
   $$

**Respuesta:**
$$

$$






------------------------------------------------------------------------

3. $$
   \int xy \ dx
   $$





------------------------------------------------------------------------------

4. $$
   \int xy \ dy
   $$

5. 
