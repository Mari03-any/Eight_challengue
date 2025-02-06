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
3. Escriba una función recursiva para calcular la operación de la potencia.<br>
4. Realice pruebas para calcular fibonacci con iteración o con recursión. Determine desde que número de la serie la diferencia de tiempo se vuelve significativa.<br>
5. Cuenta de stackoverflow 
[![Captura-de-pantalla-2025-02-05-184716.png](https://i.postimg.cc/dtfbYDYd/Captura-de-pantalla-2025-02-05-184716.png)](https://postimg.cc/N51J8sLf)<br>
6. Link del perfil de linkedin <br>
www.linkedin.com/in/maria-fernanda-parra-osorio-05169134b
