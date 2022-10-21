# JavaScript

Algoritmos em JavaScript são chamados de functions. Pra mostrar o que está dentro do algoritmo, são utilizadas chaves {} no começo e no final do que está escrito.

## Operações com números

</br>Operador de soma: +
</br>Operador de subtração: -
</br>Operador de multiplicação: *
</br>Operador de divisão: /
</br>Operador de resto: %
</br>Operador de igual: ==
</br>Operador de maior: >
</br>Operador de maior ou igual: >=
</br>Operador de menor: <
</br>Operador de menor ou igual: <=
</br>Operador de diferente: !=
</br>Operador de e (and): &&
</br>Operador de ou (or): ||
</br>Operador de inverter booleano (not): !
</br>Operador de repetição (enquanto): while
</br>Operador de repetição (para): for
</br>Operador de array: [ ]
</br>Resultado da função: return
</br>Definir uma variável: let
</br>Atribuição de variáveis: =
</br>Executar função: nome da função(valor1, valor2)
</br>Finalizamos as linhas com ;
</br>Fazer comentários: //
</br>Números decimais são utilizados com ponto: 2.5
</br>Contador = contador + 1  --->  contador++
</br>Frase = frase + “blablabla” ---->  Frase += “blablabla”
</br>Contador: i

### Exemplo

</br>function somar (num1, num2) {
</br>  let resultado = num1 + num2;
</br>  return resultado;
</br>}

</br> somar(2, 10);

Posso escrever mais de uma operação aritmética na própria linha.

### Exemplo

</br>function media(num1, num2) {
</br> return (num1 + num2) / 2
</br>}


## Operações com texto

O texto no JavaScript é colocado entre aspas “”

### Exemplo

</br>function apresentar (nome) {
</br> let texto = “Olá” + nome;
</br> return texto;
</br>}

</br>apresentar(“Maria”);

O resultado dessa função será: Olá Maria

### Exemplo de cálculo da média com resultado em texto

</br>function calcularMedia (nota1, nota2, nota3) {
</br> let media = ((nota1 * 3) + (nota2 * 3) + (nota3* 3)) / 10
</br> let resultado = “Sua média é:” + media
</br> return resultado
</br>}

</br>calcularMedia (5, 5, 10);

O resultado dessa função será: Sua média é: 7

## Condicionais

Utilizamos a construção if else. 

### Exemplo

</br>function calcularMedia (nota1, nota2, nota3) {
</br> let media = ((nota1 * 3) + (nota2 * 3) + (nota3* 3)) / 10;
</br> if (media < 7) {
</br>  return “Reprovado”;
</br> } else {
</br>  return “Aprovado”;
</br> }
</br>}

Para criar uma segunda condição, utilizamos o else if.

### Exemplo 

</br>function calcularMedia (nota1, nota2, nota3) {
</br> let media = ((nota1 * 3) + (nota2 * 3) + (nota3* 3)) / 10;
</br> if (media < 5) {
</br>  return “Reprovado”;
</br> } else if (media < 7)
</br>  return “Prova Final”;
</br> } else {
</br>  return “Aprovado”;
</br> }
</br>}


Valores booleanos são valores que retornam true ou false. Colocar valores booleanos dentro de variáveis deixa o código mais legível.

### Exemplo

</br>function calcularMedia (nota1, nota2, nota3) {
</br> let media = ((nota1 * 3) + (nota2 * 3) + (nota3* 3)) / 10;
</br>  let reprovado = (media < 7)
</br>  if reprovado {
</br>  // nunca vai executar
</br> } 
</br>}

## Condicionais e Operadores Lógicos

Para que duas condições sejam satisfeitas ao mesmo tempo, utilizamos o operador &&, que significa and. 

### Exemplo

</br>function aprovadoOuReprovado (nota1, nota2, nota3, faltas) {
</br> let media = ((nota1 * 3) + (nota2 * 3) + (nota3* 3)) / 10;
</br> let aprovadoMedia = (media >= 7)
</br> let aprovadoPresenca = (faltas < 10)
</br> if (aprovadoMedia && aprovadoPresenca) {
</br>   return “Aprovado”;
</br> } else {
</br>   return “Reprovado”;
</br> }
</br>}

Para que pelo menos uma das condições seja satisfeita, utilizamos o operador ||, que significa or. Já para inverter uma condição (mudar de true para false), utilizamos o operador !, que significa not.

### Exemplo

if(!aprovadoVestibular)

Neste exemplo, estamos buscando as pessoas que não satisfazem a condição, ou seja, não foram aprovadas no vestibular.


## Loops

Os loops fazem com que um código possa ser repetido várias vezes de maneira automática. Para isso, utilizamos o operador while (enquanto). Para definir quantas vezes o loop deve ser repetido, precisamos primeiro definir um contador partindo do 0 e então determinar que ele cresça a cada repetição. Dessa maneira, o loop só será rodado enquanto satisfizer a condição (no exemplo, até o número 99).

### Exemplo

</br>let contador = 0
</br>while (contador < 100) {
</br> contador = contador + 1;
</br>}

No próximo exemplo, a frase será concatenada 100 vezes.

### Exemplo


</br>function umbridge() {
</br>  let contador = 0
</br>  let frase = “”
</br>  while (contador< 100) {
</br>     frase = frase + “Não devo contar mentiras”;
</br>     contador = contador + 1;
</br>   }
</br>  return frase;
</br>} 
</br>umbridge()

A frase contador = contador + 1 se tornou tão comum que foi criada uma maneira de simplificar esta escrita: contador++. Da mesma maneira, para fazer o mesmo com frases, utilizamos a escrita +=.

### Exemplo

</br>frase = frase + “Não devo contar mentiras” ------> frase += “Não devo contar mentiras”
 
Para simplificar a escrita ainda mais, podemos utilizar o operador for (para).

### Exemplo

for(let contador = 0; contador < 100; contador++)

## Arrays

Um array nada mais é do que uma lista de informações. Para criar um, utilizamos os operadores [ ] (colchetes) e separamos os valores por vírgulas. Para selecionar um determinado valor do array, utilizamos nome[index], onde index é a posição do valor na lista. É importante lembrar que os arrays sempre começam na posição 0. Portanto, para selecionar o primeiro item, utilizamos nome[0]. Para saber o tamanho de um array, utilizamos o operador nome.length. Convencionou-se também utilizar a variável i para nomear o contador.

### Exemplo

</br>function teste() {
</br>  let alunos = [“Ana”, “Bia”, “Carlos”]
</br>  let texto = “”

</br>  for (let i = 0; i < alunos.length; i++) {
</br>    texto = texto + alunos[i];
</br>    }

</br>  return texto;
}

</br>teste();

No exemplo acima, o nome dos alunos será concatenado em uma string.
