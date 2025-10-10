# Questão 08
Escreva um módulo em C que, usando variáveis locais, declare uma variável inteira e um ponteiro
para essa variável, e depois altere o valor da variável através do ponteiro.

```C
#include <stdio.h>

void main()
{
    int a = 5;
    int *p;
    int c;

    p = &a;
    c = *p;

    printf("%d\n", a);
    *p = 10;

    printf("%d", a);
}



