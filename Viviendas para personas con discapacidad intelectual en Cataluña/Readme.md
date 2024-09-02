![dashboard](https://albertmillan.wordpress.com/wp-content/uploads/2024/08/dashboard.jpg?w=1024)

**INTRODUCCIÓN**

Toda mi experiencia laboral previa se centra en el sector social, mayoritariamente con personas con discapacidad intelectual. Durante muchos años he trabajado como educador en pisos tutelados donde he aprendido muchísimo. Por eso mismo me parecía muy interesante ver qué evolución han tenido este tipo de viviendas y qué características tienen a partir de un dashboard realizado con Tableau.

Sin entrar en detalles, en Cataluña existen 3 tipos de viviendas gestionadas por entidades para personas con discapacidad intelectual: las residencias («residències»), los pisos tutelados («llars-residència») y los hogares con apoyos («llars amb suport»). Los registros al respecto empiezan en el año 1988, dándose el primer registro en 1.989. Estos datos se pueden consultar en el «Registre d’entitats, serveis i establiments socials (serveis socials bàsics especialitzats)» del Departament de Drets Socials i Inclusió de la Generalitat de Catalunya y están actualizados hasta el 22 de agosto de 2.023.

Por otro lado, para poder consultar cuántas personas con discapacidad intelectual viven en Cataluña, consulté las estadísticas al respecto del mismo departamento. Cuando consulté y descargue por primera vez estos datos, el registro empezaba en el año 2.001 y finalizaban en 2.023. Sin embargo, a fecha de hoy en la web de la Generalitat, los datos se inician en 2.006, con un salto temporal hasta 2.015.

Tras juguetear un poco con los datos, vi que era necesario restructurar la base de datos con Python, así como crear una nueva con valores añadidos.


**FUENTE DE LOS DATOS**
- [Registre d’entitats, serveis i establiments socials serveis socials bàsics i especialitzats](https://analisi.transparenciacatalunya.cat/Societat-benestar/Registre-d-entitats-serveis-i-establiments-socials/ivft-vegh/about_data)
- [Estadístiques de persones amb discapacitat](https://dretssocials.gencat.cat/ca/ambits_tematics/persones_amb_discapacitat/estadistiquesdiscapacitat) 


**CONTENIDO DEL DASHBOARD**

**Filtros:**
- Año («any»): hace referencia al año del que se muestran los datos. Empieza en 2.001 y finaliza en 2.023.
- Provincia («província»): hace referencia de cuál de las 4 provincias de Cataluña se muestran los datos o bien si se recogen del conjunto de las 4 provincias.
- Servicio («servei»): hace referencia de cuál de los 3 tipos de viviendas se muestran los datos o bien si es de la totalidad de estos servicios.

**Indicadores y gráficos:**
- Viviendas («habitatges»): indicador y gráfico, que hace referencia a la cantidad total de viviendas para personas con discapacidad existentes.
- Viviendas nuevas («habitatges nous»): indicador y gráfico. Hace referencia a la cantidad de viviendas creadas ese año.
- Plazas («places»): indicador y gráfico. Hace referencia a la cantidad total de plazas existentes. A partir de este dato, podemos saber cuántas personas con discapacidad intelectual hacen uso de estos servicios.
- Plazas nuevas («places noves»): indicador y gráfico. Hace referencia a la cantidad de plazas nuevas creadas ese año.
- Plazas por vivienda nueva («places per habitatge nou»): indicador y gráfico. Hace referencia al promedio de plazas respecto a las viviendas nuevas que se han creado ese año.

- Tipo de entidad («tipus d’entitat»): indicador y gráfico. Hace referencia a la titularidad de la entidad que gestiona las viviendas (entidad de iniciativa pública, de iniciativa social o de iniciativa mercantil).
- Distribución de plazas («distribució de places»): gráfico boxplot. Hace referencia a cómo se distribuyen las diferentes viviendas en función de su número de plazas.
- Evolución de población y plazas («evolució de població i places»). Gráfico. Hace referencia a la cantidad total de personas con discapacidad intelectual censadas y de plazas en las viviendas.
- Aumento porcentual respecto 2.001 («augment percentual respecte 2.001). Gráfico. Hace referencia al aumento porcentual de cada año respecto a 2.001, que es el primer año del que tengo datos de población censada de personas con discapacidad intelectual.
- Personas por plaza y provincia («persones per plaça i província»). Gráfico. Hace referencia a la cantidad de personas con discapacidad intelectual censadas respecto al número de plazas totales existentes, en función de la provincia.
- Personas por plaza y comarca («persones per plaça i comarca»): Gráfico.

- Plazas por comarca («places per comarca»). Gráfico. Indica el número de plazas totales existentes de cada comarca.
- Viviendas por municipio («habitatges per municipi»). Mapa. Hace referencia a la cantidad de viviendas para personas con discapaciad intelectual existentes en cada municipio de Cataluña.

En breve podrás acceder a una versión de este dashboard en Tableau Public.

¡Muchas gracias por tu interés y espero que disfrutes consultando el dahsboard!
