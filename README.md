# Xaringan_RLadies

[Link](https://bookdown.org/yihui/rmarkdown/xaringan.html)

[Rmarkdown con Latex](https://github.com/HaydeePeruyero/Rmarkdown_and_LaTeX)

Ejemplo presentación R Ladies sobre el tema [link](https://www.youtube.com/watch?v=uBXEtM-OHlI&ab_channel=R-LadiesXalapa)


- Presentaciones [revealjs](https://quarto.org/docs/presentations/revealjs/)
  - [Ejemplo](https://haydeeperuyero.github.io/Xaringan_RLadies/revealjs.html)
- Presentaciones Xaringan
  - [Tema de RLadies Global](https://www.apreshill.com/project/rladies-xaringan/)
- Recomendación para hacer diagramas complicados
- Documentos de RMarkdown
- CSS y HTML

### Temas (propuesta)

- Objetivos de la charla 
- ¿Historia (breve) desarrollo Xaringan?, ¿reveal js con Quarto? ¿Qué es Rmarkdown o qué es Quarto?
- Instalación - clonar repositorio

**Xaringan y Quarto js**

- Formato de diapositivas
  - Diapositiva de titulo 
  - Diapositivas graduales 
- Clases CSS (para diapositivas en general y para dar formato a partes de la diapositiva)
  - Clases pre-incluidas
  - Propiedades útiles para presentaciones (tamaños de imagen, posición, color de texto,)
  - Como añadir css al documento 
- Ejercicios (columnas, tamaños de texto, poner imágenes, etc.)
- Temas preconfigurados que se pueden elegir
- Como hacer notas de presentador
- Como presentar (una vez que ya está el documento html)
  - shortcuts, presenter view, etc. 
- Documentos autocontenidos 
- Para el paquete de Quarto seguir capítulo de [revealjs](https://quarto.org/docs/presentations/revealjs/)
- Para Xaringan seguir [capitulo](https://bookdown.org/yihui/rmarkdown/xaringan.html) 
- Solo presentar las cosas que sean diferentes entre los paquetes.

**Ejemplos y recursos**
- [Presentación Rladies Xalapa Xaringan](https://slides.silviacanelon.com/introduccion-xaringan)
- [Curso de Xaringan](https://spcanelon.github.io/xaringan-basics-and-beyond/) - Tiene los materiales y los videos 
- [Curso CSS freecodecamp](https://www.youtube.com/watch?v=OXGznpKZ_sA&ab_channel=freeCodeCamp.org)
  - [Repositorio de recursos del curso (CSS)](https://github.com/gitdagray/css_course)

# Trabajo colaborativo

### Pasos a seguir
  1. Abrir RStudio
  2. Abrir el proyecto en el cual se está trabajando. De preferencia use `File -> Open Project in New Session...` para trabajar en el directorio correcto que únicamente tiene cargados los documentos que necesitará.
  3. Ya que estamos en un proyecto enlazado a Github (esto se explica en el [Paso 2](https://cfss.uchicago.edu/setup/git-with-rstudio/)) del manual, pinchamos la flecha azul que aparece en la pestaña *Git* para hacer _pull_ de la última versión en línea de nuestro proyecto, es decir, descargamos los últimos cambios disponibles en el repositorio de Github.
  4. *Importante*. Pinchamos en el símbolo morado para crear una rama local en la cual trabajaremos.
  ![ramalocal01](images/ramalocal01.jpeg)
  
  La cual configuramos únicamente para trabajar de manera local como se muestra en la siguiente imagen.
  ![ramalocal02](images/ramalocal02.jpeg)
  
  Este paso lo hacemos para evitar problemas cuando haya cambios en la rama principal `main`. De preferencia, realizamos esta acción cada vez que iniciamos un nuevo proyecto. Para evitar errores más adelane, el nombre de nuestra rama no debe contener símbolos especiales, ni puntos, ni acentos ni espacios: se sugiere usar un nombre del tipo `rama_local` o bien `RamaLocal`.
  
  5. Realizamos todas las acciones y actualizaciones dentro de esta rama local.
  6. Pinchamos a ``Commit``dentro de la pestaña *Git* y escribimos los comentarios necesarios para explicar nuestro trabajo realizado en la ventana que se abre. Debemos asegurarnos de _seleccionar_ solo los archivos que deseemos actualizar.
  7. Junto al nombre de nuestra rama local `rama_local` en la pestaña *Git* aparece un triángulo que apunta hacia abajo, lo pinchamos y cambiamos a la rama principal `main`. Esto nos abrirá un mensaje que, si no hay errores, indicará que hemos cambiado a la rama principal.
  8. Nuevamente hacemos _pull_ porque podría haber actualizaciones realizadas por otro colaborador.
  9. En caso de que las haya actualizaciones después de _descargar_ la última versión del repositorio, nuevamente hacemos ``Commit``. Note que estamos en la rama principal `main` del proyecto
  10. Abrimos una consola a partir del menú `Tools -> Shell`.
  11. En la consola escribimos el siguiente comando
  ```
  git merge rama_local
  ```
  donde `rama_local` es el nombre que le asignamos a la rama local en la cual trabajamos. Esto se hace para _combinar_ nuestro trabajo local con la rama principal `main` antes de subir nuestras actualizaciones al repositorio. Ya podemos cerrar la consola.
  
  12. A continuación, hacemos _push_ de nuestro trabajo. Esto se logra pinchando la flecha verde que apunta hacia arriba. Esto termina la actualización del repositorio.
  13. Eliminamos la rama local al escribir en la consola el siguiente comando
  ```
  git branch -d rama_local
  ```
  Una vez hecho esto, cerramos la consola. Hacemos esto porque en la rama local se guardan los cambios y si por alguna actualización descargada en el paso 8 no coinciden con lo obtenido en la rama principal después del paso 12, podríamos obtener versiones no compatibles y generar errores en la versión final.
  
  14. Para concluir, cerramos el proyecto desde `File -> Close Project` antes de cerrar RStudio para evitar errores al cargar la interfaz en una próxima ocasión.
  15. Cuando reabra el proyecto una próxima vez, repita a partir del paso 4 para asegurar el mejor desempeño.

