---
layout: default
---

# Partición binaria del espacio (BPS)

Algoritmo para subdividir recursivamente un espacio en elementos convexos empleando hiperplanos. Esta subdivisión da lugar a una representación de la escena por medio de una estructura de datos del árbol conocida como árbol de **BSP**.

## [](#header-2)Indice

1. Introducción
  * ¿Qué se quiere hacer?
  * Motivación (Doom games)
2. Estado del Arte
  * Alternativas
3. Método
  * consideraciones formales
  * Marco Teorico
  * Análisis computacional
  * Matemáticas
4. Referencias y Bibliografía

## [](#header-2)1. Introducción

La representación 3D(3D rendering), tiene una amplia variedad de aplicaciones que
incluyen:

- Ilustraciones gráficas.
- Juegos de primera persona (Doom, Quake, RPGs).
- Simulaciones virtuales en tiempo real (RV- Realidad virtual, Simulaciones de vuelo).
- Animaciones.
- Películas.

#### [](#header-4)Motivacion:
El algoritmo de Partición binaria del espacio (BSP) es uno de los más usados para generar mapas de juegos como Doom en los que la vista de primera persona (FPV)



## [](#header-2)2. Estado del Arte

## [](#header-2)3. Método

#### [](#header-4)Marco Teórico:

En cuanto a la división binaria del espacio (BSP/Binary Space Partition), este se
puede entender cómo un esquema que sirve para dividir un conjunto de objetos, en
sub partes llamadas hiperplanos hasta lograr que todos los objetos que se quería
dividir, estén separados (Paterson & Yao, 1992). Esta fue mostrada por primera vez
en el año de 1969 por Shumacker, Brand, Gilliland & Sharp, y aunque no fue creada
para ser usada en la industria de creación de juegos, desde los 90´s los árboles
BSP mejoran el rendimiento y posibilitan la creación de más detalles en los mapas
de éstos (Ranta-EsKola & Olofsson, 2001).

Sobre los árboles BSP también se ha encontrado que el diseño inicial de su algoritmo
se creó con la finalidad de ordenar polígonos, ya que en la época que este se desarrolló,
no se habían creado aún los hardware acelerados Zbuffers, y el software Z-buffering se
caracterizaba por su lentitud en el funcionamiento (Ranta-EsKola & Olofsson, 2001).

Entre los posibles usos que se le pueden dar a los BSP, se encuentran los que la
computación de modelos geométricos en 3D da a ellos. Esta debe realizar manipulaciones
de objetos y para ello, debe descomponerlos y reducir el número de operaciones que
esto implica; así se da uso a los BSP, que muestran una representación de la geometría
y una estructura de búsqueda (Naylor, 1998). Estos también son utilizados en la
creación de mapas de los juegos Doom (John Carmack and John Romero, 1997), en
especificidades como la estructura de datos que se crea para la remoción de la
superficie oculta en tiempo real, trazado de rayos y modelado sólido (esto en
gráficos para computadora) (Paterson & Yao, 1992).

Con el fin de profundizar en la descripción sobre los Doom, se encuentra en la
literatura gris que el Doom rendering engine, sería el núcleo del motor del juego
que se utiliza para dar potencia a otros juegos del software id, a través de un
falso 3D. Este motor usa el sistema BSP que se ha venido describiendo, con el fin
de dividir cada nivel en áreas de los nodos, y estos en subnodos, todo para dividir
subsectores en el orden correcto que beneficien la representación (doom.wikia.com,
2017).

Los problemas que los creadores de los juegos Doom deben solucionar, rondan alrededor
del cálculo de visibilidad, lo cual significa que las paredes y objetos que están
visibles en el juego deben dibujarse así: las paredes cercanas se dibujan delante
de las lejanas. Para solucionar este y otros inconvenientes a la hora del diseño,
existen los ya mencionados BSP (soulsphere.org, 2017).


## [](#header-2)4. Referencias y Bibliografía
* [Video de "3D Rendering"](https://www.youtube.com/watch?v=yTRzfKh4Tg0).
* Naylor, B. F. (1998). A tutorial on binary space partitioning trees. In Computer Games Developer Conference Proceedings (pp. 433-457).
* N.N. (2017) Binary Space Partitioning (BSP) and its use in 3-D Rendering. Recuperado de: [apocrypha/bsp](https://soulsphere.org/apocrypha/bsp/).
* N.N. (2017) Doom rendering engine. Recuperado de: [Doom_rendering_engine](http://doom.wikia.com/wiki/Doom_rendering_engine ).
* Paterson, M. S., & Yao, F. F. (1992). Optimal binary space partitions for orthogonal objects. Journal of Algorithms, 13(1), 99-113.
* Ranta-Eskola, S., & Olofsson, E. (2001). Binary space partioning trees and polygon removal in real time 3d rendering. Uppsala master’s theses in computing science, 179, 1-19.



[home](./)
