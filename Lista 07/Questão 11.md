# Questão 11
Escreva um módulo em C que, usando variáveis locais, declare um vetor de inteiros e um ponteiro
para esse vetor. Depois, peça para o usuário digitar os valores do vetor e use o ponteiro para imprimir
os valores na tela.
```C
#include <stdio.h>

void main()
{
    int v[3];
    int *p;

    for (int i = 0; i < 3; i++)
    {
        printf("Informe o valor do %d vetor: ", i + 1);
        scanf("%d", &v[i]);
    }

    p = v; // faz o ponteiro apontar para o primeiro elemento (v[0])

    printf("Valores dos vetores:\n");
    for (int i = 0; i < 3; i++)
    {
        printf("%d ", *(p + i)); // p + v[0]... p + v[1]...
    }
}
