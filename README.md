# Project-Espagna
# <center> Clasificación de las comunas de la ciudad de Medellin

Medellín es un municipio colombiano, capital del departamento de Antioquia. Es la ciudad más poblada del departamento y la segunda más poblada del país después de Bogotá. Se asienta en la parte más ancha de la región natural conocida como Valle de Aburrá, en la cordillera central de los Andes. Se extiende a ambas orillas del río Medellín, que la atraviesa de sur a norte, y es el núcleo principal del área metropolitana del Valle de Aburrá. La ciudad tiene una población proyectada de 2 508 452 habitantes (2018).

**Diseño de experimento:**

Se buscaron datos de las comunas de la ciudad en wikipedia, las variables que se pudieron obtener fueron:

* Nombre
* Zona
* Año de fundación
* Superficie en Km
* Total de Habitantes
* IDH
* Porcentaje de habitantes menores de 14 años
* Porcentaje de habitantes con edad entre 15 y 39 años
* Porcentaje de habitantes con edad entre 40 y 64 años
* Porcentaje de habitantes mayores de 65 años
* Porcentaje de habitantes Mestizos-Blancos
* Porcentaje de habitantes Afro
* Porcentaje de habitantes Indígenas
* Número total de barrios pertenecientes a la respectiva comuna.

# Problema

Se desea conocer que comunas de la ciudad son mas parecidas entre si dadas unas variables geo-poblacionales.

# Objetivo

Se desarrollo un prototipo capaz de identificar las posibles comunas similares. Se aplicaron técnicas de clasificación no supervisada.

# Resultados y conclusiones

Para identificar el número de subgrupos se utilizó Kmedias, rotando la K desde 1 hasta 17, por método del codo se tomó k = 3, pero es valido k = 2, 3, 4, 5, también se puede utilizar método de la silueta para identificar la K optima. También se pueden utilizar métodos jerárquicos como dendrograma.

Figura 1: Método del codo

![alt text](https://github.com/oecorrechag/Proyecto-Barcelona-Comunas/blob/master/codo.png)

Figura 2: Subgrupos

![alt text](https://github.com/oecorrechag/Proyecto-Barcelona-Comunas/blob/master/dendro.png)

Para K = 2, la comuna del Poblado queda separada de todas las demas.
Para K = 3, la comuna del Poblado conforma un grupo, la comuna de la candelaria (centro) conforma otro grupo, y quedan separadas de todas las demas comunas.
Se encontro que para todas las k la comuna del Poblado queda separada de todas las demas, esto puede ser que tiene mas cantidad de barrios y  mayor superficie. 

### Bibliografia

* Cournapeau, D., (2007), scikit-learn. Recuperado de: https://scikit-learn.org

* Comunas de Medellín. (s.f.). (2020). En Wikipedia. Recuperado en: https://es.wikipedia.org/wiki/Comunas_de_Medellín