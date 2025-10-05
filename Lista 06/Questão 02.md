# Questão 02
Faça um programa que receba uma frase no módulo principal. Elabore um módulo que receba a frase
e uma determinada vogal, ao final, mostre a quantidade de vezes que a vogal apareceu na frase. Fazer
tratamento de erro para evitar que leia consoante
```C
#include <stdio.h>
#include <string.h>
#include <ctype.h>

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
    frase[strcspn(frase, "\n")] = '\0';
    
    do{
        printf("Informe uma vogal:\n");
        scanf(" %c", &vogal);

        vogal = tolower(vogal);
        
        if(vogal != 'a' && vogal != 'e' && vogal != 'i' && vogal != 'o' && vogal != 'u'){
            printf("Letra digitada = consoante, invalida!\n");   
        }
    }while(vogal != 'a' && vogal != 'e' && vogal != 'i' && vogal != 'o' && vogal != 'u');


    tamanho = strlen(frase);

    troca(frase, vogal, tamanho);
}
´´´
