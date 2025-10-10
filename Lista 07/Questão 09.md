# Questão 09
Escreva um módulo em C que, usando variáveis locais, declare uma string e um ponteiro para essa
variável. Usando ponteiro, altere a string para sua versão em letras maiúsculas.

```C
#include <stdio.h>
#include <ctype.h>

void main()
{
    char str[] = "algoritmo e programacao";
    char *p;

    p = str; // aponta para o inicio da string

    printf("String normal: %s\n", str);

    while (*p != '\0')
    {
        *p = toupper(*p); // troca para maiusculo
        p++;              // avança para o proximo caracter
    }
    printf("String em maiuscula: %s", str);
}
