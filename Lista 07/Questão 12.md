# Questão 12
Escreva um módulo em C que, usando variáveis locais, declare um ponteiro para uma estrutura que
represente um aluno (com nome, idade e média). Depois, crie uma variável desse tipo e use o ponteiro
para preencher os dados da estrutura. Em seguida, imprima os dados do aluno na tela.
```C
#include <stdio.h>
#include <string.h>

typedef struct
{
    char nome[50];
    int idade;
    float media;bbhs
} aluno;

void main()
{
    aluno *p;
    aluno a;
    p = &a;
    p->idade = 18;
    strcpy(p->nome, "alberto santos");
    p->media = 6;

    printf("Idade: %d, Nome: %s, Media: %.2f", p->idade, p->nome, p->media);
}
