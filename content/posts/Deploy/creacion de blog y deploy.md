---
title: Uso del Tema FeelIt
date : 2020-03-04T15:58:26+08:00
draft: false
author: "Efrain Colque"
description: "Deploy y uso de Githup Pages para Static Web"
license: "MIT"
tags: ["Github", "Deploy"]
Categories: ["GIT"]
---

### Creacion de blog con hugo y deploy desde 0 con el tema Feelit 

Para crear un blog con Hugo y desplegarlo desde cero con el tema Feelit, puedes seguir los siguientes pasos:

1. Instalación de Hugo:
- Descarga e instala Hugo siguiendo las instrucciones de la documentación oficial: https://gohugo.io/getting-started/installing/

2. Crear un nuevo sitio de Hugo:
- Abre una terminal y ejecuta el siguiente *comando* para crear un nuevo sitio de Hugo:
```bash
hugo new site nombre-del-blog
```

3. Descargar el tema Feelit:

- Ve al repositorio oficial del tema Feelit en GitHub: https://github.com/niceandhonest/feelit-hugo-theme
- Haz clic en el botón "Code" y luego en "Download ZIP" para descargar el tema.
- Extrae el contenido del archivo ZIP descargado en la carpeta `themes` dentro de tu sitio de Hugo.

4. Configurar el tema Feelit:
- Abre el archivo `config.toml` en la raíz de tu sitio de Hugo.
- Agrega la siguiente línea para indicar que estás utilizando el tema Feelit:

```bash
theme = "feelit-hugo-theme"
```

5. Crear contenido:
- Ejecuta el siguiente comando para crear un nuevo post:
```bash
hugo new posts/nombre-del-post.md
```
- Edita el archivo markdown creado en `content/posts` para escribir tu contenido.

6. Personalizar la apariencia:
- Explora los archivos dentro del directorio `themes/feelit-hugo-theme` y personaliza los archivos CSS, HTML o cualquier otro archivo según tus necesidades.

7. Ejecutar servidor local:
- Para ver tu blog localmente antes de desplegarlo, ejecuta el siguiente comando en la terminal:
```bash
hugo server -D
```
- Abre tu navegador web y ve a `http://localhost:1313` para ver tu blog.

8. Desplegar el blog:
- Una vez que estés satisfecho con tu blog localmente, es hora de desplegarlo.
- Puedes utilizar servicios como Netlify, GitHub Pages o cualquier otro servicio de alojamiento que sea compatible con Hugo.
- Sigue las instrucciones proporcion
<iframe width="853" height="480" src="https://www.youtube.com/embed/LIFvgrRxdt4" title="Creating a Blog with Hugo and Github in 10 minutes" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Deploy con github pages


Para desplegar tu blog con GitHub Pages, puedes seguir estos pasos:

1. Crea un repositorio en GitHub:
- Ve a tu cuenta de GitHub y crea un nuevo repositorio.
- Dale un nombre al repositorio, por ejemplo "nombre-del-blog".
- Asegúrate de marcar la opción "Initialize this repository with a README".

2. Configura el repositorio remoto:
- Abre una terminal y navega hasta la carpeta raíz de tu sitio de Hugo.
- Inicializa Git en ese directorio ejecutando el siguiente comando:
```bash
git init
```

- Agrega los archivos al repositorio ejecutando el siguiente comando:
```bash
git add .
```
- Realiza el primer commit ejecutando el siguiente comando:

```bash
git commit -m "Initial commit"
```
- Enlaza tu repositorio local con el remoto ejecutando el siguiente comando:
```bash
git remote add origin URL_DEL_REPOSITORIO
```

3. Genera los archivos estáticos del sitio:
- Ejecuta el siguiente comando para generar los archivos estáticos del sitio de Hugo:
```bash
hugo -D 
```

4. Crea una rama llamada "gh-pages":
- Ejecuta el siguiente comando para crear una nueva rama llamada "gh-pages":
```bash
git checkout --orphan gh-pages
```

5. Mueve los archivos generados a la nueva rama:
- Ejecuta los siguientes comandos para mover los archivos generados a la nueva rama "gh-pages":

```bash
mv public/* .
rm -rf public/
git add .
git commit -m "Deploying to gh-pages"
git push origin gh-pages
```

6. **Activa GitHub Pages en la configuración del repositorio:**

- Ve a la página de configuración del repositorio en GitHub.
- Desplázate hacia abajo hasta la sección "GitHub Pages".
- En la opción "Source", selecciona "gh-pages branch".
- Haz clic en "Save".

Después de seguir estos pasos, tu sitio de Hugo con el tema Feelit debería estar desplegado en GitHub Pages. Puedes acceder a él a través de la URL proporcionada por GitHub


7. Uso de designer.yml(hugo.yml o static.yml) 


Para utilizar el archivo designer.yml con el tema Feelit en Hugo, puedes seguir estos pasos:

1. Crea un archivo llamado `designer.yml` en la raíz de tu sitio de Hugo.
2. Abre el archivo y agrega el siguiente contenido:

```yml
theme:
name: "feelit-hugo-theme"
version: "1.0.0"
```

3. Guarda el archivo `designer.yml`.
4. Ejecuta el siguiente comando para generar los archivos estáticos del sitio de Hugo:
```bash 
hugo
```
5. Verifica que los archivos generados estén en la carpeta `public`.

Ahora, cuando despliegues tu sitio utilizando GitHub Pages u otro servicio de alojamiento compatible con Hugo, asegúrate de incluir el archivo `designer.yml` junto con los demás archivos estáticos.

El uso del archivo `designer.yml` te permite especificar la versión del tema que estás utilizando y proporciona información adicional para la personalización y configuración del tema en tu sitio de Hugo.
