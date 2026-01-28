# 🧠 1. O que são estruturas de repetição

São estruturas que permitem **executar o mesmo bloco de código várias vezes**, enquanto uma condição for verdadeira.

# 🎯 2. Para que servem os loops

Usamos laços para:
- Percorrer listas (arrays)
- Repetir tarefas automáticas
- Ler dados
- Criar contadores
- Processar informações

# 🔄 3. `while`
Repete enquanto a condição for verdadeira.

```javascript
let i = 0;

while (i < 5) {
  console.log(i);
  i++;
}
```

# 🔁 4. `do...while`
Executa pelo menos uma vez, mesmo se a condição for falsa.

```javascript
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 5);
```

# 🔂 5. `for`
**O mais usado!**

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

📌 Estrutura:
```javascript
for (início; condição; incremento) {
}
```

# 📦 6. `for...of`

Usado para percorrer **valores de arrays.**

```javascript
let frutas = ["Maçã", "Banana", "Uva"];

for (let fruta of frutas) {
  console.log(fruta);
}
```

# 🔑 7. `for...in`
Usado para percorrer **índices ou chaves.**

Em arrays:
```javascript
for (let i in frutas) {
  console.log(i); // índices
}
```

Em objetos:
```javascript
const pessoa = { nome: "Gabrielle", idade: 20 };

for (let chave in pessoa) {
  console.log(chave, pessoa[chave]);
}
```

# ⛔ 8. `break` e `continue`
`break`

Interrompe o loop.
```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  console.log(i);
}
```

`continue`

Pula uma repetição.
```javascript
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i);
}
```

# 📚 9. Laços com arrays
**Muito comum no dia a dia:**

```javascript
let numeros = [1, 2, 3, 4];

numeros.forEach(num => {
  console.log(num * 2);
});
```