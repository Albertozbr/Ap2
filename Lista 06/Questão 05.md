# Questão 05
Crie uma sub-rotina que receba como parâmetros por referência três valores inteiros. A sub-rotina
deverá ordenar de forma crescente os valores. Sintam-se à vontade para usar vetor ou não.
```C
#include <stdio.h>

void ordenar(int *a, int *b, int *c)
{

    int aux;

    // garante que a <= b
    if (*a > *b)
    {
        aux = *a;
        *a = *b;
        *b = aux;
    }

    // garante que a <= c
    if (*a > *c)
    {
        aux = *a;
        *a = *c;
        *c = aux;
    }

    // garante que b <= c
    if (*b > *c)
    {
        aux = *b;
        *b = *c;
        *c = aux;
    }
}

void main()
{
    int x, y, z;

    printf("Informe tres numeros: ");
    scanf("%d %d %d", &x, &y, &z);

    printf("Valores antes da troca: x=%d y=%d z=%d\n", x, y, z);

    ordenar(&x, &y, &z);

    printf("Depois: x=%d y=%d z=%d", x, y, z);
}
