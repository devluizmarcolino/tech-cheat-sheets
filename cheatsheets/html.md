# HTML Cheat Sheet

Este cheat sheet traz uma referência rápida para HTML com tags essenciais, boas práticas e exemplos práticos.

## 🔗 Estrutura Básica
```html
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Título da Página</title>
  </head>
  <body>
    <h1>Bem-vindo ao Cheat Sheet de HTML!</h1>
  </body>
</html>
```

---

## ✨ Tags Comuns

### **Títulos**
```html
<h1>Título Principal</h1>
<h2>Subtítulo</h2>
<h3>Seção Menor</h3>
```

### **Parágrafos e Texto**
```html
<p>Este é um parágrafo.</p>
<strong>Texto em negrito</strong> e <em>texto em itálico</em>
```

### **Listas**
#### Lista Ordenada
```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
```
#### Lista Não Ordenada
```html
<ul>
  <li>Item A</li>
  <li>Item B</li>
</ul>
```

### **Links e Imagens**
```html
<a href="https://exemplo.com">Visite o Exemplo</a>
<img src="imagem.jpg" alt="Descrição da Imagem">
```

### **Tabelas**
```html
<table>
  <thead>
    <tr>
      <th>Coluna 1</th>
      <th>Coluna 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Dado 1</td>
      <td>Dado 2</td>
    </tr>
  </tbody>
</table>
```

### **Formulários**
```html
<form action="/enviar" method="POST">
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome">

  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <button type="submit">Enviar</button>
</form>
```

---

## 🌱 Tags Semânticas
As tags semânticas ajudam a dar significado ao conteúdo da página, tornando-a mais acessível e fácil de entender.

### **Principais Tags Semânticas**
| Tag        | Descrição                          |
|------------|----------------------------------------|
| `<header>` | Cabeçalho da página ou seção        |
| `<nav>`    | Navegação principal                  |
| `<main>`   | Conteúdo principal da página        |
| `<article>`| Conteúdo independente, como artigos   |
| `<section>`| Agrupação de conteúdo relacionado    |
| `<aside>`  | Conteúdo complementar ou lateral      |
| `<footer>` | Rodapé da página ou seção         |

### **Exemplo de Uso:**
```html
<header>
  <nav>
    <ul>
      <li><a href="#">Início</a></li>
      <li><a href="#">Sobre</a></li>
    </ul>
  </nav>
</header>
<main>
  <article>
    <h2>Título do Artigo</h2>
    <p>Conteúdo interessante aqui.</p>
  </article>
</main>
<footer>
  <p>&copy; 2025 Sua Empresa</p>
</footer>
```

---

## 🔧 Boas Práticas
1. Sempre defina o **DOCTYPE** para garantir a compatibilidade com navegadores modernos.
2. Use **tags semânticas** como `<header>`, `<footer>`, `<article>` para uma estrutura clara.
3. Inclua o atributo **alt** em imagens para acessibilidade.
4. Sempre configure o **meta viewport** para design responsivo.

---

## ⭐ Dica Extra
Explore elementos semânticos modernos:
```html
<header>
  <nav>
    <ul>
      <li><a href="#">Início</a></li>
      <li><a href="#">Sobre</a></li>
    </ul>
  </nav>
</header>
<main>
  <article>
    <h2>Título do Artigo</h2>
    <p>Conteúdo interessante aqui.</p>
  </article>
</main>
<footer>
  <p>&copy; 2025 Sua Empresa</p>
</footer>
```
