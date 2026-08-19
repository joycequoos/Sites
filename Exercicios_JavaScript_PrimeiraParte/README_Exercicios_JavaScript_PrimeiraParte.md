
# Exercícios JavaScript — Primeira Parte

[← Voltar para Desenvolvimento Web](https://github.com/joycequoos/Development)

Exercícios práticos de fundamentos de JavaScript: tipos de dados, operadores, strings, booleanos, variáveis e palavras reservadas. Cada pasta contém um `index.html` e um `script.js` executável diretamente no navegador.

## Sumário

- [01 — Compilando JavaScript Externo](#01--compilando-javascript-externo)
- [02 — Tipos de Dados: Number](#02--tipos-de-dados-number)
- [03 — Operações Aritméticas](#03--operações-aritméticas)
- [04 — Números Especiais](#04--números-especiais)
- [05 — Strings (Parte 1)](#05--strings-parte-1)
- [06 — Strings (Parte 2)](#06--strings-parte-2)
- [07 — Boolean](#07--boolean)
- [08 — Comparações Booleanas](#08--comparações-booleanas)
- [09 — Operadores Lógicos](#09--operadores-lógicos)
- [10 — Operador Ternário](#10--operador-ternário)
- [11 — Empty Values (null / undefined)](#11--empty-values-null--undefined)
- [12 — Conversão Automática de Tipos](#12--conversão-automática-de-tipos)
- [13 — Variáveis](#13--variáveis)
- [14 — Variáveis: var, let, const](#14--variáveis-var-let-const)
- [15 — Convenções de Nomes de Variáveis](#15--convenções-de-nomes-de-variáveis)
- [16 — Palavras Reservadas](#16--palavras-reservadas)

---

## 01 — Compilando JavaScript Externo

[Ver pasta](./01_CompilarJS)

Primeiro contato com JavaScript rodando a partir de um arquivo externo (`.js`) importado no HTML, em vez de escrito direto na página. Mostra o uso básico do `console.log()` para exibir mensagens no console do navegador.

```javascript
console.log('Javascript externo.');
```

---

## 02 — Tipos de Dados: Number

[Ver pasta](./02_Number)

Uso do operador `typeof` para identificar o tipo de um valor — número inteiro, número negativo, número decimal e string — mostrando como o JavaScript classifica cada um internamente.

```javascript
console.log(typeof 12);      // number
console.log(typeof -12);     // number
console.log(typeof 1.17);    // number
console.log(typeof '1.17');  // string
```

---

## 03 — Operações Aritméticas

[Ver pasta](./03_OperAritimeticas)

As cinco operações aritméticas básicas: soma, subtração, multiplicação, divisão e resto da divisão (módulo).

```javascript
console.log(5 + 5);   // soma
console.log(5 * 5);   // multiplicação
console.log(5 - 5);   // subtração
console.log(20 / 2);  // divisão
console.log(10 % 2);  // resto (módulo)
```

---

## 04 — Números Especiais

[Ver pasta](./04_SpecialNumber)

Introdução aos valores numéricos especiais do JavaScript: `Infinity`, `-Infinity` e `NaN` (*Not a Number* — usado quando uma operação matemática não resulta em um número válido).

```javascript
console.log(Infinity);
console.log(-Infinity);
console.log(NaN);
```

---

## 05 — Strings (Parte 1)

[Ver pasta](./05_Strings01)

As diferentes formas de declarar uma string em JavaScript — aspas simples, aspas duplas, aspas aninhadas (uma dentro da outra) e template strings (crase). Também reforça que `Infinity` pode ser tratado tanto como texto quanto como valor numérico especial.

```javascript
console.log("Este é um texto");
console.log('Este é um texto');
console.log('Este é "um" texto');
console.log("Este é 'um' texto");
console.log(`Este é um texto`);
```

---

## 06 — Strings (Parte 2)

[Ver pasta](./06_Strings02)

Recursos mais avançados de strings: quebra de linha com `\n`, interpolação de variáveis dentro de template strings (`${}`) e concatenação de textos com o operador `+`.

```javascript
console.log("Este\n texto \n quebra\n a linha");

let soma = 10 + 10;
console.log(`A soma de 10 + 10 é ${soma}`);

console.log('String' + 'Concatenada');
console.log('String ' + 'Concatenada ' + 'com ' + 'espaço');
```

---

## 07 — Boolean

[Ver pasta](./07_Boolean)

Introdução ao tipo booleano (`true` / `false`) e como expressões de comparação retornam automaticamente um valor booleano.

```javascript
console.log(true);
console.log(false);
console.log(5 > 2);    // true
console.log(10 > 100); // false
```

---

## 08 — Comparações Booleanas

[Ver pasta](./08_CompBoolean)

Todos os operadores de comparação do JavaScript: maior que, menor que, maior ou igual, menor ou igual, igual (`==`), diferente (`!=`) e idêntico (`===` — compara valor **e** tipo).

```javascript
console.log(10 > 5);              // true
console.log(50 < 100);            // true
console.log(100 >= 100);          // true
console.log(100 <= 50);           // false
console.log(50 == 50);            // true
console.log('vinicius' != 'vinicius'); // false
console.log('5' === 5);           // false — tipos diferentes (string vs number)
console.log(5 === 5);             // true — mesmo valor e mesmo tipo
```

---

## 09 — Operadores Lógicos

[Ver pasta](./09_OpLogicos)

Os operadores lógicos `&&` (E), `||` (OU) usados para combinar múltiplas condições em uma única expressão booleana.

```javascript
console.log(10 > 5 && 50 < 100);  // true — as duas condições são verdadeiras
console.log(10 > 5 || 50 > 100);  // true — pelo menos uma condição é verdadeira
console.log((50 > 4));
```

---

## 10 — Operador Ternário

[Ver pasta](./10_OpTernario)

Forma resumida de escrever uma condição `if/else` em uma única linha: `condição ? valorSeVerdadeiro : valorSeFalso`.

```javascript
console.log(10 < 7 ? 'certo' : 'errado'); // 'errado'
```

---

## 11 — Empty Values (null / undefined)

[Ver pasta](./11_empyValues)

Introdução aos valores que representam "ausência de dado" em JavaScript: `null` (ausência intencional de valor) e `undefined` (variável ainda não definida).

```javascript
campoNome == null ? 'certo' : 'errado';
```

---

## 12 — Conversão Automática de Tipos

[Ver pasta](./12_ConversaoAuto)

Demonstra a *coerção de tipos* — quando o JavaScript converte automaticamente um tipo de dado para outro ao executar uma operação, o que pode gerar resultados inesperados se não for bem entendido.

```javascript
console.log(10 * null);       // 0 — null vira 0 na multiplicação
console.log("20" - 5);        // 15 — string numérica vira number na subtração
console.log("20" + 5);        // "205" — number vira string na concatenação
console.log('cinco' * 'cinco'); // NaN — texto não numérico não pode virar number
```

---

## 13 — Variáveis

[Ver pasta](./13_Variavel)

Declaração de variáveis com `let`, reatribuição de valor, uso em operações matemáticas, interpolação em template strings e declaração de múltiplas variáveis em uma única linha.

```javascript
let preco = 5;
console.log(preco);
console.log(preco * preco);
console.log(`O valor da sua compra foi de ${preco} reais`);

preco = 10;
console.log(`O valor da sua compra foi de ${preco} reais`);

let num1 = 1, num2 = 2, num3 = 3;
console.log(num1 + num2 + num3);
```

---

## 14 — Variáveis: var, let, const

[Ver pasta](./14_Variaveis-2)

Comparação entre as três formas de declarar variáveis em JavaScript: `var` (forma antiga), `let` (forma moderna, recomendada) e `const` (para valores que não podem ser reatribuídos).

```javascript
var variavel1 = 10;
let variavel2 = 20;
const variavel3 = 30; // não pode ser reatribuída depois

console.log(variavel1);
```

---

## 15 — Convenções de Nomes de Variáveis

[Ver pasta](./15_conversaoVar)

Exemplos de nomes válidos e boas práticas para nomear variáveis em JavaScript: uso de `camelCase`, `$` e `_` como caracteres permitidos, e a regra de que nomes não podem começar com número.

```javascript
let $name = 'vinicius';
let _name = 'vinicius';
let Name = 'Vinicius';
let nomeDeVariavelImput = 'vinicius';
let nome$vinicius = 'vinicius';
```

---

## 16 — Palavras Reservadas

[Ver pasta](./16_palavrasReservadas)

Lista de referência das palavras reservadas do JavaScript — termos que não podem ser usados como nomes de variáveis por já fazerem parte da sintaxe da linguagem (`if`, `for`, `function`, `return`, `class`, `let`, `var`, entre outras).

---

## Principais aprendizados

- Tipos primitivos do JavaScript (`number`, `string`, `boolean`, `null`, `undefined`) e como identificá-los com `typeof`
- Operadores aritméticos, de comparação e lógicos
- Diferentes formas de declarar strings, incluindo template strings e interpolação
- Diferenças entre `var`, `let` e `const`, e por que `let`/`const` são preferíveis hoje
- Conversão automática de tipos (coerção) e como ela pode gerar resultados inesperados
- Boas práticas de nomenclatura de variáveis

**Próximos passos:** estruturas condicionais (`if/else`, `switch`), estruturas de repetição (`for`, `while`) e funções — conteúdo provável da [Segunda Parte](https://github.com/joycequoos/Sites/tree/main/Exercicios_JavaScript_SegundaParte).
