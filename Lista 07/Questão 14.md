# Questão 14
Crie uma estrutura "Pessoa" com os campos nome, idade e endereço (com os campos rua, número
e cidade). Em seguida, declare um ponteiro para uma variável do tipo Pessoa e imprima os dados da
pessoa na tela.

```C
#include <stdio.h>
#include <string.h>

typedef struct
{
    char rua[50];
    int numero;
    char cidade[50];
} endereco;

typedef struct
{
    char nome[50];
    int idade;
    endereco endereco;
} pessoa;

void main()
{
    pessoa p1;
    pessoa *p;
    p = &p1;
    strcpy(p->nome, "Alberto Santos Entreportes");
    p->idade = 18;
    strcpy(p -> endereco.cidade, "Jatai-go");
    p -> endereco.numero = 54;
    strcpy(p -> endereco.rua, "Tiradentes");
    
    printf("Nome: %s\n Idade: %d\n Cidade: %s\n Numero: %d\n Rua: %s.", p->nome, p->idade, p->endereco.cidade, p->endereco.numero, p->endereco.rua);

}
