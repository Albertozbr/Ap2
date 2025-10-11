# Questão 15
 Crie uma função que receba como parâmetro um array e o imprima. Não utilize índices para
percorrer o array, apenas aritmética de ponteiros. 
```C
#include <stdio.h>

void array(int n, int *p)
{

    for (int i = 0; i < n; i++)
    {
        printf("[%d]", *(p + i));
    }
}

void main()
{
    int n;

    printf("enter the size of your vector: ");
    scanf("%d", &n);
    int v[n];

    for (int i = 0; i < n; i++)
    {
        printf("Enter the numbers your vector: ");
        scanf("%d", &v[i]);
    }

    array(n, v);
}
