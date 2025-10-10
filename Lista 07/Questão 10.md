# Questão 10
 Escreva um módulo em C que, usando variáveis locais, que declare um vetor com 5 posições e um
ponteiro para essa variável. Usando ponteiro, retorne a soma de todos os elementos do vetor.
```C
#include <stdio.h>

int soma(int v[])
{

    int soma = 0;
    int *p = v; // primeiro elemento do vetor
    for (int i = 0; i < 5; i++)
    {

        soma += *(p + i);
    }
    return soma;
}

void main()
{
    int v[] = {1, 2, 3, 4, 5};

    printf("%d", soma(v));
}
