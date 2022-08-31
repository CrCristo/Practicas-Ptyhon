# Ejercicios con módulos

## Ejercicio 1
Escribir un programa en python modularmente qu determine ciantos años bisiestos existen en un periodo dado por el usuario.
Ej : de 1999 a 2010 3 años bisiestos

Nota: un año bisiesto si es múltiplo de 4 salvo el caso en qu sea múltiplo de 100 que no es bisiesto y no sea multiplo de 400. 
Ej. el año 1900 no fue bisiesto e 2000 sí lo es y el 2100 no lo es.

#### Planteamiento

    Inicio
    Declarar año de inioio(int), año de fin(int), año bisiestos[], num de años bisiestos(int)
    Asignar num de años bisiestos=0
    mientras año de inioio diferente de año de fin
      If año de inioio modular 4 == 0 and año de inioio modular 100 != 0 and año de inioio modular 400 != 0 
        num de años bisiestos =num de años bisiestos+1
        año bisiestos.append(año de inicio)
      año de inioio = año de inioio + 1
    mostrar (num de años bisiesto, año bisiestos)

  
#### Programa

      año_in= int(input("Ingrese el año del inicio del periodo: "))
      año_fin= int(input("Ingrese el año del fin del periodo: "))
      años_bis = []
      num_años_bis = 0
      while año_in != año_fin:
        if año_in%4==0 and año_in%100!=0 and año_in%400!=0 :
          num_años_bis = num_años_bis +1
          años_bis.append(año_in)
        año_in=año_in +1
      print (num_años_bis,años_bis)


## Ejercicio 2
La fecha de cualquier domingo de Pascua se calcula de la siguiente forma 
Sea X el año para el que se quiere calcular la fecha 
Sea A el resto de la division de X entre 19
Sea B el resto de la division de X entre 4
Sea C el resto de la division de X entre 7 
Sea D el resto de la division de (19*A+24) entre 30
Sea E el resto de la division de (2*B+4*C+6*D+5) entre 7
La fecha para el domingo de pascua es el día (22+D+E) de Marzo
(observese que puede dar una fehca en mes de abril)

Escribir  un programa en Python  modularmente  que pida como entrada un año y saque por pantalla la fecha ddel Domingo de Pascua para ese año

    Inicio
        Declarar X,A,B,C,D,E, domingo de pascua
        Mostrar ("ingresar el año")
        Asignar X
        Asignar A = X modular 19
        Asignar B = X modular 4
        Asignar C = X modular 7
        Asignar D =  (19*A+24) modular 30
        Asignar E =  (2*B+4*C+6*D+5) modular 7
        Asignar domingo de pascua = (22+D+E)
        if  domingo de pascua<=31:
          print (domingo de pascua,"de Marzo del ", X)
        else:
          domingo de pascua=domingo de pascua-31
          print (domingo de pascua,"de Abril del ", X)

Nota: marzo tiene 31 días 

### programa
    pascua=0
    año=int(input("ingresar el año: "))
    A = año%19
    B = año%4
    C = año%4
    D =  (19*A+24)%30
    E =  (2*B+4*C+6*D+5)%7
    pascua= (22+D+E)
    if  pascua<=31:
      print (pascua,"de Marzo del ", año)
    else:
      pascua=pascua-31
      print (pascua,"de Abril del ", año)


## Ejercicio 3
La ley de los cosenos establece:  Para cualquier triangulo que se encuetre en el plano, con ángulos internos: alpha,beta,gamma y longitudes de lados opuestos a,b,c reespectivamente se cumple:
a/sen alpha  = b/senbeta = c/sengamma
a=6
alpha=20
beta=80
escribir un programa en python modularmente que solicite estos datos y determine b,c,el angulo de gamma y el perimetro del triangulo

#### Planteamiento

    de math importar sen,cos, tan
    Declarar alpha,beta,gamma,a,b,c,perimetro
    mostrar (Ingrese el valor de a: )
    asignar a
    mostrar (Ingrese el valor de alpha: )
    asignar alpha
    mostrar (Ingrese el valor de beta: )
    asignar beta
    asignar gamma=180-(beta + alpha)
    b = (a/sen alpha)*senbeta
    c = (a/sen alpha)*sengamma
    perimetro = a+b+c
    print ("Los valores de los angulos: alpha,beta,gamma del triangulo son: ",  alpha,beta,gamma, "respectivamente.\nLos valores de los lados: a,b,c del triangulo son: ",a,b,c,"respectivamente.\nEl perimetro del triangulo es ",perimetro," unidades."


#### programa

    import math
    a = int(input("Ingrese el valor de a: "))
    alpha = int(input("Ingrese el valor de alpha: "))
    beta = int(input("Ingrese el valor de beta: "))
    gamma=180-(beta + alpha)
    b = (a/math.sin(alpha))*math.sin(beta)
    c = (a/math.sin(alpha))*math.sin(gamma)
    if b<0:
      b=b*-1
    if c<0:
      c=c*-1
    perimetro = a+b+c
    print ("Los valores de los angulos: alpha,beta,gamma del triangulo son: ",  alpha,beta,gamma, "respectivamente.\nLos valores de los lados: a,b,c del triangulo son: ",a,b,c,"respectivamente.\nEl perimetro del triangulo es ",perimetro," unidades.")
