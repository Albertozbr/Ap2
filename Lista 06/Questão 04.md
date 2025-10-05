# Questão 04
Crie uma sub-rotina que receba como parâmetros um vetor, *xmin e a quantidade de elementos do
vetor (use o comando sizeof( ) dentro do módulo principal). A rotina deverá calcular o menor elemento
do vetor e também deverá fazer a multiplicação de cada elemento com o menor elemento do vetor.
```C
#include <stdio.h>
#include <string.h>

void sub_rotina(int v[], int n, int *xmin)
{

    if (n <= 0)
    {
        *xmin = 0;
        return;
    }
    int min = v[0];
    for (int i = 1; i < n; i++)
    {
        if (v[i] < min)
        {
            min = v[i];
        }
    }
    *xmin = min; // devolve o menor valor para o ponteiro

    for (int i = 0; i < n; i++)
    {
        v[i] *= min;
    }
}

void main()
{

    int v[] = {5, 10, 45, 2, -2, 7};

    int n = sizeof(v) / sizeof(0); // calcular a quantidade de elementos

    int xmin; // função guardar o menor valor

    printf("Vetor original: ");
    for (int i = 0; i < n; i++)
    {
        printf("%d,", v[i]);
    }
    printf("\n");
    printf("Quantidade de elementos do vetor: %d\n", n);

    sub_rotina(v, n, &xmin);

    printf("Menor elemento do vetor: %d\n", xmin);

    printf("Vetor multiplicado: ");
    for (int i = 0; i < n; i++)
    {
        printf("%d,", v[i]);
    }
    printf("\n");
}
