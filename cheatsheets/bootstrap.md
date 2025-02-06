# 📘 Bootstrap Cheat Sheet

## 🚀 Introdução ao Bootstrap

Bootstrap é um framework front-end que facilita o desenvolvimento de interfaces responsivas e modernas com HTML, CSS e JavaScript.

---

## 📥 Instalação

### 1️⃣ Usando CDN (Mais Fácil)
Adicione no `<head>` do seu HTML:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

### 2️⃣ Instalando via npm
```sh
npm install bootstrap
```
Depois, importe o Bootstrap no seu CSS ou JavaScript:
```css
@import 'bootstrap/dist/css/bootstrap.min.css';
```
```js
import 'bootstrap/dist/js/bootstrap.bundle.min';
```

### 3️⃣ Usando via arquivo local
Baixe os arquivos do [site oficial](https://getbootstrap.com/) e inclua no seu projeto.

---

## 📐 Layout e Grid System

Bootstrap usa um sistema de 12 colunas flexível para layout responsivo.

### Exemplo de Grid
```html
<div class="container">
  <div class="row">
    <div class="col-md-6 bg-primary text-white">Coluna 1</div>
    <div class="col-md-6 bg-secondary text-white">Coluna 2</div>
  </div>
</div>
```
📌 **Dica:** Use `col-md-6` para dividir o espaço em telas médias (≥768px).

### Classes de Grid Comuns
| Classe        | Descrição |
|--------------|------------|
| `.container` | Contêiner centralizado |
| `.row` | Linha flexível |
| `.col` | Coluna flexível |
| `.col-4` | Ocupa 4 das 12 colunas |
| `.col-md-6` | 6 colunas para telas médias (≥768px) |

---

## 🎨 Cores e Background

### Texto Colorido
```html
<p class="text-primary">Texto azul</p>
<p class="text-danger">Texto vermelho</p>
```

### Fundo Colorido
```html
<div class="bg-success text-white p-3">Fundo verde</div>
```
📌 **Dica:** Use `p-3` para adicionar espaçamento interno (padding).

---

## 🔘 Botões e Componentes

### Botões
```html
<button class="btn btn-primary">Botão Primário</button>
<button class="btn btn-danger">Botão de Alerta</button>
```

### Ícones (Usando Bootstrap Icons)
```html
<i class="bi bi-alarm"></i>
```
Adicione o CSS do Bootstrap Icons:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css">
```

---

## 📑 Formulários e Inputs

### Exemplo de Formulário
```html
<form>
  <div class="mb-3">
    <label class="form-label">Email</label>
    <input type="email" class="form-control" placeholder="Digite seu email">
  </div>
  <button class="btn btn-success">Enviar</button>
</form>
```
📌 **Dica:** Use `mb-3` para espaçamento entre os elementos.

---

## 📱 Responsividade e Breakpoints

Bootstrap possui breakpoints para diferentes tamanhos de tela:

| Breakpoint | Classe | Largura mínima |
|------------|---------|---------------|
| `sm` | `col-sm-*` | 576px |
| `md` | `col-md-*` | 768px |
| `lg` | `col-lg-*` | 992px |
| `xl` | `col-xl-*` | 1200px |

Exemplo de responsividade:
```html
<div class="col-sm-12 col-md-6 col-lg-4">Responsivo</div>
```

---

## 🔗 Links de Referência
- [Bootstrap Oficial](https://getbootstrap.com/)
- [Bootstrap CDN](https://www.bootstrapcdn.com/)
- [Bootstrap Icons](https://icons.getbootstrap.com/)
- [Documentação Grid](https://getbootstrap.com/docs/5.3/layout/grid/)
