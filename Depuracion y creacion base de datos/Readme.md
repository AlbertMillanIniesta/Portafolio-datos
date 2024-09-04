![código](https://albertmillan.wordpress.com/wp-content/uploads/2024/09/codigopython.png?w=750)



**INTRODUCCIÓN**

A veces, la estructura de la base de datos puede acabar dando más dolores de cabeza que el trabajo posterior. Y es todavía peor cuando uno se encabezona en que el programa que se utiliza debería poder hacer lo que uno cree y se va dando continuamente cabezazos contra un muro por no querer restructurar la base de datos.

Pues esto es lo que me pasó con el proyecto con el proyecto de “Viviendas para personas con discapacidad intelectual en Cataluña”. Decidí que el programa debía poder hacer cosas que no hacía hasta que me di cuenta que mi testarudez evitaba que pudiese conseguir los resultados que deseaba y que era mucho más sencillo empezar a escribir código

Pero todo esto no fue negativo: aprendí mucho de Tableau y que uno debe adaptarse al programa y no al revés.


**CONTENIDO DEL CÓDIGO**

Parte 1

La base de datos dónde se registran todos los servicios incluye muchos servicios que no se analizan en el proyecto anteriormente nombrado. Así que realicé una sencilla limpieza de datos y adapté algunos valores a partir de:

- Quitar las columnas con variables innecesarias para este proyecto.

- Seleccionar para la base de datos las filas de la columna que indica el tipo de servicio con los servicios a tratar.

- Cambio de nombre de algunas columnas y de ciertos valores.

- Cambio de formato de los valores a formato fecha para la columna que lo requería.

- Guardar la base de datos resultante como un archivo .csv llamado 'Habitatge1.csv

Parte 2

Como comentaba anteriormente, los programas no siempre hacen lo que creemos que pueden hacer. En mi caso, deseaba que realizar etiquetas para el dashboard en las que Tableau contase que cuando había ausencia de valores, el resultado debía ser 0. Tras intentarlo con diversas fórmulas y rebuscar en foros de Tableau, encontré una entrada similar a mi problema, donde recomendaban rehacer las base de datos. Y eso hice.

- Obtener todas las posibles combinaciones de años, comarcas y tipología de servicio y crear un dataframe con ellas.

- Crear un dataframe con las combinaciones faltantes.

- Unir ambos dataframes.

- Añadir las comarcas de las que no había datos.

- Substitución de los valores faltantes (NAs) por 0s.

- Suma acumulada de los valores de las diferentes columnas.

- Conversión de los valores a tipo numérico.

- Guardar la base de datos resultantos como un archivo .csv llamado "Habitatge2.csv"
