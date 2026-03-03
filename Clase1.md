#### **1. Operaciones básicas.** 
Lo primero que podemos hacer en RStudio es utilizarlo como calculadora, para esto simplemente debemos usar símbolo que corresponda. 


``` r
10+10
```

```
## [1] 20
```

``` r
10-5
```

```
## [1] 5
```

``` r
5*8
```

```
## [1] 40
```

``` r
25/5
```

```
## [1] 5
```

``` r
sqrt(144)
```

```
## [1] 12
```

``` r
12**2
```

```
## [1] 144
```

---

#### **2. Crear un vector.** 
Un vector en R es la estructura de datos más básica, consistente en una secuencia ordenada de elementos de un mismo tipo. Para crearlo utilizamos la función **c()** que significa "concatenar" o "combinar". El vector debe tener un nombre conocido y no tan genérico para que sea fácil de recordar, de escribir y no se confunda con otros que puedas estar usando paralelamente. Además, debe estar acompañado del signo **<-** que sirve para indicar todo lo que contendrá el vector.


``` r
# Vector de caracteres
x <- c("a", "b", "c", "d")
x
```

```
## [1] "a" "b" "c" "d"
```

``` r
# Vector numérico
hola <- c(1, 2, 3, 4, 5)
hola
```

```
## [1] 1 2 3 4 5
```

---

#### **3. Operaciones con vectores.** 
Una de las caracteristicas más potentes de R es la **vectorizacion**. Esto significa que cualquier operación aritmética que apliquemos a un vector, se realizará automáticamente para cada uno de los elementos que contiene, sin necesidad de hacerlo uno por uno.


``` r
# Sumar o restar un valor constante a todos los elementos
hola + 1
```

```
## [1] 2 3 4 5 6
```

``` r
# Crear dos vectores nuevos
mi_vector_1 <- c(1, 2, 3)
mi_vector_2 <- c(4, 5, 6)

# Operar entre vectores (elemento por elemento)
mi_vector_1 + mi_vector_2
```

```
## [1] 5 7 9
```

``` r
# También podemos "pegar" o juntar varios vectores en uno solo
mi_vector_3 <- c(mi_vector_1, mi_vector_2)
mi_vector_3
```

```
## [1] 1 2 3 4 5 6
```

---

#### **4. Secuencias numéricas.** 
R permite generar listas de números ordenados  utilizando el operador **:**.


``` r
# Secuencia simple del 1 al 10
1:10
```

```
##  [1]  1  2  3  4  5  6  7  8  9 10
```

``` r
# Secuencia en orden inverso
10:1
```

```
##  [1] 10  9  8  7  6  5  4  3  2  1
```

``` r
# Vector con una secuencia del 1 al 10
secuencia <- c(1:10)
```

---

#### **5. Matrices.** 
Una matriz es una estructura de datos bidimensional (organizada en filas y columnas). A diferencia de los vectores, tienen dos dimensiones, pero mantienen la regla de que todos sus elementos deben ser del mismo tipo (generalmente números).


``` r
# Crear una matriz a partir de una secuencia de 1 al 12
# Podemos definir el número de filas (nrow) y columnas (ncol)
matrix(1:12, nrow=3, ncol=4)
```

```
##      [,1] [,2] [,3] [,4]
## [1,]    1    4    7   10
## [2,]    2    5    8   11
## [3,]    3    6    9   12
```

``` r
# O cambiar la orientación a 4 filas y 3 columnas
matrix(1:12, nrow=4, ncol=3)
```

```
##      [,1] [,2] [,3]
## [1,]    1    5    9
## [2,]    2    6   10
## [3,]    3    7   11
## [4,]    4    8   12
```

``` r
# También podemos realizar operaciones matemáticas directas sobre toda la matriz
mi_matriz <- matrix(1:9, nrow=3, ncol=3)
mi_matriz * 2
```

```
##      [,1] [,2] [,3]
## [1,]    2    8   14
## [2,]    4   10   16
## [3,]    6   12   18
```

``` r
mi_matriz^3
```

```
##      [,1] [,2] [,3]
## [1,]    1   64  343
## [2,]    8  125  512
## [3,]   27  216  729
```

---

#### **6. Data Frames.** 
El Data Frame esla estructura más importante en arqueología. A diferencia de la matriz, un Data Frame permite que cada columna tenga un tipo de dato diferente (por ejemplo: una columna con nombres de sitios, otra con tipos de cerámica, etc.). Es lo más parecido a una tabla de Excel.


``` r
# Crearemos un set de datos (dataset) con 3 columnas
mi_dataframe <- data.frame(
  "secuencia" = 1:4, 
  "letra" = c("a", "b", "c", "d"), 
  "numero" = c(1.2, 3.4, 4.5, 5.6)
)

mi_dataframe
```

```
##   secuencia letra numero
## 1         1     a    1.2
## 2         2     b    3.4
## 3         3     c    4.5
## 4         4     d    5.6
```

``` r
# Podemos consultar información básica del Data Frame
length(mi_dataframe) # Nos da el número de columnas
```

```
## [1] 3
```

``` r
names(mi_dataframe)  # Nos da los nombres de las columnas
```

```
## [1] "secuencia" "letra"     "numero"
```

---

#### **7. Coerción de datos.** 
En R, "coercionar" significa forzar un objeto de un tipo a otro. Es muy común, por ejemplo, convertir una matriz de números en un Data Frame para poder procesarlo con herramientas estadísticas más avanzadas.


``` r
# Creamos una matriz simple
matriz_ejemplo <- matrix(1:12, ncol=4)

# La transformamos a Data Frame
df_final <- as.data.frame(matriz_ejemplo)

df_final
```

```
##   V1 V2 V3 V4
## 1  1  4  7 10
## 2  2  5  8 11
## 3  3  6  9 12
```

<div style="text-align: center; margin-top: 50px; margin-bottom: 30px;">
  
  <a href="" class="btn btn-default">← Clase Anterior</a>
  <a href="index.html" class="btn btn-default" style="margin: 0 10px;">Índice</a>
  <a href="Clase2.html" class="btn btn-default">Siguiente Clase →</a>

</div>
