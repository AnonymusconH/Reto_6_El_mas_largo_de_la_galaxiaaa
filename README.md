# Reto_6_El_mas_largo_de_la_galaxiaaa

## Punto 1

Una función matemática para calcular el volumen y el área superficial.

Para esto nos guiaremos en las formulas para hallar tanto el volumen y área superficial de una esfera y de un cono. Dichas formulas son:

Volumen y área superficial de una esfera:

[![area.jpg](https://i.postimg.cc/Jndg9dLG/area.jpg)](https://postimg.cc/hzTpmshB)



Volumen de un cono:

[![Vco.png](https://i.postimg.cc/K8DmdFsj/Vco.png)](https://postimg.cc/jDCVfVTY)

Área superficial de un cono: El cual esta definido como el área de su base cirular mas su altura. Todo finalizad queda asi:

```
import math 
pi=math.pi

def CalcularVolumen(r1:float,r2:float,h:float)-> float:
    Vol= ((4*(pi*r1**3))/3) + ((pi*r2**2*h)/3)
    return Vol

def CalcularAreaSuperficial(r1:float,r2:float,h:float)-> float:
    Asup= (4*pi*r1**2) + (pi*r2*(math.sqrt((r2**2)+(h**2))))
    return Asup

if __name__ == "__main__":
    r1=float(input("Ingresa el primer radio de la esfera: "))
    r2=float(input("Ingresa ahora el radio del cono: "))
    h=float(input("Ingresa una altura del cono: "))
    volumentotal= CalcularVolumen(r1,r2,h)
    Superficietotal= CalcularAreaSuperficial (r1,r2,h)
print("El volumen total es: "+str(volumentotal))
print("El área superficial total es: "+ str(Superficietotal))

```

## Punto 2 

A grandes rasgos, lo único que tenemos que ensamblar en nuestro código son las operaciones concretas ligadas al perímetro y área del rectángulo más el perimetro de los 2 circulos, asi:

```
import math 
pi=math.pi

def Cal_Area(r:float, b:float, a:float)-> float:
    Área= (b*a)+ (2(pi*r**2))
    return Área

def Cal_Perimetro(r:float, b:float, a:float)-> float:
    Perímetro= ((2*b)+(2*a)) + (2(2*pi*r))
    return Perímetro

if __name__ == "__main__":
  r = float(input("Ingresa el radio de los circulos:"))
  a = float(input("Ingresa una altura para el rectangulo:"))
  b = float(input("Ingresa una base para el rectangulo:"))
  Área_total = Cal_Area(r, a, b)
  Perímetro_total = Cal_Perimetro(r, a, b)

  print("El area total es " + str(Área_total))
  print("El perimetro total es " + str(Perímetro_total))

```

## Punto 3

```

import math 

def Calcular_cantidad_de_carne(N:float, M:float, K:float)-> float:
    Cantidad_carne= (6*N) + (7*M) + (1*K)
    return Cantidad_carne

if __name__ == "__main__":

    N=float(input("Ingresa el número de Gallinas: "))
    M=float(input("Ingresa el número de Gallos: "))
    K=float(input("Ingresa el número de Pollitos: "))

    Carne_en_total= Calcular_cantidad_de_carne (N,M,K)
    print("La cantidad total de carne es: " + str(Carne_en_total))

```

## Punto 4 

Aqui basicamente nos guiaremos bajo la premisa que a la cantidad B de billetes le restaremos el total del precio de las cantidad de unidades que compre el usuario. Un código adecuado sería el siguiente:

```
def Mercado(P:float, M:float, H:float, B:float)-> float:
    Lista_de_compras= B - ((300*P) + (3300*M) + (350* H)) 
    return Lista_de_compras

if __name__ == "__main__":


    P=float(input("Cuantos panes compaste: "))
    print("Te queda en: " + str(300*P))

    M=float(input("Cuantas bolsas de leche compraste: "))
    print("Te queda en: " + str(3300*M))

    H= float (input("Cuanto huevos compraste: "))
    print("Te queda en: " + str(350*H))


    B= float(input("Pagaste en total con: "))

    vueltas= Mercado(P, M, H, B)


    print("Te quedan de vueltas un total de: " + str(vueltas))

```

## Punto 5

Para resolver este punto nos guiaremos de una de las formulas que existen para el interes compuesto:

[![formula-interes-compuesto.png](https://i.postimg.cc/WbCnVQtP/formula-interes-compuesto.png)](https://postimg.cc/2VdvF94H)

Ya empleado en código, nos quedaria asi:

```

def interes_compuest(c:int,i:int,n:int)->int:
    interes_aplicado= (c*((1+i)**n))
    return interes_aplicado

c=int(input("Ingrese un capital inicial: "))
i=int(input("Ingrese una tasa de interes (no sea usurero pai): "))
n=int(input("Ingrese el número de meses que desea dicho interes: "))

interes_final= interes_compuest(c,i,n)

print("El interes compuesto determinado para los parametros que dicto fue: " +str(interes_final))

```

## Punto 6







