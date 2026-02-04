# DOM em JavaScript
## 1️⃣ O que é Dom?

→ É a forma como o JavaScript enxerga e controla o HTML.

→ Cada tag vira um objeto que pode ser acessado, alterado ou removido.

<h4>
📄 HTML <br>
⬇️ <br>
🌳 DOM (árvore de elementos)
</h4>

## 2️⃣ Estrutura do DOM (árvore)

Exemplo HTML:

```html
<body>
  <h1>Título</h1>
  <p>Texto</p>
</body>
```

No DOM:

- `documento`
    - `body`
        - `h1`
        - `p`

Tudo começa no objeto `document`

----------

## 3️⃣ Selecionando elementos
### 🔹 `getElementById`: 

Seleciona um único elemento.

```js
const titulo = document.getElementById("#título")
```

HTML: 
```html
<h1 id="titulo">Olá</h1>
```

----

### 🔹 `getElementByClassName`: 

Seleciona vários elementos.

```js
const titulo = document.getElementById(".título")
```

HTML: 
```html
<h1 id="titulo">Olá</h1>
```

---

### 🔹 `getElementByTagName`: 
Seleciona pela tag

```js
const paragrafos = document.getElementsByTagName("p");
```

---
### 🔹 `querySelector`: (Mais usado)

Seleciona o primeiro que encontrar.

```js
const texto = document.querySelector(".texto");
```

---
### 🔹 `querySelectorAll`: 
Seleciona todos

```js
const botoes = document.querySelectorAll("button");
```

## 4️⃣ Manipulando conteúdo

### 🔹 `textContent`
Altera somente o texto 

```js
titulo.innerHTML = "<span>Olá</span>";
```

---

### 🔹 `innerHTML`
Altera texto com HTML

```js
titulo.innerHTML = "<span>Olá</span>";
```

## 5️⃣ Manipulando estilos

```js
titulo.style.color = "blue";
titulo.style.fontSize = "30px";
```

CSS vira camelCase:

- `font-size` → `fontSize`

## 6️⃣ Manipulando atributos
→ Atributos são as informações dentro das tags HTML:

```html
<input type="text" disabled>
<img src="foto.png" alt="Imagem">
<a href="https://site.com">Link</a>
```

### 🔹 Alterar atributo
```js
img.src = "foto.png";
```

### 🔹 Usando métodos

```js
img.setAttribute("alt", "Imagem");
img.removeAttribute("alt");
```

### 🔹 Sobre o setAttribute()
→ Cria ou altera um atributo em um elemento.

📌 Sintaxe
```js
elemento.setAttribute("atributo", "valor");
```

✅ Exemplo 1: alterar o src de uma imagem
```js
const img = document.querySelector("img");
img.setAttribute("src", "nova-foto.png");
```

✅ Exemplo 2: adicionar disabled em um input

```js
const input = document.querySelector("input");
input.setAttribute("disabled", "true");
```

Resultado:

```js
<input disabled>
```
📌 Mesmo passando "true", o HTML entende apenas que o atributo existe.

### 🔹 `removeAttribute()`
→ Remove completamente um atributo do elemento.

📌 Sintaxe
```js
elemento.removeAttribute("atributo");
```

✅ Exemplo 1: habilitar um input
```js
input.removeAttribute("disabled");
```
📌 Agora o campo volta a ser editável.

✅ Exemplo 2: remover href de um link

```js
link.removeAttribute("href");
```

O `<a>` deixa de funcionar como link.

## 7️⃣ Eventos no DOM
Eventos são ações do usuário:
- Clique
- Teclado
- Mouse 
- Carregamento

### 🔹 Como usa o Evento addEventListener

```js

botao.addEventListener("click", function() {
  console.log("Botão clicado")
});
```

## 8️⃣ event e currentTarget

```js
botao.addEventListener("click", function(event) {
  console.log(event.currentTarget)
})

```

- `event` → informações do evento
- `currentTarget` → elemento que recebeu o evento

→ Muito usado quando **vários elementos** compartilham evento.

## 9️⃣ Criar, remover e alterar elementos

### 🔹 Criar elemento

```js
const p = document.createElement("p");
p.textContent = "Nova parágrafo";
document.body.appendChild(p)
```

### 🔹 Remover elemento

```js
p.remove();
```

### 🔹 Alterar classe

```js
p.classList.add("ativo")
p.classList.remove("ativo")
p.classList.toggle("ativo")
```