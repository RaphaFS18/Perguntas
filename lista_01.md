
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
X a) A saída será undefined seguido de erro  
R:A resposta é que vai ser undefined porque ele tem uma variavel mas nao foi atribuido nenhum valor para ela, e depois vai ser erro pois por mais que tenha a variavel, ela nao foi inicializada

b) A saída será 5 seguido de 10 

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log



**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

X a) Substituir if (a || b === 0) por if (a === 0 || b === 0)
R:O motivo de estar dando erro é porque o codigo esta vendo se apenas o B é igual a zero pois ai da erro. Para corrigir, precisa colocar parenteses no A e no B para verem individualemnte se os valores sao validos ou nao.

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)


______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

X b) O código imprime 200.
R:O codigo vai imprimir 200 pois como nao tem break depois do "case eletronico"ele vai continuar executando o codigo e nao vai imprimir 100. Como o proximo é "case vestuario" como possui o break, entao ele vai imprimir o valor de 200, que é o valor desse case. Ele nao vai executar o proximo codigo pois ele possui o "Break"que impossibilita de continuar o coidgo

c) O código imprime 50.

d) O código gera um erro.


______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

X d) 24
R: Ele usa 3 metodos para calcular o valor. o primeiro é o "Map"onde é vai multiplicar todos os valores por 2, ficando 2, 4, 6, 8, 10. Depois ele usa o "Filter, onde
vai filtrar todos os valores maiores que 5, que sao 6, 8, 10. Depois, ele usa "Reduce"para somar todos os valores, que vai dar 24(6+8+10=24)


______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

X c) ["banana", "abacaxi", "manga", "laranja"]
R:O uso do "Splice"adiciona ou remove algo do array. Quando ele disse (1, 2) significou que ele queria remover dois indices a partir da posicao 1, e substituir eles por
abacaxi, manga. Como os indices comecam a partir do 0, o 1 indice é a maca, entao vai remover a maca, 1 indice e a uva, 2 indice, os substituindo por abacaxi e manga.

d) ["banana", "maçã", "uva", "abacaxi", "manga"]


______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


X a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.
R:As duas sao verdadeiras uma vez que a herança permite que a subclasse herde métodos e propriedades de uma superclasse, evitando repeticao de codigo. A palavra 
"Extends"significa que uma classe foi herdada a partir de outra e por isso justifica a primeira afirmacao porque permite que as classes sejam herdadas.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.


______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

X a) I e II são verdadeiras.
R: Como esta usando extends para herdar uma classe, siginifica que nao só é permitido herdar como vai herdar da classe Pessoa. Como ele usa um "Super"classe, significa
que ela vai se sobrepor a classe anterior pois tem esse super, sendo assim verdadeiro, e o codigo vai sim funcionar pois poce herdar uma classe

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.



**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

X b) A asserção é verdadeira e a razão é falsa.
R: O polimorfismo permite que diferentes classes coloquem o mesmo metodos mas de forma diferente, entao significa que os objetos podem ter varias frormas, entao esta certo. A razao é falsa pois nao pode ter uma sobrecarga, uma vez que so a ultima vai ser considerada, entao é falsa

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.



Desconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, apl# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

ERRADO
```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

CERTO
```javascript
function somaArray(numeros) {
    var soma = 0; //Precisa criar uma variavel pois nao tinha
    for (var i = 0; i < numeros.length; i++) {    //Precisa colocar variavel e tambern nao pode ter size, precisa ser lenght
        soma += 2 * numeros[i];   //Vai salvar o dobro do valor
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));   //Fica 2x1 + 2x2 + 2x3 + 2x4 = 20
```



10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calculaicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

R: O produto é uma classe geral, tipo um molde para qualquer coisa que pode ser vendida, como cadeiras, mesas, celular. Ela já vem com um desconto de 10%.

Ja o ivro, é uma versão mais específica de Produto, mas como tem descontos diferentes, a gente precisa mudar essa regra. Então, dentro da classe Livro, a gente cria um novo método calcularDesconto(), que dá 20% em vez de 10%.

```javascript
// Classe base Produto
class Produto {
  constructor(nome, preco) {
    this.nome = nome;
    this.preco = preco;
  }

  calcularDesconto() {
    return this.preco * 0.9; // 10% de desconto pois essa classe, todos os produtos dentro dela tem 10 % de descoonto. Faz sempre o numero restante para o chegar a 100% e multiplica pois ai am perca do valor é do desconto 
  }
}

// Classe Livro que herda de Produto
class Livro extends Produto {
  calcularDesconto() {
    return this.preco * 0.8; // 20% de desconto, agora pelo livro estar dentro dessa classe, entao ele vai mudar o desconto para 20%
  }
}

// Criando objetos
const produto = new Produto("Cadeira", 200);
console.log(`Preço com desconto: R$ ${produto.calcularDesconto()}`); //Ai em seguida, pela cadeira estando na classe produto, ela vai ter um desonto de 10%

const livro = new Livro("JavaScript Básico", 150);
console.log(`Preço do livro com desconto: R$ ${livro.calcularDesconto()}`);  //Livro por estar dentro das classes, vai ter um desconto de 20% nele
