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

Or if you want to do more fancy things, go full rgba:

![transparent red overlay]({{ '/assets/images/mm-header-overlay-red-filter.jpg' | relative_url }})

```yaml
excerpt: "This post should [...]"
header:
  overlay_image: /assets/images/unsplash-image-1.jpg
  overlay_filter: rgba(255, 0, 0, 0.5)
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  actions:
    - label: "More Info"
      url: "https://unsplash.com"
```
