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
Un problema sencillo que aun no tiene una demostración para todos los números naturales. La conjetura de Collatz fue trasmitida de forma oral por Lothar Collatz en el Congreso de Matemáticasen la universidad de Cambridge en 1950. Al captar la atención y sobre todo curiosidad de los matamáticos de la época se pensó inclusive que era una forma de distraer a los matemáticos de Norteamerica durante la guerra fria. 


## Quién fue Collatz

Lothar Collatz , como la mayoría de los estudiantes alemanes de su época, estudió en diversas universidades. Ingresó en la Universidad de Greifswald en 1928 , trasladándose a Múnich, luego a Gotinga y finalmente a Berlín, donde se doctoró con Alfred Klose. Collatz obtuvo su doctorado en 1935. 

## El problema
Para poder plantear este problema vamos a hacer un ejemplo sencillo. Empezamos con un numero natural cualquiera si es par entonces debemos de dividirlo entre dos, si no, debemos multiplecarlo por 3 y sumarle uno. Empecemos con el 5,  es impar por lo que lo multiplecamos por 3 y le sumamos 1: 5 * 3 = 15, 15 + 1 = 16. El resultado es par entonces lo dividimos entre 2, 16/2 = 8, al ser par lo dividimos nuevamente 8/2 = 4, nuevamente 4/2=2 y finalmente 2/2 = 1. 

a esto se le conoce entonces como el problema $3n+1$



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
