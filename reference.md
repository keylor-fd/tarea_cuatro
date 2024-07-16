# Métodos Numéricos para la Aproximación

Existen varios métodos numéricos utilizados para aproximar soluciones de ecuaciones diferenciales. Entre los más conocidos se encuentran:

### Método de Euler

El método de Euler es el más elemental de los métodos numéricos para resolver ecuaciones diferenciales. Se basa en la aproximación lineal de la función en pequeños pasos $h$:

$$ y(x+h) = y(x) + h f(x,y) $$

Aunque es simple y eficiente computacionalmente, el método de Euler tiende a ser menos preciso que otros métodos más avanzados como el método de Runge-Kutta.

### Método de Runge-Kutta

El método de Runge-Kutta es una familia de métodos numéricos que ofrecen mayor precisión que el método de Euler, a costa de requerir más cálculos por iteración. Aquí se describen dos variantes populares:

#### Segundo Orden (RK2)

El método de Runge-Kutta de segundo orden mejora la precisión al considerar la pendiente en el punto medio del intervalo $h$:

$$ y(x+h) = y(x) + h k_{2} $$

Donde $k_{i}$ se calculan como:

- $k_{1} = f(x,y)$
- $k_{2} = f\left(x + \frac{h}{2}, y + \frac{k_{1}}{2}\right)$

#### Cuarto Orden (RK4)

El método de Runge-Kutta de cuarto orden es uno de los métodos numéricos más precisos para la aproximación de ecuaciones diferenciales. Aunque es más complejo computacionalmente, proporciona resultados más exactos al calcular promedios ponderados de las pendientes en varios puntos dentro del intervalo $h$:

$$ y(x+h) = y(x) + \frac{h}{6} (k_{1} + 2k_{2} + 2k_{3} + k_{4}) $$

Donde $k_{i}$ se definen como:

- $k_{1} = f(x,y)$
- $k_{2} = f\left(x + \frac{h}{2}, y + \frac{k_{1}}{2}\right)$
- $k_{3} = f\left(x + \frac{h}{2}, y + \frac{k_{2}}{2}\right)$
- $k_{4} = f(x + h, y + k_{3})$

Estos métodos numéricos son fundamentales cuando no es posible obtener soluciones analíticas exactas para ecuaciones diferenciales complejas. La elección del método adecuado depende de la precisión requerida y del costo computacional tolerable.

