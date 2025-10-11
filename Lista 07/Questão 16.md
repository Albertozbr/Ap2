# Questão 16
Considere a seguinte declaração:

int A, *B, **C, ***D;

Escreva um programa que leia a variável a e calcule e exiba o dobro, o triplo e o quádruplo desse valor
utilizando apenas os ponteiros B, C e D. O ponteiro B deve ser usada para calcular o dobro, C o triplo e
D o quadruplo.


```C
#include <stdio.h>

void main()
{
    int a;
    int *b;
    int **c;
    int ***d;

    printf("Enter the number for A: ");
    scanf("%d", &a);

    b = &a;
    c = &b;
    d = &c;

    int rb = *b * 2;
    int rc = **c * 3;
    int rd = ***d * 4;

    printf("Valor de A: %d\n Dobro: %d\n Triplo: %d\n Quadruplo: %d", a, rb, rc, rd);
}
