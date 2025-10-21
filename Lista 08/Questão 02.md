# Questão 02
Faça um programa que renomeie o arquivo criado no exercício 1, para MATRICULADOS.TXT.
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
    
    system("pause");
    int resultado = rename("dados.txt", "MATRICULADOS.TXT");
    if (resultado == 0)
    {
        printf("Arquivo renomeado: 'MATRICULADOS.TXT'\n");
    }
    else
    {
        printf("Erro");
    }
    printf("arquivo criado e texto gerado sucesso\n");
}
