# Proyecto de Análisis de Datos: Brecha de Género en STEM con Python

## :open_book: Introducción

En el mundo actual, la Ciencia, Tecnología, Ingeniería y Matemáticas (STEM) son campos que impulsan la innovación, el desarrollo y el progreso de nuestra sociedad. Sin embargo, existe una brecha de género notable en estos campos. A pesar de los avances significativos en la igualdad de género en las últimas décadas, las mujeres siguen estando subrepresentadas en las disciplinas de STEM.

¿Sabías que la participación de las mujeres en STEM es considerablemente menor en comparación con la de los hombres? Esta disparidad no solo limita la diversidad y la inclusión en estos campos vitales, sino que también restringe el potencial de desarrollo e innovación al excluir a las mujeres de estas áreas críticas.

Este proyecto está basado en en el El proyecto "Inequality in STEM" disponible en la plataforma de [Kaggle.](https://www.kaggle.com/code/minkles/inequality-in-stem/notebook)

## :dart: Objetivos

Este proyecto tiene como propósito desarrollar un modelo de aprendizaje automático para identificar y comprender las causas principales de la brecha de género en STEM. Utilizaremos gráficos intuitivos y técnicas de machine learning aplicadas a los datos recopilados.

El modelo buscará responder preguntas clave, y complementaremos nuestras respuestas con visualizaciones:
### ¿Cómo influye el origen hispano en la participación en carreras STEM?
 - Analizaremos la participación en STEM en relación con el origen hispano.
 - Mediremos la participación de diferentes grupos hispanos en carreras STEM, revelando patrones y tendencias significativas.
### ¿Existen disparidades de género significativas en la población hispana en STEM?
 - Examinaremos la distribución de género en la participación hispana en carreras STEM.
 - Identificaremos posibles desequilibrios de género entre hombres y mujeres en campos STEM, destacando disparidades.
### ¿Cómo varía la brecha de género en STEM con diferentes grupos de edad?
 - Analizaremos la evolución de la brecha de género en carreras STEM en diferentes grupos de edad.
 - Identificaremos patrones de cambio en la participación de hombres y mujeres a medida que avanzan en sus carreras.
 ### ¿Existen diferencias notables en la participación de géneros en STEM según la edad?
 - Investigaremos posibles variaciones en la participación de hombres y mujeres en carreras STEM en relación con la edad.
 - Identificaremos diferencias significativas en la distribución de género a lo largo de la
trayectoria educativa y profesional.
### ¿Se observan patrones significativos de inequidad de género en STEM en grupos raciales específicos?
 - Investigaremos la existencia de patrones notables de inequidad de género en campos STEM dentro de grupos raciales específicos.
 - Identificaremos posibles disparidades en la participación de hombres y mujeres en STEM en contextos raciales específicos.

El objetivo final de este proyecto es implementar estrategias efectivas que reduzcan significativamente la brecha de género en el campo de STEM. Buscamos promover la equidad de oportunidades y maximizar el potencial de todas las personas en STEM, contribuyendo así a un futuro más inclusivo e innovador en estas disciplinas.

## Análisis y limpieza de los Datos 
Para comenzar con el análisis de los datos se utilizó el siguiente conjunto de datos:
- [ss13pusa.csv](https://drive.google.com/file/d/1_5t_pSyMYnaYmBUjjArcUwUQDk7-ho6I/view?usp=sharing)

Antes de comenzar con la limpieza de los datos, se realizó el análisis del conjunto de datos para definir las columanas a utilizar. Derivado de este análisis se notó que en algunas de las columnas no contaban con datos (NaN) y contenia datos String, debido a esto se realizaron cambios en las siguientes columanas:

- Género: Se Cambio el valor 1 a 0, representando la categoría masculina y el valor 2 a 1, representando la categoría femenina.
- recodificar_raza: Se agregaron nuevas categorías son 'Hispano', 'Blanco', 'Negro', 'Asiático' y 'Otro'.
- Creamos una nueva variable llamada 'titulo_stem' para indicar si una persona tiene un título en STEM.
- Utilizamos un diccionario llamado 'mapa_titulo_stem' para asignar el valor 1 a aquellos con un título STEM y 0 a los demás.
- Creamos la columna 'ocupacion_stem' para indicar si una persona tiene una ocupación en STEM.
- Utilizamos una lista de códigos específicos asociados con ocupaciones en ciencia y tecnología.
- Paara finalizar se eliminaron columnas no necesarias ('Origen_Hispano', 'Lugar_Nacimiento', 'Raza', 'Ciencia_Tecnologia', 'Ocupacion').

Dataset después de realizar las modificaciones anteriores

![](https://github.com/AndreaChavezR/Proyecto__Brecha_G-nero_STEM/blob/main/imagenes/imagen%20dataframe.png)

#### Resumen de registros por origen hispano y el total de ocupación STEM 

| origen_hispano       | ocupacion_stem |
| -------------        | -------------  |
| No Hispano/Latino    |	   2727306     |
| Mexicano	            |    329060      |
| Puertorriqueño	      |    38836       |
| Cubano	              |    28530       |
| Salvadoreño	         |    18188       |
| Otros Hispano/Latino	|    15516       |
| Guatemalteco	        |    12534       | 
| Colombiano	          |    10260       |
| Español	             |    7458        |
| Dominicano	          |    7424        |
| Peruano	             |    5826        |
| Hondureño	           |    5608        |
| Nicaragüense	        |    5080        |
| Ecuatoriano	         |    3624        |
| Venezolano	          |    2748        |
| Argentino            |   	2686        |
| Panameño	            |    1630        |
| Chileno	             |    1560        |
| Costarricense	       |    1288        |
| Boliviano	           |    836         |
| Uruguayo	            |    548         |
| Otro Centroamericano	|    378         |
|Otro Sudamericano	    |    232         |
| Paraguayo	           |    188         |

#### Tasas de títulos en ciencias por origen hispano
| origen_hispano       |   titulo_stem  |
| -------------        | -------------  |
| Argentino            |    	0.148920   |
| Venezolano	          |     0.144105   |
| Chileno	             |     0.137179   |
| Uruguayo	            |     0.102190   |
| Colombiano	          |     0.097856   |
| Boliviano	           |     0.095694   |
| Peruano	             |     0.092688   |
| No Hispano/Latino	   |     0.088863   |
| Español	             |     0.086618   |
| Panameño	            |     0.083436   |
| Ecuatoriano	         |     0.078366   |
| Cubano	              |     0.075640   |
| Paraguayo	           |     0.074468   |
| Costarricense	       |     0.069876   |
| Nicaragüense	        |     0.053937   |
| Otro Centroamericano	|     0.052910   |
| Dominicano	          |     0.048491   |
| Puertorriqueño	      |     0.043362   |
| Otro Sudamericano	   |     0.043103   |
| Otros Hispano/Latino	|     0.041634   |
| Salvadoreño	         |     0.025511   |
| Guatemalteco	        |     0.024254   |
| Hondureño	           |     0.023894   |
| Mexicano	            |     0.021637   |


### Gráfico sobre la relación en STEM con el origen hispano y el género

![](https://github.com/AndreaChavezR/Proyecto__Brecha_G-nero_STEM/blob/main/imagenes/grafico%201.png)

En el anterior grafico se pueden realizar las siguientes observaciones:

- Se observa una variación significativa en la participación entre diferentes orígenes hispanos. Algunos orígenes, como “Argentino” y “Venezolano”, muestran una mayor participación masculina en STEM. Para otros orígenes, como “Boliviano” o “Paraguayo”, la diferencia entre géneros no es tan pronunciada.

- Las altura de las barras correspondientes a cada país o región de origen, se puede comparar la participación en STEM. Esto puede revelar patrones o tendencias específicas, como qué regiones tienen mayor o menor representación en estas áreas.

- Si algunas barras son notablemente más altas o más bajas que otras, esto podría indicar áreas de oportunidad o desafíos particulares en la promoción de STEM entre ciertos grupos.

- Implicaciones Sociales: La participación en STEM es un indicador importante del acceso a educación y oportunidades laborales en campos técnicos.

### Gráfico de tasas de títulos en STEM por edad y sexo

![](https://github.com/AndreaChavezR/Proyecto__Brecha_G-nero_STEM/blob/main/imagenes/grafico%202.png)

En el anterior grafico se pueden realizar las siguientes observaciones:

- La gráfica muestra una diferencia notable en la representación de género en STEM. El porcentaje de hombres con títulos en STEM es consistentemente más alto que el de las mujeres en todas las edades.

- Ambas curvas muestran un aumento rápido hasta los 20 años, sin embargo, d de los 20 años, hay una disminución gradual, lo que podría indicar una disminución en la participación en la educación o en carreras en STEM.

### Gráfico de la distribución de Género por Origen Hispano en Grupos Raciales

![](https://github.com/AndreaChavezR/Proyecto__Brecha_G-nero_STEM/blob/main/imagenes/grafico%204.png)

En el anterior grafico se pueden realizar las siguientes observaciones:

- Las barras son coloreadas para representar diferentes orígenes hispanos y géneros; los hombres están marcados con tonos más oscuros mientras que las mujeres están en tonos más claros.

- La gráfica muestra una barra prominente en el grupo racial “Blanco”, indicando una alta cantidad de individuos en esta categoría. Las otras categorías, como “Afroamericano”, “Asiático”, “Indio Americano” y “Otro” tienen barras mucho más bajas, lo que indica una menor cantidad de individuos.


