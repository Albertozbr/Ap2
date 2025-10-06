# Questão 06: Construa um programa que leia um vetor de números reais e que possui 5 posições. O programa principal fará as seguintes chamadas de funções:
## a)
int soma(float *v, int tamanho) – Retorna o somatório dos valores do vetor;

```C
#include <stdio.h>
#include <math.h>

float soma(float *v, int tamanho)
{
    int total = 0;

    for (int i = 0; i < tamanho; i++)
    {
        total += v[i];
    }
    return total;
}
´´´
## b)

```C
float media(float soma, int tamanho)
{
    return soma / tamanho;
}

float desvio(float *v, float media, int tamanho)
{
    float somatorio = 0;

    for (int i = 0; i < tamanho; i++)
    {
        somatorio += pow(v[i] - media, 2);
    }
    return sqrt(somatorio / tamanho);
}

void substitui(float *v, int tamanho)
{
    for (int i = 0; i < tamanho; i++)
    {
        if (v[i] < 0)
        {
            v[i] = 0;
        }
    }
}

void main(){
    float vetor[5];
    int tamanho = 5;

    for(int i = 0; i < tamanho; i++){
        printf("Informe o valor do %d vetor:\n", i + 1);
        scanf("%f", &vetor[i]);
    }
    float total = soma(vetor, tamanho);
    float med = media(total, tamanho);
    float desv = desvio(vetor, med, tamanho);
    substitui(vetor, tamanho);

    printf("Soma: %.2f\n", total);
    printf("Média: %.2f\n", med);
    printf("Desvio: %.2f\n", desv);
    printf("Substituido: \n");
    for(int i = 0; i < tamanho; i++){
        printf("%.2f", vetor[i]);
    }
}
