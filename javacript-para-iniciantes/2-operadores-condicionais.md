# Números e Operadores

## 🧠 1. O que são números em JavaScript
-> Em JavaScript, não existe separação entre inteiro e decimal como em outras linguagens.

Tudo é do tipo `number`.

```js
let idade = 20;
let preco = 19.99;
```

## 🔢 2. Tipos de números
-> Mesmo sendo tudo `number`, podemos ter:

```js
let inteiro = 10;
let decimal = 2.5;
let negativo = -3;
```
- 📌 Internamente, o JS trata tudo como número.

## ➕➖ 3. Operadores aritméticos

| Operador | Sigificado | Exemplo |
|----------|------------|---------|
|`+`|Soma|`2 + 2`|
|`-`|Subtração|`5 - 3`|
|`*`|Multiplicação|`4 * 2`|
|`/`|Divisão|`10 / 2`|
|`%`|Resto|`10 % 3`|

📌 Exemplo:

```js
let total = 10 + 5 * 2; // 20
```

## 🔢 4. Ordem de precedência

JavaScript segue a matemática:

1️⃣ Parênteses

2️⃣ Multiplicação e divisão

3️⃣ Soma e subtração

```js
let resultado = (10 + 5) * 2; // 30
```
## 🧩 5. Operadores de atribuição
```js
let x = 10;

x += 5; // x = x + 5
x -= 2; // x = x - 2
x *= 3; // x = x * 3
x /= 2; // x = x / 2
```

## 🔼🔽 6. Incremento e decremento

➕ Incremento (++)
- Soma 1 ao valor da variável.

```js
let x = 5;
x++;   // agora x vale 6
```

<br>

➖ Decremento (--)
- Subtrai 1 do valor da variável.

```js
let y = 5;
y--;   // agora y vale 4
```

### 🔹 Pré vs Pós 
A diferença NÃO é no resultado final da variável,
mas no momento em que o valor é usado.

#### 1️⃣ Pós-incremento (`variavel++`)
👉 Usa o valor atual primeiro,

👉 incrementa depois.

```js
let a = 5;
console.log(a++); // 5
console.log(a);   // 6
```

O que aconteceu:

1. Mostrou `5`
2. Depois somou `1`

#### 1️⃣ Pré-incremento (`++variavel`)
👉 Incrementa primeiro, <br>
👉 usa o valor depois.

```js
let b = 5;
console.log(++b); // 6
console.log(b);   // 6
```

🧠 O que aconteceu:

1. Somou 1
2. Depois mostrou 6

### 🔁 Mesmo vale para decremento

#### Pós-decremento
```js
let c = 5;
console.log(c--); // 5
console.log(c);   // 4
```

#### Pré-decremento
```js
let d = 5;
console.log(--d); // 4
console.log(d);   // 4
```

#### 🔎 Comparação direta 

| Tipo | O que acontece primeiro |
|------|-------------------------|
|`x++` | usa  o valor → depois soma|
|`++x` | soma → depois usa|
|`x--` | usa o valor → depois subtrai|
|`--x` | subtrai → depois usa|

## 🔄 7. Conversão de números
```js
Number("10");     // 10
parseInt("10");  // 10
parseFloat("2.5"); // 2.5
```

# Boolean e Condicionais

## 🧠 Boolean
-> Boolean é um tipo de dado lógico que só pode ter dois valores

📌 Exemplo:
```javascript
true
false
```
```javascript
let possuiGraduacao = true;
let possuiDoutorado = false;
```

É usado para decisões no código.

## Expressões booleanas
-> São expressões que o JavaScript avalia como true ou false.

### **1. Operadores de comparação**

| Operador | Significado |
|----------|-------------|
| `>`  | maior que |
| `<`  | menor que |
| `>=` | maior ou igual |
| `<=` | menor ou igual |
| `==` | igual (compara valor) |
| `===` | igual estrito (valor e tipo) |
| `!=` | diferente |
| `!==` | diferente estrito |

📌 Exemplo:
```javascript
let idade = 18;
idade >= 18; // true
```

```javascript
10 > 5; // true
5 > 10; // false
20 < 10; // false
10 <= 10 // true
10 >= 11 // false
```


```javascript

10 == '10'; // true
10 == 10; // true
10 === '10'; // false
10 === 10 // true
10 != 15 // true
10 != '10' // false
10 !== '10' // true

```

### **2. Operadores Lógicos**
`&&` (E)
| Operador | Significado | 
|----------|-------------|
| `&&, AND, E` | todas as condições verdadeiras |
| ` \|\|, OR, OU`   | pelo menos uma verdadeira |
| `!, NOT, NÃO` | inverte o valor |

📌 Exemplo:

```javascript
// Usando (E)
idade >= 18 && temCNH

// Usando (OU)
temCartao || temDinheiro

// Usando (NÃO)
!true  // false
!false // true
```

## 🧩 Estrutura Condicional
### O que é uma condição?
-> É uma decisão que o programa toma com base em um valor booleano.

### **Condições If e Else**
->  Verificar se uma expressão é verdadeira com if, caso contrário o else será ativado.

### 1. `if`
Executa o código se a condição for verdadeira.

📌 Exemplo:
```javascript
if (idade >= 18) {
  console.log("Maior de idade");
}
```

### 2. `else`
Executa quando a condição for falsa.

📌 Exemplo:
```javascript
if (idade >= 18) {
  console.log("Maior de idade");
} else {
  console.log("Menor de idade");
}
```

### 3. `else if`

📌 Exemplo:

Usado quando há mais de uma condição.

```javascript
if (nota >= 7) {
  console.log("Aprovado");
} else if (nota >= 5) {
  console.log("Recuperação");
} else {
  console.log("Reprovado");
}
```

### Condições aninhadas
-> Um if dentro de outro.

📌 Exemplo:

```javascript
if (idade >= 18) {
  if (temCNH) {
    console.log("Pode dirigir");
  }
}
```

### Operador Ternário
-> Forma curta de escrever um if/else.

📌 Exemplo:

```javascript
let status = idade >= 18 ? "Maior" : "Menor";
```

### **Switch**
-> Com o switch você pode verificar se uma variável é igual à diferentes valores utilizando o case. Caso ela seja igual, você pode fazer alguma coisa e utilizar a palavra chave break; para cancelar a continuação. O valor de default ocorrerá caso nenhuma das anteriores seja verdadeira.

📌 Exemplo:

```javascript
let corFavorita = 'Azul'

switch (corFavorita) {
    case 'Azul':
    console.log('Olhe para o céu.');
    break;
  case 'Vermelho':
    console.log('Olhe para rosas.');
    break;
  case 'Amarelo':
    console.log('Olhe para o sol.');
    break;
  default:
    console.log('Feche os olhos');
}
```
