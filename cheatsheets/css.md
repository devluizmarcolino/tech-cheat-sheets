# CSS Cheat Sheet

Este cheat sheet traz uma referência rápida para CSS com tags essenciais, boas práticas e exemplos práticos.

---

## Seletores Básicos

### Seletores Elementares
- `*`: Seleciona todos os elementos
- `div`: Seleciona todos os elementos `<div>`
- `.classe`: Seleciona elementos com uma classe específica
- `#id`: Seleciona um elemento com um ID específico

### Seletores Combinadores
- `div p`: Seleciona parágrafos dentro de divs
- `div > p`: Seleciona parágrafos filhos diretos de divs
- `div + p`: Seleciona parágrafos imediatamente após divs
- `div ~ p`: Seleciona parágrafos que são irmãos de divs

## Propriedades Fundamentais

### Box Model
```css
.elemento {
    width: 200px;
    height: 100px;
    padding: 10px;
    margin: 15px;
    border: 2px solid black;
    box-sizing: border-box; /* Inclui padding e border no tamanho total */
}
```

### Cores e Fundos
```css
.elemento {
    color: #333;
    background-color: rgba(255, 0, 0, 0.5);
    background-image: url('imagem.jpg');
    background-size: cover;
    background-repeat: no-repeat;
}
```

## Layout Moderno

### Flexbox
```css
.container {
    display: flex;
    flex-direction: row; /* row | column | row-reverse | column-reverse */
    justify-content: space-between; /* Alinhamento horizontal */
    align-items: center; /* Alinhamento vertical */
    gap: 10px; /* Espaço entre itens */
}
```

#### Flex Item Properties
- `flex-grow`: Proporção de crescimento
- `flex-shrink`: Proporção de redução
- `flex-basis`: Tamanho inicial do item

### CSS Grid
```css
.grid-container {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr; /* Colunas proporcionais */
    grid-template-rows: 100px 200px;
    gap: 15px;
}

.grid-item {
    grid-column: span 2; /* Ocupar duas colunas */
    grid-row: 1 / 3; /* Da linha 1 até a 3 */
}
```

## Responsividade

### Media Queries
```css
/* Telas menores que 600px */
@media screen and (max-width: 600px) {
    .elemento {
        flex-direction: column;
        width: 100%;
    }
}
```

## Boas Práticas

### Dicas de Estilo
- Use variáveis CSS para cores e dimensões recorrentes
- Priorize unidades relativas (`rem`, `%`) sobre absolutas (`px`)
- Utilize `box-sizing: border-box` globalmente
- Minimize a especificidade dos seletores

### Variáveis CSS
```css
:root {
    --cor-primaria: #3498db;
    --espacamento-padrao: 1rem;
}

.elemento {
    background-color: var(--cor-primaria);
    margin: var(--espacamento-padrao);
}
```

## Truques Úteis

### Reset CSS Moderno
```css
*, *::before, *::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
**Motivo**: 
- Elimina margens e paddings padrão dos navegadores
- Garante que o tamanho total do elemento inclua padding e border
- Cria uma base consistente para estilização em diferentes navegadores

### Centralização Perfeita
```css
.centralizado {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
```
**Motivo**:
- Flexbox oferece método simples de centralização
- Funciona para elementos de qualquer tamanho
- `height: 100vh` centraliza verticalmente na tela inteira

## Animações
```css
@keyframes slideIn {
    from { transform: translateX(-100%); }
    to { transform: translateX(0); }
}

.elemento {
    animation: slideIn 0.5s ease-in-out;
}
```

## Performance
- Minimize reflows e repaints
- Use `transform` e `opacity` para animações
- Evite seletores muito específicos
- Use `will-change` com moderação

## Ferramentas e Debugging

### Ferramentas de Desenvolvimento
- **Chrome DevTools**: 
  - Inspecionar e modificar estilos em tempo real
  - Verificar layout, box model e responsividade
  - Analisar performance de renderização

- **Firefox Developer Tools**:
  - Grid e Flexbox inspector
  - Ferramentas de animação
  - Análise de layout 3D

### Frameworks CSS
- Tailwind CSS: Utility-first
- Bootstrap: Sistema de grid responsivo
- Bulma: Flexbox-based

### Pré-processadores
- Sass
- Less
- Stylus

### Validadores
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/): Verifica a validade do seu código CSS
- [CSS Lint](http://csslint.net/): Ferramenta de análise de qualidade do código

### Ferramentas de Otimização
- PurgeCSS: Remove CSS não utilizado
- PostCSS: Transformações de CSS com JavaScript
- Critical: Extrai CSS crítico para carregamento inicial

### Recursos Online
- [CSS-Tricks](https://css-tricks.com/)
- [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
- [CodePen](https://codepen.io/) para experimentação