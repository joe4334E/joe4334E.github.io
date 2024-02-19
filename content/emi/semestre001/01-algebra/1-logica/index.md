---
title: Indice de 
subtitle: ""
date: 2020-03-04T15:58:26+08:00
lastmod: 2020-03-04T15:58:26+08:00
draft: false
author: "Efrain Colque"
authorLink: "https://github.com/joe4334E"
description: ""
license: ""
images: []

tags: [LOGICA]
categories: [ALGEBRA]
featuredImage: ""
featuredImagePreview: ""

hiddenFromHomePage: false
hiddenFromSearch: false
twemoji: false
lightgallery: true
ruby: true
fraction: true
fontawesome: true
linkToMarkdown: true
rssFullText: false

toc:
  enable: true
  auto: true
code:
  copy: true
  # ...
math:
  enable: true
  # ...
mapbox:
  accessToken: ""
  # ...
share:
  enable: true
  # ...
comment:
  enable: true
  # ...
library:
  css:
    # someCSS = "some.css"
    # located in "assets/"
    # Or
    # someCSS = "https://cdn.example.com/some.css"
  js:
    # someJS = "some.js"
    # located in "assets/"
    # Or
    # someJS = "https://cdn.example.com/some.js"
seo:
  images: []
  # ...
---

## Indice de la materia Logica

```bash 
#!/bin/bash

# Definir la ruta base
base_path="emi/Semestre_1/01. ALGEBRA/1 LÓGICA"

# Definir los nombres de los archivos
files=("1.1 Proposiciones y Valores de verdad.md"
       "1.2 Proposiciones simples y compuestas.md"
       "1.3 Tablas de verdad.md"
       "1.4 Proposiciones lógicamente equivalentes.md"
       "1.5 Algebra de proposiciones.md"
       "1.6 Argumentación y Reglas de inferencia.md"
       "1.7 Cuantificadores.md"
       "1.8 Métodos de demostración.md")

# Crear los archivos con hugo new
for file in "${files[@]}"; do
  hugo new "$base_path/$file"
done

```

