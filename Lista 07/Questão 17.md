# Questão 17
Implemente uma função que receba como parâmetro um array de números reais de tamanho N e
retorne quantos números negativos há nesse array. Essa função deve obedecer ao protótipo:
int negativos(float *vet, int N);

```C
#include <stdio.h>

int negativo(float *v, int n)
{
    int contador = 0;
    for (int i = 0; i < n; i++)
    {
        printf("Informe o %d numero do vetor: ", i + 1);
        scanf("%f", &v[i]);
        if (v[i] < 0)
        {
            contador++;
        }
    }
    return contador;
}

void main()
{
    int n;

    printf("Informe o tamanho do vetor desejado: ");
    scanf("%d", &n);

    float v[n];

    printf("O vetor tem %d numeros negativos", negativo(v, n));
}
