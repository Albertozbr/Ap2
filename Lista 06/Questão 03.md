# Questão 03
Foi realizada uma pesquisa com os habitantes de bairro. Crie um programa que define a estrutura
habitante com os dados: nome, idade, sexo, salário e número de filhos. Usando o módulo altera (*
habitante x) altere os dados e do módulo exibe ( * habitante x), para exibir os membros da struct.
```C
#include <stdio.h>
#include <string.h>

typedef struct {
    char nome[50];
    int idade;
    char sexo[9];
    float salario;
    int filhos;
}habitante;

void troca(habitante *x){
    printf("Informe o nome: ");
    scanf(" %49[^\n]", x->nome);

    printf("Informe a idade: ");
    scanf("%d", &x->idade);

    printf("Informe o sexo(masculino ou feminino): ");
    scanf(" %9[^\n]", x->sexo);

    printf("Informe o salario: ");
    scanf("%f", &x->salario);

    printf("Informe quantos filhos: ");
    scanf("%d", &x->filhos);
}

void exibir(habitante *x){
    printf("Nome: %s\n", x->nome);
    printf("Idade: %d\n", x->idade);
    printf("Sexo: %s\n", x->sexo);
    printf("Salario: %.2f\n", x->salario);
    printf("Filhos: %d\n", x->filhos);
}

void main(){
    habitante h;

    troca(&h);
    exibir(&h);
}
´´´
