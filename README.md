# Reto #3

1.Plantear el algoritmo para obtener los números primos hasta n, usando pseudocódigo y diagramas de flujo.

- Pseudocodigo:
    
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


Revise el procedimiento matemático para hallar raíces cuadradas (son divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.

Cree un repositorio en github en donde muestre el desarrollo de la actividad y comparta el enlace por el canal de slack reto_3.
