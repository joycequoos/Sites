[← Voltar para Sites / Desenvolvimento Web](https://github.com/joycequoos/Sites/blob/main/README.md)

# Exercícios JavaScript — Segunda Parte

Continuação dos [exercícios da Primeira Parte](https://github.com/joycequoos/Sites/tree/main/Exercicios_JavaScript_PrimeiraParte), agora avançando para funções nativas (built-in), estruturas condicionais, laços de repetição, funções próprias, escopo, closures, recursão, arrays e objetos.

## Sumário

**Funções nativas (built-in)**
- [17 — Estrutura de uma Função](#17--estrutura-de-uma-função)
- [18 — prompt()](#18--prompt)
- [19 — alert()](#19--alert)
- [20 — Objeto Math](#20--objeto-math)

**Estruturas condicionais**
- [21 — if](#21--if)
- [22 — if / else](#22--if--else)
- [23 — if / else if / else](#23--if--else-if--else)
- [24 — Condicionais Aninhadas (if dentro de if)](#24--condicionais-aninhadas-if-dentro-de-if)
- [31 — switch](#31--switch)

**Laços de repetição**
- [25 — while](#25--while)
- [26 — do...while](#26--dowhile)
- [27 — for](#27--for)
- [28 — break](#28--break)
- [29 — continue](#29--continue)
- [30 — Incrementação (`+=` e `++`)](#30--incrementação--e-)

**Funções**
- [32 — Definindo Funções](#32--definindo-funções)
- [33 — Mais Exemplos de Função](#33--mais-exemplos-de-função)
- [34 — Escopo de Função](#34--escopo-de-função)
- [35 — Arrow Function](#35--arrow-function)
- [36 — Argumentos Opcionais](#36--argumentos-opcionais)
- [37 — Argumentos Default](#37--argumentos-default)
- [38 — Closure](#38--closure)
- [39 — Recursão](#39--recursão)

**Estruturas de dados**
- [40 — Array](#40--array)
- [41 — Métodos e Objetos](#41--métodos-e-objetos)

---

## 17 — Estrutura de uma Função

[Ver pasta](./17_estruturaFuncoes)

Introdução ao conceito de chamar (invocar) uma função passando argumentos, antes mesmo de aprender a criá-la — mostrando a sintaxe básica de invocação.

```javascript
nomeDaFuncao(a, b);
```

---

## 18 — prompt()

[Ver pasta](./18_built-in_prompt)

Uso da função nativa `prompt()`, que abre uma caixa de diálogo no navegador para capturar uma entrada de texto do usuário e armazená-la em uma variável.

```javascript
let cor = prompt('Qual a sua cor favorita?');
console.log(cor);
```

---

## 19 — alert()

[Ver pasta](./19_Built-in-alert)

Uso da função nativa `alert()` para exibir uma mensagem em uma janela pop-up, combinada com interpolação de variável em template string.

```javascript
let nome = 'Josi';
alert(`Meu nome é ${nome}`);
```

---

## 20 — Objeto Math

[Ver pasta](./20_Built-in_math)

Métodos nativos do objeto `Math` para operações matemáticas comuns: `Math.max()` (maior valor), `Math.min()` (menor valor), `Math.round()` (arredondamento) e `Math.ceil()` (arredondamento para cima).

```javascript
let number = Math.max(1, 15, 50, 7);   // 50
let number2 = Math.min(1, 15, 50, 7);  // 1
let arredondr = Math.round(2.57);      // 3
let arredondrPracima = Math.ceil(2.27); // 3
```

---

## 21 — if

[Ver pasta](./21_Estrutura_Condicionais)

Estrutura condicional básica `if`, testando duas variáveis (`ticket` e `idade`) de forma independente, sem `else`.

```javascript
let ticket = false;
let idade = 20;

if (ticket == true) {
  console.log('Seja Bem vindo');
}
if (idade >= 18) {
  console.log('Prossiga com a festa');
}
```

---

## 22 — if / else

[Ver pasta](./22_Estrutura_Condicional_Else)

Mesmo cenário do exercício anterior, agora usando `else` para tratar o caso contrário dentro da mesma estrutura, evitando repetir a lógica em dois blocos `if` separados.

```javascript
if (ticket == true) {
  console.log('Seja Bem vindo');
} else {
  console.log('Volte para sua casa');
}
```

---

## 23 — if / else if / else

[Ver pasta](./23_Estrutura_CondicionalElseIF)

Encadeamento de múltiplas condições com `else if`, combinando operadores lógicos (`&&`) para testar mais de uma variável na mesma condição.

```javascript
if (ticket == true && idade >= 18) {
  console.log('Seja Bem vindo e prossiga na festa.');
} else if (filhoDoDono) {
  console.log('Prossiga e mande um abraço para o chefe.');
} else {
  console.log('Volte para sua casa');
}
```

---

## 24 — Condicionais Aninhadas (if dentro de if)

[Ver pasta](./24_condicional_if_com_if)

Um `if` dentro de outro `if`, usado para validar uma regra secundária (idade do acompanhante) somente depois que a condição principal já foi satisfeita.

```javascript
if (ticket == true && idade >= 18 && acompanhante == true) {
  if (idadeAcompanhante >= 18) {
    console.log('Seja Bem vindo e prossiga na festa.');
  } else {
    console.log('Infelizmente o seu acompanhante não pode entrar.');
  }
} else if (filhoDoDono) {
  console.log('Prossiga e mande um abraço para o chefe.');
} else {
  console.log('Volte para sua casa');
}
```

---

## 31 — switch

[Ver pasta](./31_condicional_switch)

Estrutura `switch/case` como alternativa a uma cadeia longa de `else if`, útil quando se compara uma mesma variável contra vários valores possíveis. `break` evita que a execução "vaze" para o próximo `case`, e `default` cobre o caso que não bate com nenhuma opção.

```javascript
switch (raca) {
  case 'Bigol':
    console.log('A raça é Bigol');
    break;
  case 'Hotweiller':
    console.log('A raça é Hotweiller');
    break;
  default:
    console.log('Nenhuma raça encontrada');
}
```

---

## 25 — while

[Ver pasta](./25_laco_while)

Laço `while`: repete um bloco de código enquanto a condição for verdadeira. Usado aqui para contar de 20 até 1.

```javascript
let count = 20;
while (count > 0) {
  console.log(count);
  count = count - 1;
}
```

---

## 26 — do...while

[Ver pasta](./26_laco_do_while)

Variante do `while` em que o bloco é executado **pelo menos uma vez** antes de checar a condição — a diferença fica clara comparando os dois exemplos do arquivo (contagem regressiva e contagem progressiva).

```javascript
let count = 10;
do {
  count = count - 1;
  console.log(count);
} while (count > 0);
```

---

## 27 — for

[Ver pasta](./27_laco_for)

Laço `for`, o mais usado para repetições com número definido de passos. O segundo exemplo mostra o uso mais comum na prática: percorrer um array usando o índice (`i`) e a propriedade `.length`.

```javascript
for (let i = 0; i < 10; i = i + 1) {
  console.log(i);
}

let nomes = ['Vinicius', 'João', 'Andressa', 'Ricardo'];
for (let i = 0; i < nomes.length; i = i + 1) {
  console.log(nomes[i]);
}
```

---

## 28 — break

[Ver pasta](./28_break)

A palavra-chave `break` interrompe o laço completamente assim que a condição é atendida — aqui, o loop para no momento em que `i` chega a 5.

```javascript
for (let i = 0; i <= 10; i = i + 1) {
  if (i == 5) {
    console.log('Parou o loop');
    break;
  }
  console.log(i);
}
```

---

## 29 — continue

[Ver pasta](./29_continue)

A palavra-chave `continue` pula apenas a iteração atual e segue para a próxima, sem interromper o laço inteiro — diferente do `break`.

```javascript
for (let i = 0; i <= 10; i = i + 1) {
  if (i == 7) {
    console.log('Pulamos o: ' + i);
    continue;
  }
  console.log(i);
}
```

---

## 30 — Incrementação (`+=` e `++`)

[Ver pasta](./30_Incrementacao)

Duas formas equivalentes de incrementar uma variável a cada volta do laço: `i += 1` (soma e reatribui) e `i++` (operador de incremento, forma mais curta e comum).

```javascript
for (let i = 0; i < 10; i += 1) { console.log(i); }
for (let i = 0; i < 10; i++) { console.log(i); }
```

---

## 32 — Definindo Funções

[Ver pasta](./32_Definindo_funcao)

Três formas de declarar e usar funções: função sem retorno (apenas executa uma ação), função com `return` (devolve um valor que pode ser usado depois) e função anônima atribuída a uma constante (function expression).

```javascript
function imprimirMsgConsole() {
  console.log('Esta é uma função');
}
imprimirMsgConsole();

function soma(a, b) {
  return a + b;
}
console.log(soma(1, 5));

const cadastraUsuario = function (name) {
  console.log(name);
};
cadastraUsuario('Josi');
```

---

## 33 — Mais Exemplos de Função

[Ver pasta](./33_MaisFuncao)

Duas funções mais elaboradas: uma que valida uma condição (maioridade) e outra que combina função com laço `for` para gerar a tabuada de um número.

```javascript
function verifyAge(number) {
  if (number >= 18) {
    console.log('Você já é de maior');
  } else {
    console.log('Você ainda é uma criança');
  }
}
verifyAge(15);

function tabuada(number) {
  for (let i = 1; i <= 10; i++) {
    console.log(`${number} X ${i} = ${number * i}`);
  }
}
tabuada(8);
```

---

## 34 — Escopo de Função

[Ver pasta](./34_Escopo_Funcao)

Demonstra escopo de variáveis: uma variável global (`numero = 100`), uma variável local de mesmo nome dentro de uma função (não conflita com a global) e uma variável de escopo de bloco dentro de um `if`.

```javascript
let numero = 100; // variável global

function number() {
  let numero = 350; // variável local, mesmo nome, escopo diferente
  console.log(numero);
}
number();

if (1 == 1) {
  let numero = 1000; // escopo restrito ao bloco do if
  console.log(numero);
}
```

---

## 35 — Arrow Function

[Ver pasta](./35_Arrow_Function)

Sintaxe moderna e mais curta para escrever funções (`=>`), atribuídas a uma constante — alternativa às funções tradicionais vistas no exercício 32.

```javascript
const animal = (name) => {
  console.log(name);
};
animal('Cachorro');

const soma = (number) => {
  console.log(number + 5);
};
soma(10);
```

---

## 36 — Argumentos Opcionais

[Ver pasta](./36_ArgumentosOpcionais)

Validação manual de argumentos: a função verifica se algum parâmetro não foi passado (`undefined`) antes de executar a lógica principal.

```javascript
const veiculo = (nome, marca) => {
  if (nome == undefined || marca == undefined) {
    console.log('É necessário passar os dois argumentos.');
  } else {
    console.log(nome, marca);
  }
};
veiculo('c4 Pallas'); // marca não foi informada
```

---

## 37 — Argumentos Default

[Ver pasta](./37_Argumentos_Default)

Forma nativa do JavaScript de definir um valor padrão para um parâmetro, usado automaticamente quando o argumento não é informado na chamada da função.

```javascript
function createRouterLogin(username, password = 'hjuioplkn') {
  console.log(username, password);
}
createRouterLogin('Josi'); // usa a senha padrão
```

---

## 38 — Closure

[Ver pasta](./38_closure)

Uma função que retorna outra função, "guardando" (fechando sobre) o valor do parâmetro externo mesmo depois que a função externa já terminou de executar — é a base do conceito de *closure* em JavaScript.

```javascript
function armazenaSoma(x) {
  return (y) => x + y;
}

let soma1 = armazenaSoma(10);
console.log(soma1(5)); // 15 — "lembra" que x = 10
```

---

## 39 — Recursão

[Ver pasta](./39_recursion)

Função que chama a si mesma até atingir uma condição de parada — aqui, decrementa o número até encontrar um valor par.

```javascript
function retornaNumeroPar(number) {
  if (number % 2 == 0) {
    console.log('O numero é par: ' + number);
  } else {
    console.log(number);
    retornaNumeroPar(number - 1); // chamada recursiva
  }
}
retornaNumeroPar(39);
```

---

## 40 — Array

[Ver pasta](./40_Array)

Criação de arrays e acesso a seus elementos por índice — incluindo o padrão comum de acessar o último elemento com `array.length - 1`.

```javascript
const arrayNomes = ['Josi', 'Leandro', 'Debi', 'Tinho'];

console.log(arrayNomes[1]);                    // 'Leandro'
console.log(arrayNomes[arrayNomes.length - 1]); // 'Tinho' — último elemento
```

---

## 41 — Métodos e Objetos

[Ver pasta](./41_Metodo)

Dois conceitos no mesmo exercício: **método de array** (`toLocaleUpperCase()`, que transforma uma string em maiúsculas) e **objeto literal**, com propriedades (`raca`, `patas`, `doenca`, `cor`) e um método próprio (`latir()`).

```javascript
const arrayAnimal = ['Cachorro', 'Passáro', 'Gato'];
console.log(arrayAnimal[2].toLocaleUpperCase()); // 'GATO'

const Cachorro = {
  raca: 'Labrador',
  patas: 4,
  doenca: false,
  cor: 'Branco',
  latir() {
    console.log('Au Au');
  },
};

console.log(Cachorro.raca);
Cachorro.latir();
```

---

## Principais aprendizados

- Funções nativas do navegador: `prompt()`, `alert()` e o objeto `Math`
- Estruturas condicionais completas: `if`, `if/else`, `else if`, condicionais aninhadas e `switch`
- Laços de repetição: `while`, `do...while`, `for`, e controle de fluxo com `break` e `continue`
- Declaração de funções (tradicional, function expression e arrow function)
- Escopo de variáveis (global, de função e de bloco)
- Conceitos intermediários: argumentos default/opcionais, closures e recursão
- Arrays e objetos: acesso por índice, métodos de string e objetos literais com propriedades e métodos próprios

**Próximos passos:** métodos de array mais avançados (`map`, `filter`, `reduce`, `forEach`), manipulação do DOM e eventos — para conectar a lógica em JavaScript com interações reais na página.
