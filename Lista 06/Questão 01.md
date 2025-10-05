# QUESTÃO 01
## a)Crie um programa para testar as funções a seguir:
• Uma função que receba dois números a e b, em seguida, faça a troca destes dois números. Dica:
a e b devem ser passados por referência.

```C

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int troca(int x, int y){
    int aux;

    printf("%d %d\n", a, b);

    c = a;
    a = b;
    b = c;

    printf("%d %d", a, b);
}

void main(){

    int a, b, aux;
    printf("Informe dois numeros 'a' e 'b': \n");
    scanf("%d %d", &a, &b);

    troca(aux);
}
```

## b)• Uma função que receba dois números a e b, em seguida, decremente o primeiro e incremente o
segundo. Dica: a e b devem ser passados por referência.

```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
void troca(int *a, int *b)
{
    (*a)--;
    (*b)++;
}
void main()
{
    int a, b;
    printf("Informe dois numeros 'a' e 'b': \n");
    scanf("%d %d", &a, &b);
    printf("%d %d\n", a, b, &a, &b);
    troca(&a, &b);
    printf("%d %d", a, b, &a, &b);
}
´´´
