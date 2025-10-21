# Questão 03
Faça um programa para criar um arquivo chamado ALUNOS.DAT, no qual cada registro será
composto pelos seguintes campos: matrícula, nome, curso, nota1 e nota2.
```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct{
    int matricula;
    char nome[50];
    char curso[50];
    float n1, n2;
}aluno;

void main(){
    FILE *f;
    f = fopen("ALUNO.DATA", "w");
    if(f == NULL){
        printf("Erro, arquivo nao encontrado\n");
        system("pause");
        exit(1);
    }
    aluno a;

    for(int i = 0; i < 2; i++){
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

        fprintf(f, "Matricula: %d\n Nome: %s\n Curso:%s\n Nota 1:%.2f/Nota 2:%.2f\n", a.matricula, a.nome, a.curso, a.n1, a.n2);
    }
    fclose(f);
    system("pause");

}
