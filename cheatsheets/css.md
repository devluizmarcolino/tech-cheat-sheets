# CSS Cheat Sheet

Este cheat sheet traz uma referência rápida para CSS com tags essenciais, boas práticas e exemplos práticos.

---

## 🔗 Estrutura Básica
```html
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página com CSS</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>Olá, CSS!</h1>
  </body>
</html>
```
```css
/* styles.css */
body {
  font-family: 'Poppins', sans-serif;
  background-color: #f4f4f4;
  color: #333;
}
```

---

## 🛏 Seletor Básico
```css
h1 {
  color: #338da4;
  font-size: 2rem;
  text-align: center;
}
```
### Explicação
- `color`: Cor do texto.
- `font-size`: Tamanho da fonte.
- `text-align`: Alinhamento do texto.

---

## 🔧 Boas Práticas
1. **Mantenha o CSS Organizado:** Separe seletores por seções e comente onde necessário.
2. **Evite IDs:** Prefira classes para reutilização de estilos.
3. **Mobile First:** Comece pensando no design para telas menores.

Exemplo básico de responsividade:
```css
body {
  font-size: 16px;
}

@media (max-width: 768px) {
  body {
    font-size: 14px;
  }
}
```

---

## 💡 Truques Úteis
### Estilizar Links Apenas ao Passar o Mouse
```css
a:hover {
  text-decoration: underline;
  color: #569987;
}
```
### Centralizar Conteúdo com Flexbox
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```
### Efeitos Suaves com Transições
```css
button {
  background-color: #338da4;
  color: white;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #569987;
}
```
---

## 🌱 Propriedades Que Valem a Pena Decorar
- **margin:** Espaço externo ao redor do elemento.
- **padding:** Espaço interno dentro do elemento.
- **border:** Borda ao redor do elemento.
- **display:** Controla o layout (ex: `block`, `inline`, `flex`).
- **position:** Define o posicionamento (`static`, `absolute`, `fixed`, etc).

---

## ✨ Estrutura de Layout Simples
```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  display: grid;
  gap: 10px;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```
---

## ⭐ Dica Extra
Use variáveis CSS para padronizar seu design:
```css
:root {
  --cor-primaria: #338da4;
  --cor-secundaria: #569987;
  --espacamento-padrao: 16px;
}

body {
  background-color: var(--cor-primaria);
  color: white;
  padding: var(--espacamento-padrao);
}
```
---

Pronto para deixar seus projetos lindos? Fique à vontade para ajustar e experimentar!
