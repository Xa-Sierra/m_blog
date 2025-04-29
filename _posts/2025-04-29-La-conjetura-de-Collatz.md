---
title: "La conjetura de Collatz"
header:
  overlay_image: /assets/images/Collatz-2.png
  overlay_filter: 0.5 
  caption: ""
  actions:
    - label: "Home"
      url: "https://xa-sierra.github.io/m_blog"
categories:
  - Matemáticas
  - Uncategorized
tags:
  - Collatz
  - conjetura
  - problema
last_modified_at: 2025-04-29T11:39:01-04:00
---
Un problema sencillo que aun no tiene una demostración para todos los números naturales

## El problema
Para poder platear este problema vamos a hacer un ejemplo sencillo. Empezamos con un numero natural cualquiera, por ejemplo el 5, si es par entonces debemos de dividirlo entre dos, si no, debemos multiplecarlo por 3 y sumarle uno. Entonces, el 5 es impar, por lo que lo multiplecamos por 3 y le sumamos 1: 5 * 3 = 15, 15 + 1 = 16. El resultado es par entonces lo dividimos entre 2, 16/2 = 8, al ser impar lo dividims nuevamente 8/2 = 4, nuevamente 4/2=2 y finalmente 2/2 = 1. 
## Quién fue Collatz

Lothar Collatz , como la mayoría de los estudiantes alemanes de su época, estudió en diversas universidades. Ingresó en la Universidad de Greifswald en 1928 , trasladándose a Múnich, luego a Gotinga y finalmente a Berlín, donde se doctoró con Alfred Klose. Collatz obtuvo su doctorado en 1935. 

```python
def collatz(n):
    secuencia = []
    while n != 1:
        secuencia.append(n)
        n = n // 2 if n % 2 == 0 else 3 * n + 1
    secuencia.append(1)  # Añadimos el 1 final
    return secuencia

# Probemos con n = 17
print(collatz(137))
```
