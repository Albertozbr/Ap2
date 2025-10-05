# Questão 02
```C
#include <stdio.h>
#include <string.h>

void troca(char *frase, char vogal, int tamanho)
{

    int contador = 0;
    for (int i = 0; i < tamanho; i++)
    {
        if (frase[i] == vogal)
        {
            contador++;
        }
    }
    printf("%d", contador);
}

void main()
{
    int tamanho;
    char frase[50];
    char vogal;
    int contador = 0;

    printf("Informe uma frase:\n");
    fgets(frase, 50, stdin);
    frase[strcspn(frase, "\n")] = '0';

    printf("Informe uma vogal:\n");
    scanf("%c", &vogal);

    tamanho = strlen(frase);

    troca(frase, vogal, tamanho);
}
´´´
