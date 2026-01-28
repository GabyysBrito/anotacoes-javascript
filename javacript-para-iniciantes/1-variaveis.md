# 🧠 1. O que são variáveis
-> Variáveis são espaços na memória usados para guardar informações que podem ser usadas depois.

📌 Pense nelas como caixinhas com nome.

```js
let nome = "Gabrielle";
```

# 🎯 2. Para que servem as variáveis

> Usamos variáveis para:

- guardar valores
- reutilizar dados
- evitar repetição
- facilitar leitura do código
- tornar o código dinâmico

# 🧩 3. Declarando variáveis (`var`, `let`, `const`)

🔹`let`

```js
let idade = 20;
```

✔ pode mudar o valor

<br><br>
🔹`const`
```js
const pi = 3.14;
```

✔ valor fixo

❌ não pode reatribuir

<br><br>
🔹`var` (evite usar)
```js
var cidade = "São Paulo";
```
❌ escopo confuso

❌ comportamento antigo

<br><br>

# 🔍 5. Escopo de variáveis

-> Escopo é onde a variável existe.

```js
if (true) {
  let x = 10;
}

console.log(x); // erro
```

Com `var`:

```js
if (true) {
  var y = 10;
}

console.log(y); // funciona (problema)
```

# 🔄 6. Reatribuição de valores

Com `let`:
```js
let contador = 0;
contador = 1;
```

Com `const`:
```js
const idade = 20;
idade = 21; // erro
```

# 🧪 7. Tipos de dados em variáveis

```js
let nome = "Texto";     // string
let idade = 20;        // number
let ativo = true;      // boolean
let lista = [];        // array
let pessoa = {};       // objeto
let vazio = null;      // nulo
let indefinido;        // undefined
```