# Questão 01
Faça um programa que crie um arquivo TEXTO em disco, com o nome “dados.txt” e escreva
neste arquivo em disco uma contagem de 20 em 20, que vá de 0 até 1000, com um número em
cada linha.
```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

void main()
{
    FILE *f;
    f = fopen("dados.txt", "w");
    if (f == NULL)
    {
        printf("Arquivo não existe\n");
        system("pause");
        exit(1);
    }

    int soma = 0;
    for (int i = 0; i < 51; i++)
    {
        fprintf(f, "%d\n", soma);

        soma += 20;
    }

    fclose(f);
    printf("arquivo criado e texto gerado sucesso\n");
    system("pause");
}
