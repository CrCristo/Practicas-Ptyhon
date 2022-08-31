## Ordenar númerons de menor a mayor

Observar cómo: 

Agregar elementos a una lista con lista.append(variable)

Ordenar los elementos de una lista de menos a mayor (números y letras) con lista.sort()

      cant= int(input("Ingrese la cantidad de números a ordenar: "))
      nums= []
      for i in range (0,cant):
        nums.append(int(input("Ingrese el número: ")))
      nums.sort()
      print (nums)

## Adivinar el número secreto

Observar cómo: 

Sacar un número aleatorio con import random y  random.randint(rango)

Usar un while(condición): y break  

Dos numeros distintos ( != )

      import random
      num_sec= random.randint(0,10)
      vidas=5
      print ("Bienvenido al - Nùmero Secreto -\nAdivina el nùmero entre 0 y 10")
      num_ply= int(input("Ingresa tu número: "))
      while ((vidas!=0 or num_ply!=num_sec) and 0<=num_ply<=10):
        vidas = vidas-1
        if num_ply==num_sec:
          break
        elif num_ply<num_sec:
          print ("El número es más grande")
        else:
          print ("El número es más pequeño")
        print (vidas, " vidas restantes")
        num_ply= int(input("Ingresa tu número: "))  
      if num_sec==num_ply:
          print ("¡Felicidades! Encontraste el - Número Secreto -")
      elif vidas==0:
        print ( "Perdiste.")
      else:
        print ("Formato inválido")
      print ("El número secreto es ",num_sec)

Buscar forma de no usar tanto if

## Write a Python function that takes a sequence of numbers and determines whether all the numbers are different from each other

### prueba 1

    inicio
    declarar num_1,num_2(int)
    if num_1!=num_2   o   num_1-num_2==0   o  num_1/num_2=1   o  if list_num/num_1 != 1 
          print ("los números son distintos")
    fin
    
### prueba 2

    inicio
    for i in range (vars_list):
          elelemtos de la lista/num_1
          if != 1 
          print ("el elemento #"posicions del elementos en la lista,"sea : (",elemento de la lista,"), es diferente."
    fin

    for i in range (numero de variables)
    num_n int input ()
          for i in range (vars_list):
                elelemtos de la lista/num_n
                if != 1 
                print ("el elemento #"posicions del elementos en la lista,"sea : (",elemento de la lista,"), es diferente de", num_n.
    num_n.append(lista)


## Write a Python program to create all possible strings by using 'a', 'e', 'i', 'o', 'u'. Use the characters exactly once

 Observar como calcular un factrorial y como sacar permutaciones y utilización de if con string

 permutaciones:  https://ajaxhispano.com/ask/generar-todas-las-combinaciones-de-una-lista-en-python-110467/
 
 combinaciones: https://www.delftstack.com/es/howto/python/combinations-of-list-in-python/
 
 ordenar de diferentes formas: --

    inicio
    declarar numero de variables(int), variable a añadir(char), lista de variables
    mostrar ("Ingresar la cantidad de elementos a revisar")
    asignar número de variables
    for i in range número de variables 
          mostrar "Ingrese la variable a añadir"
          asignar variable a añadir
          Añadir a  lista de variables
    for i in range númer de variables !
          mostrar permutaciones de lista de variables
    fin

#### Código

            from itertools import permutations
            num_vars = int(input("Ingrese la catidad de elementos a revisar: "))
            vars = []
            for i in range (num_vars):
              var_n = str(input("Ingrese la variable a añadir: "))
              vars.append(var_n)
              
            #calcular una factorial
            
            fact = 1
            for i in range(1, num_vars+1):
              fact = fact * i
            print ("Hay",fact,"permutaciones para los elementos ingresados \n¿Desea mostrarlas?")
            
            #preguntar si mostrar las permutaciones
            
            des=str(input("y/n: "))
            if des=="y" or des=="Y":
            
            #crear todas las permutaciones posibles
            
              permutations = list(permutations(vars))
              print(permutations)      

## Write a Python program to remove and print every third number from a list of numbers until the list becomes empty.
métodosde eliminación de una lista 
 https://uniwebsidad.com/libros/python/capitulo-7/metodos-de-eliminacion
contar el número de elementos de una lista 
 https://www.delftstack.com/es/howto/python/count-elements-in-list-python/#:~:text=lista%20en%20Python.-,Utilice%20la%20funci%C3%B3n%20len()%20para%20contar%20el%20n%C3%BAmero%20de,tipo%20de%20elementos%20que%20contiene.
último elemento de una lista 
 https://www.delftstack.com/es/howto/python/get-last-element-of-list-in-python/

    inicio
    vars = []
    mientras la lista tenga elementos 
          mostrar lista
          eliminar elemento indice 3
          si elementos de la lista<3
          eliminar dos y uno 


### Código

    num_vars = int(input("Ingrese la catidad de elementos a revisar: "))
    vars = []
    for i in range (num_vars):
      var_n = str(input("Ingrese la variable a añadir: "))
      vars.append(var_n)
    while len(vars)!=0:
      print (vars)
      if len(vars)>=3:
        vars.pop(2)
      else:
        vars.pop(-1)
