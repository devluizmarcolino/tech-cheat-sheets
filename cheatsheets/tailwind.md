# Tailwind CSS Cheat Sheet

Este cheat sheet traz uma referência rápida ao Tailwind CSS com classes essenciais, boas práticas e exemplos práticos.

---

## 📌 Instalação

### Usando npm
```sh
npm install -D tailwindcss
npx tailwindcss init
```

### CDN (Apenas para testes)
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@3.0.0/dist/tailwind.min.css" rel="stylesheet">
```

📌 **Dica:** Se você estiver criando um projeto real, prefira a instalação via npm para maior controle e personalização.

---

## 🎨 Estrutura Básica

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.tailwindcss.com"></script>
  <title>Tailwind CSS</title>
</head>
<body class="bg-gray-100 p-4">
  <h1 class="text-3xl font-bold text-blue-600">Hello, Tailwind!</h1>
</body>
</html>
```

📌 **Dica:** Use `class="bg-gray-100"` para definir o fundo cinza claro e `p-4` para adicionar um espaçamento interno.

---

## 📏 Layout

### Containers
```html
<div class="container mx-auto px-4">Conteúdo</div>
```
📌 **Dica:** `container` define uma largura máxima e `mx-auto` centraliza horizontalmente.

### Flexbox
```html
<div class="flex justify-center items-center h-screen bg-gray-200">
  <p class="text-lg">Centralizado</p>
</div>
```
📌 **Dica:** `flex` ativa o Flexbox, `justify-center` centraliza horizontalmente e `items-center` centraliza verticalmente.

### Grid
```html
<div class="grid grid-cols-3 gap-4">
  <div class="bg-blue-200 p-4">1</div>
  <div class="bg-blue-300 p-4">2</div>
  <div class="bg-blue-400 p-4">3</div>
</div>
```
📌 **Dica:** `grid-cols-3` cria três colunas e `gap-4` adiciona espaçamento entre elas.

---

## 🎨 Cores e Estilos

### Cores de fundo
```html
<div class="bg-red-500 text-white p-4">Vermelho</div>
```
📌 **Dica:** O Tailwind usa uma paleta de cores baseada em escalas numéricas (`100` a `900`).

### Texto
```html
<p class="text-xl font-semibold text-gray-800">Texto grande e escuro</p>
```
📌 **Dica:** `text-xl` aumenta o tamanho do texto e `font-semibold` o torna semi-negrito.

### Bordas e Sombras
```html
<div class="border border-gray-400 shadow-lg p-4 rounded-lg">
  Com borda, sombra e cantos arredondados
</div>
```
📌 **Dica:** `rounded-lg` suaviza os cantos e `shadow-lg` adiciona uma sombra pronunciada.

---

## 📱 Responsividade

```html
<div class="text-base sm:text-lg md:text-xl lg:text-2xl xl:text-3xl">
  Texto responsivo
</div>
```
📌 **Dica:** O Tailwind usa prefixos como `sm:`, `md:`, `lg:`, `xl:` para diferentes tamanhos de tela.

---

## 📋 Outras Classes Úteis

### Espaçamentos
```html
<div class="m-4 p-4">Margem e padding de 4 unidades</div>
```
📌 **Dica:** `m-4` adiciona margem externa e `p-4` adiciona padding interno.

### Largura e Altura
```html
<div class="w-1/2 h-32 bg-blue-500">Metade da largura e altura fixa</div>
```
📌 **Dica:** `w-1/2` define a largura como 50% do contêiner pai.

### Botão Personalizado
```html
<button class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded">
  Clique Aqui
</button>
```
📌 **Dica:** `hover:bg-green-700` muda a cor ao passar o mouse.

---

## 🔗 Links de Referência
- [Tailwind CSS Oficial](https://tailwindcss.com/)
- [Configuração Tailwind](https://tailwindcss.com/docs/installation)
- [Playground Online](https://play.tailwindcss.com/)
