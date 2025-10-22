# Questão 04
Faça um programa para incluir alunos no arquivo criado no Exercício 3, lembrando que não
podem existir dois alunos com o mesmo número de matrícula.
```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct
{
    int matricula;
    char nome[50];
    char curso[50];
    float n1, n2;
} aluno;

void main()
{
    FILE *f;
    f = fopen("ALUNO.DAT", "a");
    if (f == NULL)
    {
        printf("Erro, arquivo nao encontrado\n");
        system("pause");
        exit(1);
    }
    int qtd;

    printf("Informe quantos alunos deseja incluir: ");
    scanf("%d", &qtd);
    getchar();
    aluno a;

    for (int i = 0; i < qtd; i++)
    {
        printf("Informe a matricula do %d aluno: ", i + 1);
        scanf("%d", &a.matricula);
        getchar();

        printf("Informe o nome do %d aluno: ", i + 1);
        fgets(a.nome, 50, stdin);
        a.nome[strcspn(a.nome, "\n")] = '\0';

        printf("Informe o curso do %i aluno: ", i + 1);
        fgets(a.curso, 50, stdin);
        a.curso[strcspn(a.curso, "\n")] = '\0';

        printf("Informe a primeira e a segunda nota do aluno %d: ", i + 1);
        scanf("%f %f", &a.n1, &a.n2);
        getchar();

        int duplicada = 0;
        int mat;
        char nome[50], curso[50];
        float n1, n2;

        rewind(f); // volta para o inicio do arquivo, para poder ler tudo novamente pois quando abre o arquivo já vai para o final.

        while (fscanf(f, "%d %49s %49s %f %f", &mat, nome, curso, n1, n2) == 5)
        { // irá ler linha por linha do arquivo e salvar
            if (a.matricula == mat)
            {
                printf("já existe alguma aluno com essa matricula\n");
                duplicada = 1;
                break;
            }
        }
        if (!duplicada)
        {

            fprintf(f, "Matricula: %d\n Nome: %s\n Curso:%s\n Nota 1:%.2f/Nota 2:%.2f\n", a.matricula, a.nome, a.curso, a.n1, a.n2);
        }
    }
    fclose(f);
    system("pause");
}
