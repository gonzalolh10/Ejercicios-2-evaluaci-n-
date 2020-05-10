# Ejercicios-2-evaluaci-n-
Programación
#include <stdio.h>

int main()
{
    int hora;
    int minutos;    
    int segundos;

    printf("Por favor, introduzca la hora: ");
    scanf("%d", &hora);
    printf("\n");

    printf("Por favor, introduzca los minutos: ");
    scanf("%d", &minutos);
    printf("\n");

    printf("Por favor, introduzca los segundos: ");
    scanf("%d", &segundos);
    printf("\n");

    segundos = hora*3600 + minutos*60 + segundos;
    printf("Los segundos totales son : %d", segundos);
    
    return 0;
}
#include <stdio.h>

int main()
{
    int anyo;
        printf("Por favor, introduzca el año: ");
        scanf("%d", &anyo);
        printf("\n");
        
    if(anyo % 4 == 0 && !(anyo%100==0 && !anyo%400!=0)){
        printf("El año es bisiesto");
    }
    
    else{
        printf("El año no es bisiesto");
    }
    

    return 0;
}
#include <stdio.h>

int main()
{
    int numero1;
    
    printf("Si quieres saber lo que tienes que hacer en cada color de los semáforos, introduzca uno de los números siguientes. 1 es el rojo, 2 es el ámbar, 3 es el verde:");
    scanf("%d", &numero1);
    printf("\n");
    switch (numero1){
        case 1: 
            printf("No debo pasar");
            break;
        case 2:
            printf("Puedo pasar con cuidado");
            break;
        case 3: 
            printf("Puedo pasar");
            break;
    }
    
    
    

    return 0;
}
#include <stdio.h>

int main()
{
    int hora;
    int minutos;    
    int segundos;

    printf("Por favor, introduzca la hora: ");
    scanf("%d", &hora);
    printf("\n");

    printf("Por favor, introduzca los minutos: ");
    scanf("%d", &minutos);
    printf("\n");

    printf("Por favor, introduzca los segundos: ");
    scanf("%d", &segundos);
    printf("\n");
     
    if(hora < 24 && minutos < 60 && segundos < 60) {
        printf("La hora es correcta");
    }
     else{
        printf("La hora que ha introducido no es correcta\n");
    }
      return 0;
}
#include <stdio.h>

int main()
{
    int numero1;
    int numero2;
    printf("Por favor, introduzca el primer número: ");
    scanf("%d", &numero1);
    printf("\n");
    printf("Por favor,introduzca el segundo número: ");
    scanf("%d", &numero2);
    if (numero2<numero1) {
        int aux = numero1;
        numero1 = numero2;
        numero2 = aux;
    }
    int i=numero1;
    int suma = 0;
    while (i <= numero2){
        suma = i + suma;
        i  = i + 1;  
    }
   
    printf("El total es: %d", suma);

    return 0;
}
#include <stdio.h>

int main()
{
    int i, numero1;
    printf("Por favor, introduzca el primer número: ");
    scanf("%d", &numero1);
    printf("\n");
    for (i=1 ; i<=numero1; i++){
        printf("El cuadrado de %d es: %d\n", i , i*i);
    } 
   
    return 0;
}
#include <stdio.h>

int main()
{
    int numero1;
    
    printf("Por favor, introduzca el primer número: ");
    scanf("%d", &numero1);
   
    int i = numero1;
    while (i >= 1){
        i  = i / 2 ;
        printf("El resultado es: %d\n", i);
     
    }
   
   

    return 0;
}
#include <stdio.h>

int main()
{
    int suma(int numero1, int numero2){
        return numero1+numero2;
    }
    int resta(int numero1, int numero2){
        return numero1-numero2;
    }
    int multiplicacion(int numero1,int numero2){
        return numero1*numero2;
    }
    int division(int numero1, int numero2){
        return numero1/numero2;
    }
    int numero1;
    int numero2;
    int operacion;
    int resultado = 0;
    
            printf("Por favor, introduzca el primer número: ");
            scanf("%d", &numero1);
            printf("\n");
        
            printf("Por favor, introduzca el segundo número: ");
            scanf("%d", &numero2);
            printf("\n");
            
            printf("Por favor, introduzca la operación que desee realizar. 1 es la suma, 2 es la resta, 3 es la multiplicación y 4 es la división: ");
            scanf("%d", &operacion);
            printf("\n");
        
    switch (operacion){
        case 1:
            resultado = suma(numero1, numero2);
            break;
        case 2:
            resultado = resta(numero1, numero2); 
            break;
        case 3: 
            resultado =  multiplicacion(numero1,numero2);
            break;
        case 4:
            resultado =  division(numero1, numero2);
    }
        
            printf("El resultado es:%d" ,resultado);
    
    
    

 return 0;
}
#include <stdio.h>

struct Persona{
    char nombre[10];
    int edad;
};

int main()
{
    struct Persona personas [3];
    
    printf("Por favor, introduzca el nombre de la primera persona: ");
    scanf("%s", personas[0].nombre);
    printf("\n");
    printf("Por favor, introduzca la edad de la primera persona: ");
    scanf("%d", &personas[0].edad);
    printf("\n");
    printf("Por favor, introduzca el nombre de la segunda persona: ");
    scanf("%s", personas[1].nombre);
    printf("\n");
    printf("Por favor, introduzca la edad de la segunda persona: ");
    scanf("%d", &personas[1].edad);
    printf("\n");
    printf("Por favor, introduzca el nombre de la tercera persona: ");
    scanf("%s", personas[2].nombre);
    printf("\n");
    printf("Por favor, introduzca la edad de la tercera persona: ");
    scanf("%d", &personas[2].edad);
    printf("\n");

    int i = 0;
    while (i<=2){
        if(personas[i].edad>=18){
            printf("Las personas que son mayores de edad son: %s\n", personas[i].nombre);
        }
        i++;
    }
    
    
    
    
    
    return 0;
}
#include <stdio.h>
void intercambio (int * numero1, int * numero2){
    int aux = *numero1;
    *numero1 = *numero2;
    *numero2 = aux;
}
int main()
{
    int numero1;
    int numero2;
    printf("Por favor, introduzca el primer numero: ");
    scanf("\n %d", &numero1);
    printf("Por favor, introduzca el segundo numero: ");
    scanf("\n %d", &numero2);
    
    intercambio(&numero1, &numero2);
    
    printf("El intercambio de los numeros son : El numero 1 sería %d El numero 2 sería %d", numero1, numero2);
    

    return 0;
}
