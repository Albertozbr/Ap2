# QUESTÃO 01
## a)
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

## b)
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
<img width="440" height="280" alt="image" src="https://github.com/user-attachments/assets/6971c5a7-e604-4057-9532-fa2ba1c33111" />
´´´
