# Questão 01
 O que as linhas abaixo fazem? Escreva como um comentário, assim como na primeira linha
int i=99, j; //Declara duas variáveis do tipo inteiro: i, j, sendo que o valor de i=99.
int *p; 
p = &i;
j = *p + 300;

int *p; //Declarar um ponteiro "p" do tipo inteiro
p = &i; // p está apontando para o endereço de i
j = *p + 300; // J está recebendo o conteudo de i(99) + um valor de 300

# Questão 02
Faça o teste de mesa do exercício anterior, não deixe de colocar um campo para indicar o endereço
de memória.

Teste de mesa

<img width="435" height="145" alt="image" src="https://github.com/user-attachments/assets/37167c50-b0e5-4073-9cb5-a8913850ee05" />



Explicação de *p e &i (fiquei em duvida)

&i: representa o endereço de memória que tem a variavel i
*p mostra o conteudo da variavel que p aponta, nesse caso, o conteudo de i = 99

Então *p = 99 já que ele é o conteudo que a variavel p aponta e ela está apontando para i e a variavel i vale 99.





