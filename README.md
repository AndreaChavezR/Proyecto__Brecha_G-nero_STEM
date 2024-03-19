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

Dataset final 
![Dataset después de realizar las modificaciones anteriores .](https://github.com/AndreaChavezR/Proyecto__Brecha_G-nero_STEM/blob/main/imagenes/imagen%20dataframe.png)

