# LIBRERÍA COMPUTACIÓN CUÁNTICA: NÚMEROS COMPLEJOS

##  Introducción
Este laboratorio tiene como objetivo crear una librería en Python para poder operar números complejos, el desarrollo de la implementación por operaciones es el siguiente:

#### Suma
La suma de números complejos esta definida de la siguiente manera...

* (a1 + b1i) + (a2 + b2i) = (a1 + a2) + (b1 + b2)i

La solución en Python es:

    def suma_complejos(x,y):
    a = x[0] + y[0]
    b = x[1] + y[1]

    return (a,b)
#### Producto.
El producto de números complejos esta definido de la siguiente manera...

* (a1 + b1i) × (a2 + b2i) = ((a1a2) − (b1b2)) + ((a1b2) + (a2b1))

La solución en Python es:

    def suma_complejos(x,y):
    a = x[0] + y[0]
    b = x[1] + y[1]

    return (a,b)


#### Resta.
La resta de números complejos esta definida de la siguiente manera...

* (a1 + b1i) - (a2 + b2i) = (a1 - a2) + (b1 - b2)i

La solución en Python es:

    def suma_complejos(x,y):
    a = x[0] + y[0]
    b = x[1] + y[1]

    return (a,b)


#### División.
La division de números complejos esta definida de la siguiente manera...

* (a1 + b1i) / (a2 + b2i) = (((a1 * a2) + (b1 * b2)) / ((a2)^2^ +(b2)^2^ ))+ (((a2 * b1) − (a1 * b2)) / ((a2)^2^+(b2)^2^))i

La solución en Python es:

    def division_complejos(x,y):
    a = ((x[0]*y[0]) + (x[1]*y[1]))/((y[0]**2)+(y[1]**2))
    b = ((x[1]*y[0]) - (x[0]*y[1]))/((y[0]**2)+(y[1]**2))

    return(a,b)


#### Módulo.
El modulo de números complejos esta definida de la siguiente manera...

*| | : ℂ → ℝ : | c | = |a + bi| =**√ (a2)^2^+(b2)^2^** 

La solución en Python es:

    def modulo_complejos(x):
    c = ((x[0]**2)+(x[1]**2))**(1/2)
    
    return c


#### Conjugado.
El conjugado de números complejos esta definida de la siguiente manera...
* ¯ : ℂ → ℂ : ¯c¯ = ¯a + bi¯ = a − bi

La solución en Python es:

    def conjugado_complejos(x):
    
    return (x[0],x[1]*-1)


#### Conversión entre representaciones polar y cartesiano.
La solución en Python es:

    def polar_cartesiano_complejos(x):

    r = x[0]
    angulo = math.radians(x[1])
    a = r * math.cos(angulo)
    b = r * math.sin(angulo)
    return [a, b]
    
    def cartesiano_polar_complejos(x):
    angulo = math.degrees(math.atan2(x[1], x[0]))
    r = math.sqrt((x[0]**2) + (x[1]**2))
    
    return [r, angulo]


#### Retornar la fase de un número complejo.
La Fase de un numero complejo esta definida de la siguiente manera...

* c ≡ α = arctg (b/a)

La solución en Python es:

    def fase_complejos(x):
    c = math.degrees(math.atan2(x[1], x[0]))

    return c
## inventario
1. lib_complejos.py
2. test_lib_complejos.py

### Ejecución

1. Para abrir los archivos debe ejecutarlos con un software que pueda reconocer lenguajes como python.
2. Para ejecutar las pruebas debe tener un compilador que sea capaz de ejecutar python 3 
3. Para usar la libreria en otro codigo debe importarla de la siguiente forma:

     import lib_complejos as lb 
     
     Debe usar también el indicador de la importación al principio de la invocación de cada función 
     
     lb.suma_complejos(x,y), (11,4)
