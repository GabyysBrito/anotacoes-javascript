# 📚 Objetos em JavaScript

## 🧠 O que são objetos
-> Objetos são estruturas que permitem guardar vários dados relacionados em um só lugar.

- Em vez de várias variáveis soltas, usamos um objeto.

📌 Exemplo sem objeto:

```javascript
let nome = "Gabrielle";
let idade = 20;
let curso = "ADS";
```

Com objeto:

```javascript
let pessoa = {
  nome: "Gabrielle",
  idade: 20,
  curso: "ADS"
};
```

## 🧩 2. Estrutura de um objeto

```javascript
const objeto = {
    chave: valor,
    chave2: valor2,
}
```
📌 Exemplo

```javascript
const carro = {
  marca: "Toyota",
  ano: 2020,
  cor: "Preto"
};
```

## 📦 3. Propriedades e métodos
- **Propriedades**: dados do objeto
- **Métodos**: funções dentro do objeto

```javascript
const usuario = {
  nome: "Gabrielle",
  idade: 20,
  estudar: function() {
    console.log("Estudando...");
  }
};
```

## 🔍 4. Acessando dados do objeto
<h3>Forma com ponto:</h3>

```javascript
console.log(usuario.nome);
```

<h3>Forma com colchetes:</h3>

```javascript
console.log(usuario["idade"]);
```

📌 A forma com colchetes é útil quando o nome da chave vem de uma variável.

## ✏️ 5. Alterando e adicionando propriedades

<h3>Alterar:</h3>

```javascript
usuario.idade = 21;
```

<h3>Adicionar:</h3>

```javascript
usuario.cidade = "São Paulo";
```

## ⚙️ 6. Objetos com funções (métodos)

```javascript
const pessoa = {
  nome: "Gabrielle",
  apresentar() {
    console.log("Oi, meu nome é " + this.nome);
  }
};
```

Chamando o método:
```javascript
pessoa.apresentar();
```
📌 this se refere ao próprio objeto.

## 🔄 7. Percorrendo objetos

Com `for...in`:
```javascript
for (let chave in pessoa) {
  console.log(chave, pessoa[chave]);
}
```

## 🏠 8. Objetos dentro de objetos

```javascript
const aluno = {
  nome: "Gabrielle",
  curso: {
    nome: "ADS",
    periodo: "2º"
  }
};
```
📌 Acessando:
```javascript
console.log(aluno.curso.nome);
```

## 📚 9. Arrays de objetos
Muito comum em sistemas:

```javascript
const produtos = [
  { nome: "Caneta", preco: 2.5 },
  { nome: "Caderno", preco: 15 }
];
```

Percorrendo:
```javascript
produtos.forEach(produto => {
  console.log(produto.nome);
});
```