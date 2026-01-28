# O que são arrays

Arrays são estruturas que permitem armazenar vários valores dentro de uma única variável, de forma organizada.

- Cada valor fica em uma posição (índice).

📌 Exemplo sem array:
```javascript
let fruta1 = "Maçã";
let fruta2 = "Banana";
```

📌 Com array:
```javascript
let frutas = ["Maçã", "Banana", "Uva"];
```

# 2. Criando arrays

```js
let numeros = [1, 2, 3, 4];
let nomes = ["Ana", "João"];
let misto = [10, "Texto", true];
```

- Arrays podem ter tipos misturados

# 🔍 3. Acessando elementos do array
Usamos indíce (começa no 0)

```js
let frutas = ["Maçã", "Banana", "Uva"];

console.log(frutas[0]); // Maçã
console.log(frutas[1]); // Banana
```

# ✏️ 4. Alterando valores do array

```js
frutas[1] = "Morango";
```

# 5. Tamanho do array (`length`)
```js
let frutas = ["Maçã", "Banana", "Uva"];

console.log(frutas.length); // 3
```

- Retorna quantos elementos existem no array.

# 🧰 6. Principais métodos de arrays

➕ `push` (adiciona no final)
```js
frutas.push("Abacaxi");
```

➕ `unshift` (adiciona no início)
```js
frutas.unshift("Laranja");
```

➖ `pop` (remove o último)
```js
frutas.pop();
```

➖ `shift` (remove o primeiro)
```js
frutas.shift();
```

# 🔄 7. Percorrendo arrays 

Com `for`:
```js
for (let i = 0; i < frutas.length; i++) {
  console.log(frutas[i]);
}
```

Com `for...of`:
```js
for (let fruta of frutas) {
  console.log(fruta);
}
```
Com `forEach`:
```js
frutas.forEach(fruta => {
  console.log(fruta);
});
```

**Por que usamos length no loop?**

-> Porque o length diz quantos elementos existem no array.

👉 E no `for` precisa saber até onde ele pode ir sem estourar o array.

🔍 Entendendo passo a passo

Suponha:
```js
let frutas = ["Maçã", "Banana", "Uva"];
```

O array é assim na memória:

| Índice | Valor | 
|----------|-------------|
| `0` | Maça |
| `1`   | Banana |
| `2` | Uva |

```js
frutas.length // 3
```
📌 O último índice válido é length - 1.


O que o loop faz:
```js
let i = 0;           // começa no primeiro índice
i < frutas.length;  // enquanto i for menor que 3
i++;                // anda para o próximo índice
```

Valores de `i`:

- `i = 0` → frutas[0] ✅
- `i = 1` → frutas[1] ✅
- `i = 2` → frutas[2] ✅
- `i = 3` → ❌ para (3 < 3 é falso)

➡️ Assim ele percorre todos os elementos sem erro.

-------------------
**OBS:** No dia a dia, não se usa tanto o `for` tradicional com índice para percorrer arrays simples.

O mais comum hoje é usar `for...of` e `forEach`.

🔹 `for...of` (simples e limpo)

📌 Funciona bem quando precisa de break

```js
for (let fruta of frutas) {
  console.log(fruta);
}
```

🔹 forEach **(muito usado)**

📌 Ideal quando você só quer percorrer e fazer algo.

```js
frutas.forEach(fruta => {
  console.log(fruta);
});
```

⚠️ Quando usar o `for` tradicional

- Precisa do índice
- Precisa pular posições
- Precisa controlar início/fim
- Trabalha com lógica mais complexa

# 🧱 8. Arrays de objetos

Muito comum em sistemas:
```js
let produtos = [
  { nome: "Caneta", preco: 2.5 },
  { nome: "Caderno", preco: 15 }
];
```

Percorrendo:

```js
produtos.forEach(produto => {
  console.log(produto.nome);
});
```

🔹 O que é o `for...in`?

O `for...in` percorre as CHAVES, não os valores.

👉 Ele é feito principalmente para objetos, não para arrays.

```js
const usuario = {
  nome: "Gabrielle",
  idade: 20,
  curso: "ADS"
};

for (let chave in usuario) {
  console.log(chave, usuario[chave]);
}
```

🔎 Resultado:

```nginx
nome Gabrielle
idade 20
curso ADS
```

# ⚡ 9. Métodos modernos (`map`, `filter`, `find`)

`map` (transforma array)

- Percorre o array e cria um NOVO array, transformando cada item.
```js
let numeros = [1, 2, 3, 4];

let dobro = numeros.map(n => n * 2);

console.log(dobro);
// [2, 4, 6, 8]
```

<h3>📦 Exemplo com objetos</h3>

```js
let produtos = [
  { nome: "Caneta", preco: 2.5 },
  { nome: "Caderno", preco: 15 }
];

let nomes = produtos.map(produto => produto.nome);

console.log(nomes);
// ["Caneta", "Caderno"]
```

🧠 Quando usar map?

- modificar dados
- formatar valores
- criar um novo array baseado em outro
<br><br>

`filter` (filtra array)
- Cria um novo array só com os itens que passam na condição.

📌 A função precisa retornar `true` ou `false`.

```js
let numeros = [1, 2, 3, 4, 5];

let pares = numeros.filter(n => n % 2 === 0);

console.log(pares);
// [2, 4]
```

<h3>📦 Exemplo com objetos</h3>

```js
let caros = produtos.filter(produto => produto.preco > 10);

console.log(caros);
// [{ nome: "Caderno", preco: 15 }]
```

🧠 Quando usar filter?

- remover itens
- selecionar itens específicos
- aplicar condições
<br><br>

`find` (encontra um item)
- Retorna o PRIMEIRO item que satisfaz a condição.

```js
let numeros = [1, 2, 3, 4];

let encontrado = numeros.find(n => n > 2);

console.log(encontrado);
// 3
```

<h3>📦 Exemplo com objetos</h3>

```js
let produto = produtos.find(p => p.nome === "Caneta");

console.log(produto);
// { nome: "Caneta", preco: 2.5 }
```

🧠 Quando usar find?

- encontrar um único item
- buscar por ID
- localizar um registro

