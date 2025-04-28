# La Ecuación de una Recta

La ecuación de una recta en el plano cartesiano es una de las bases de la geometría analítica.  
La forma más común es la forma pendiente-intersección:

\[
y = mx + b
\]

donde:
- \(m\) es la **pendiente** de la recta (qué tan inclinada está).
- \(b\) es el **intercepto** en el eje \(y\) (donde la recta cruza el eje \(y\)).

## ¿Qué significa la pendiente?

La pendiente \(m\) indica cuánto sube o baja la recta por cada unidad que avanzamos en \(x\).

- Si \(m > 0\), la recta sube hacia la derecha.
- Si \(m < 0\), la recta baja hacia la derecha.
- Si \(m = 0\), la recta es horizontal.

## Ejemplo en Python

Vamos a trazar una recta con pendiente \(m = 2\) e intercepto \(b = 1\).

```python
import numpy as np
import matplotlib.pyplot as plt

# Definimos la pendiente y el intercepto
m = 2
b = 1

# Creamos valores de x
x = np.linspace(-10, 10, 100)

# Calculamos los valores de y
y = m * x + b

# Graficamos
plt.plot(x, y, label="y = 2x + 1")
plt.xlabel('x')
plt.ylabel('y')
plt.title('Gráfica de la ecuación de una recta')
plt.grid(True)
plt.legend()
plt.show()
