# Questão 12+1
Crie uma estrutura "Aluno" com os campos nome, idade e nota. Em seguida, declare um ponteiro
para uma variável da estrutura tipo Aluno. Usando o ponteiro, preencha os campos da estrutura com
dados informados pelo usuário e imprima os dados do aluno na tela.

```C
#include <stdio.h>
#include <string.h>

typedef struct
{
    char nome[50];
    int idade;
    float nota;
} aluno;

void main()
{
    aluno a;
    aluno *p;
    p = &a;

    printf("Informe o nome do aluno:\n");
    fgets(p->nome, 50, stdin);
    p->nome[strcspn(p->nome, "\n")] = '\0';

    printf("Informe a idade:\n");
    scanf("%d", &p->idade);
    getchar();

    printf("Informe a nota:\n");
    scanf("%f", &p->nota);
    getchar();

    printf("Nome: %s\n Idade: %d\n Nota: %.2f\n", p->nome, p->idade, p->nota);
}
