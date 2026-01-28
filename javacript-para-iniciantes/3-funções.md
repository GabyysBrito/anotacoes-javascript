# Função em JavaScript

## 🧠 1. O que são funções
-> Funções são blocos de código reutilizáveis que executam uma tarefa específica.

📌 Em vez de repetir o mesmo código várias vezes, você cria uma função e usa quando precisar.

## 🎯 2. Para que servem as funções

Funções servem para:

- Organizar o código
- Evitar repetição
- Facilitar manutenção
- Deixar o código mais legível
- Resolver problemas por partes

## 🧩 3. Estrutura básica de uma função

```javascript
function nomeDaFuncao() {
    //código aqui
}
```

📌 Exemplo:
```javascript
function mostrarMensagem() {
    console.log("Olá, Mundo!");
}
```

## ▶️ 4. Chamando (executando) uma função
-> Criar a função não executa ela.

-> Para executar, você precisa chamar:

```javascript
mostrarMensagem();
```

## 📥 5. Parâmetros e argumentos
-> Parâmetros são os valores que a função recebe para trabalhar.

```javascript
function saudacao(nome) {
  console.log("Olá, " + nome);
}
```

```javascript
saudacao("Gabrielle");
```

➡️ nome é o parâmetro

➡️ "Gabrielle" é o argumento

## 🔄 6. Retorno de valores(return)
-> Funções podem devolver um valor para quem chamou.

```javascript
function soma(a, b) {
    return a + b;
}

```

- Usando o retorno:

```javascript
let resultado = soma(3, 4);
console.log(resultado); //7

```

## 🔍 7. Funções com e sem retorno

- Sem retorno

```javascript
function mostrarNome() {
  console.log("Gabrielle");
}
```

- Com retorno
```javascript
function dobro(numero) {
  return numero * 2;
}
```

## 👤 8. Funções anônimas
-> Funções sem nome, geralmente guardadas em variáveis

```javascript
const saudacao = function(nome) {
  console.log("Oi " + nome);
};
```

## ⚡ 9. Arrow Functions
-> Formas modernas e mais curtas de escrever funções

```javascript
const soma = (a, b) => {
    return a + b;
}

console.log(soma(2,3))
```
Ou ainda mais simples:

```javascript
const soma = (a, b) => a + b;

console.log(soma(2,3))
``` 

## ✅ 10. Boas práticas com funções

✔ Nome claro e objetivo <br>
✔ Função faz apenas uma coisa <br>
✔ Evite funções muito grandes <br>
✔ Use verbos nos nomes:

- calcularTotal
- mostrarMensagem
- validarUsuario
