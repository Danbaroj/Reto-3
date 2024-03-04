# Reto #3

1. Plantear el algoritmo para obtener los números primos hasta n, usando pseudocódigo y diagramas de flujo.

- Pseudocodigo:

```pseudocode

    n : entero
    Z : entero

    Inicio

        Mientras 2 < n

        Mientras (0 < i <= 10) hacer

            Si n = 2*i  Entonces

                Escribir (" n no es primo ");

            Si no Si n ≠ 2*1 Entonces

                Escribir (" n es primo ");

            Fin Mientras  n < z hacer

                Si z = n*1 Entonces

                    Escribir (" z no es primo");

                Si no Si z ≠ n*1

                    Escribir (" z es primo ")

            Fin Mientras

    Fin



```
    
- Diagrama de flujo:

```mermaid

flowchart TD;
    A(Inicio) -->B[Numero n]
    B -->F[Lista de n > 2]
    F -->Q[ i > 0]
    Q -->J[ i >= 10 ]
    J -->K[z > n]
    K -->C[2*i 
    Multiplicando 2 por todos los valores 
    de i]
    C -->L[Los resultados de 2*i son numeros no primos,
    anotarlos en una lista] 
    L -->D{¿ n = 2*i ?}
    D -->|Si|G[No es primo]
    G -->Ñ[Tomar otro numero n > 2 ]
    Ñ -->D
    D -->|No|H[Es primo ]
    H -->P[n*i
    Tomando todos los resultados de n*i
    añandiendolos a la lista]
    P -->O{¿ z = n*i
    ó
    z = 2*i ?}
    O -->|Si|U[No es primo]
    O -->|No|I[Es primo ]
    U -->Y[Tomar otro numero z > n ]
    Y -->O
    I -->T[z*1
    Tomando todos los resultados de z*i
    añandiendolos a la lista]
    T -->R[Repetir el proceso]
    R -->D
    R -->E(Fin)
```

2. Revise el procedimiento matemático para hallar raíces cuadradas (son divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.

- Pseudocodigo:

```pseudocode

    n : Entero
    x : Entero
    z : Entero

    Inicio
        Dividir n en parejas de digitos;
            Mientras x^2 <= primera pareja de digitos de n Hacer
                Si (Primera pareja de digitos de n - x^2)=0
                    Si (n < 100) entonces
                        escribir ("x es raiz de n")
                    Si no
                        Pasar a la siguiente pareja de n;
                                Mientras z^2 <= la siguiente pareja de digitos n Hacer
                                    Si (Siguiente pareja de digitos de n - 2x*(z*z)=0)
                                        Si (n < 10000) entonces
                                            escribir ("xy son la raiz de n")
                                        Si no
                                            Pasar a la siguiente pareja de n;
                                Repetir ahora x = xz
//¿Como se usa repetir o como puedo hacer repetir una secuencia?
                Si no
                    agrupar el resultado de la resta con la siguiente pareja de digitos del numero n;
                    Mientras z^2 <= la siguiente pareja de digitos n con el resultado de la resta Hacer
                         Si (Siguiente pareja de digitos de n - 2x*(z*z)=0)
                            si (n < 10000) entonces
                                Escribir ("xy son la raiz de n")
                            Si no
                                Pasar a la siguiente pareja de n
                           
                    Repetir ahora x=xz
            Fin Mientras
        Fin
```

- Diagrama de flujo

```mermaid
flowchart TD;
    A(Inicio) -->B[Numero n]
    B -->C[Dividir el numero n en parejas de digitos]
    C -->D[Encontrar un numero x,
    donde 
    x^2 <= primer grupo de digitos de n]
    D -->E[ Primer pareja de digitos - x^2 ]
    E -->F{¿Su resultado es 0?}
    F -->|Si|I{¿Su numero n era un numero
     con dos digitos?}
    I -->|Si|J[x es el la raiz de n]
    I -->|No|K[Pase a la siguiente pareja]
    K -->L[Duplicar x]
    F -->|No|G[Agrupar el resultado de la resta
    con la siguiente pareja de digitos]
    G -->H[Duplicar x]
    H -->M[Encontrar un z^2 que al multiplicarlo con
    el doble de x sea <= a la pareja agrupada con el
    resultado de las resta]
    M -->N[Restar los digitos agrupados con 2x*z^2]
    L -->Ñ[Encontrar un z^2 que al multiplicarlo con
    el doble de x sea <= a la siguiente pareja que se 
    encontraba agrupada]
    Ñ -->N
    N -->O{¿La resta es 0?}
    O -->|Si|P{¿Su numero n era de 4 digitos?}
    O -->|No|S[Agrupar el resultado de la resta con
    la siguiente pareja de digitos]
    S -->U[Repita pero ahora x = x y z unidos como digitos]
    U -->H
    P -->|Si|Q[El numero x y z,unidos como digitos
    son la raiz de n]
    P -->|No|R[Pase a la siguiente pareja]
    R -->T[Repita, pero ahora x = x y z unidos como digitos]
    T -->L
    Q -->V(Fin)
```
