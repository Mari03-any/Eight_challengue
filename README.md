# Reto 8
Maria Fernanda Parra Osorio CC 1014980661 <br>
1.De los retos anteriores selecione 3 funciones y escribalas en forma de lambdas.<br>
```python
# Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente
if __name__ == "__main__":
   # Se pide el valor al usuario
    n = int(input("Ingrese el número de gallinas: "))
    m = int(input("Ingrese el número de gallos: "))
    k = int(input("Ingrese el número de pollitos: "))
    calcular_carne_aves = lambda n, m, k: (n * 6) + (m * 7) + (k * 1) # Se determina la función lambda con las variables y la formula para saber el peso total de los animales

    if n >= 0 and m >= 0 and k >= 0: # Condicional para confirmar los valores positivos
        carne_total = calcular_carne_aves(n, m, k)
        print("La cantidad total de carne de aves es:", carne_total, "kilos.") # Imprimir el resultado final
    else:
        print("El número de aves debe ser un valor positivo o cero.")
```
```python
#Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.
if __name__ == "__main__": 
  # Se pide el valor al usuario
    p = float(input("Ingrese el valor inicial del préstamo: "))
    i = float(input("Ingrese el interés compuesto (en porcentaje): "))
    n = float(input("Ingrese el número de meses: "))

    calcular_prestamo = lambda p, i, n: p * (1 + (i / 100))**n #Se ejecuta la función lambda, con la formula del valor del prestamo con las variables

    if p > 0 and i > 0 and n > 0: # Condicional para confimar valores positivos
        valor_c = calcular_prestamo(p, i, n) # Se crea una variable de la función
        print("El valor del préstamo después de", n, "meses es:", valor_c) # Imprimir el resultado final
    else:
        print("Ingrese valores positivos.")
```
```python
# Escriba un programa que pida 5 números reales y calcule el promedio

import math
 
if __name__ == "__main__":
  # Se pide el valor al usuario
  n = float(input("Ingrese el primer numero real:"))
  i = float(input("Ingrese el segundo numero real:"))
  x = float(input("Ingrese el tercer numero real:"))
  y = float(input("Ingrese el cuarto numero real:"))
  z = float(input("Ingrese el quinto numero real:"))

  calcular_promedio = lambda n, i, x, y, z: (n + i + x + y + z)/5 #Se ejecuta la función lambda, creando la suma dividido en la cantidad de valores

if n > 0 and i > 0 and x > 0 and y > 0 and z > 0: # Condicional para confimar valores positivos
    promedio = calcular_promedio(n, i, x, y, z) # Se crea una variable de la función
    print("Promedio",promedio,) # Imprimir el resultado final
else:
  print("Error: Ingresa solo números reales.")
```
2. De los retos anteriores selecione 3 funciones y escribalas con argumentos no definidos (*args).<br>
```python
# Escriba un programa que pida 5 números reales y calcule la raíz cúbica del menor número
def raiz_menor(*args):
    menor = min(args)  # Encuentra el valor mínimo de los argumentos
    return menor ** (1 / 3)  # Calcula la raíz cúbica del menor número

if __name__ == "__main__":
    # Ingresar los cinco números como parte de los argumentos
    n = float(input("Ingrese el primer numero real: "))
    i = float(input("Ingrese el segundo numero real: "))
    x = float(input("Ingrese el tercer numero real: "))
    y = float(input("Ingrese el cuarto numero real: "))
    z = float(input("Ingrese el quinto numero real: "))
    
    # Verificar si todos los números son positivos
    if n > 0 and i > 0 and x > 0 and y > 0 and z > 0:
        raiz_cubica = raiz_menor(n, i, x, y, z)  # Pasamos los números como *args
        print("Raíz cúbica del menor:", raiz_cubica)
    else:
        print("Error: Ingresa solo números reales.")
```
```python
# Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Taylor. 

import math

def exp_aprox(*args):
    x = args[0]  # Primer argumento es x
    n = args[1]  # Segundo argumento es el número de términos
    suma = 0  # Inicializa la suma
    for i in args[2]:  # Usamos los números pasados en args[2] como el rango de términos
        t = (x ** i) / math.factorial(i)  # Calcula el término con la función exponencial
        suma += t  # Suma el término a la secuencia
    return suma

if __name__ == "__main__":
    x = float(input("Ingrese el valor de x: "))  # Ingresar x
    n = int(input("Ingrese el número de términos de la serie: "))  # Ingresar el número de términos
    aprox = exp_aprox(x, n, range(n))  # Pasamos el rango de términos como parte de *args
    real = math.exp(x)  # Valor real de e^x

    print("Aproximación de e^x usando", n, "términos:", aprox)  # Imprimir la aproximación
    print("Valor real de e^x:", real)  # Imprimir el valor real
    print("Diferencia entre el valor real y la aproximación:", abs(real - aprox))  # Imprimir la diferencia
```
```python
# Una función matemática para calcular el área y el perimetro de un rectangulo 

import math

def calcular_perimetro_rectangulo(*args):
    a, b = args  # Desempaquetamos los argumentos
    perimetro_rectangulo = 2 * (a + b)
    return perimetro_rectangulo

def calcular_area_rectangulo(*args):
    a, b = args  # Desempaquetamos los argumentos
    area_rectangulo = a * b
    return area_rectangulo

if __name__ == "__main__":
    a = float(input("Ingrese el primer lado del rectángulo: "))
    b = float(input("Ingrese el segundo lado del rectángulo: "))
    r = float(input("Ingrese el radio de los círculos: "))

    if a > 0 and b > 0 and r > 0:
        # Llamadas a las funciones pasando los argumentos con *args
        perimetro_rectangulo = calcular_perimetro_rectangulo(a, b)
        area_rectangulo = calcular_area_rectangulo(a, b)
        
        print("El perímetro del rectángulo es:", perimetro_rectangulo)
        print("El área del rectángulo es:", area_rectangulo)

    else:
        print("El radio y los lados deben ser números positivos.")
```
3. Escriba una función recursiva para calcular la operación de la potencia.<br>
```python
def potencia_recursiva(base, n):
  # Caso base 
  if n == 0: # Cualquier numero elevado a 0 es 1
    return 1
  else:
    # Condicion de la funcion recursiva
    return base * potencia_recursiva(base, n - 1) # Crea el ciclo hasta que llegue a 0 y multiplica todos los resultados anteriores

if __name__ == "__main__":
  # El usuario ingresa el numero de la base y el exponente
  base = int(input("Ingrese la base: "))
  n = int(input("Ingrese el exponente: "))

  resultado = potencia_recursiva(base, n)
  print(base, " elevado a ", n , " es:", resultado,)
```
4. Realice pruebas para calcular fibonacci con iteración o con recursión. Determine desde que número de la serie la diferencia de tiempo se vuelve significativa.<br>
- Plantilla a tener en cuenta:
```python
import time

start_time = time.time()
# instrucciones sobre las cuales se quiere medir tiempo de ejecución
end_time = time.time()

timer = end_time - start_time
print(timer)
```
- La función recursiva de fibonacci:
```python
import time

def fibonacci_recursivo(n):
    if n <= 1:
        return n
    else:
        return fibonacci_recursivo(n-1) + fibonacci_recursivo(n-2)

```
- La función iterativa de fibonacci:
```python
def fibonacci_iterativo(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a
```
- Al unir y comparar todo obtenemos:
```python
import time

def fibonacci_recursivo(n): # Creamos la función recursiva
    if n <= 1: # Comenzamos con numero menores o igual a 0 por cada numero
        return n
    else:
        return fibonacci_recursivo(n-1) + fibonacci_recursivo(n-2)

def fibonacci_iterativo(n): # Creamos la fucnión iterativa
    a, b = 0, 1
    for _ in range(n): # Crear el rango de 0 a n
        a, b = b, a + b # Se suman las variables
    return a

def medir_tiempos():
    # Definir el rango de valores de n para probar (de 30 a 50)
    for n in range(30, 51):  # Probar para números de 30 a 50
        # Medir el tiempo de la versión recursiva
        start_time = time.time()
        fibonacci_recursivo(n)
        end_time = time.time()
        timer_recursivo = end_time - start_time
        
        # Medir el tiempo de la versión iterativa
        start_time = time.time()
        fibonacci_iterativo(n)
        end_time = time.time()
        timer_iterativo = end_time - start_time
        
        print("n =", n, ", Recursivo:", timer_recursivo, "segundos,", "Iterativo:", timer_iterativo, "segundos") # Imprimir el resultado 
        if timer_recursivo > timer_iterativo:
            print("   Diferencia significativa en n =", n) # Marca ek 30 que esta evaluando

if __name__ == "__main__":
    medir_tiempos()
```
- Finalmente, al pobrar un rango tan grande podemos decir que el interativo siempre es mucho mejor con una potencia negativa y con el numero e

5. Cuenta de stackoverflow 
[![Captura-de-pantalla-2025-02-05-184716.png](https://i.postimg.cc/dtfbYDYd/Captura-de-pantalla-2025-02-05-184716.png)](https://postimg.cc/N51J8sLf)<br>
6. Link del perfil de linkedin <br>
www.linkedin.com/in/maria-fernanda-parra-osorio-05169134b  <br>
*FIN*
