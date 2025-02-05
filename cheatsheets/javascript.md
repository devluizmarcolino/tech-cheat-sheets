# JavaScript Cheat Sheet 

Este cheat sheet traz uma referência rápida para JavaScript com tags essenciais, boas práticas e exemplos práticos.

## Fundamentos Básicos

### Variáveis
```javascript
// Três formas de declarar variáveis
var idade = 25;        // Escopo de função, pode ser redeclarada
let nome = "João";     // Escopo de bloco, não pode ser redeclarada
const PI = 3.14159;    // Constante, não pode ser modificada
```

**Explicação para Bebês:**
- `var`: É como um brinquedo velho que você pode trocar a qualquer momento;
- `let`: É como um brinquedo novo que você cuida com mais cuidado;
- `const`: É como um brinquedo especial que nunca pode ser mudado.

---

### Tipos de Dados
```javascript
// Tipos Primitivos
let numero = 42;           // Number
let texto = "Olá mundo";   // String
let verdadeiro = true;     // Boolean
let nulo = null;           // Null
let indefinido = undefined;// Undefined

// Tipos Complexos
let lista = [1, 2, 3];     // Array
let objeto = {             // Object
    nome: "Maria",
    idade: 30
};
```

### Operadores
```javascript
// Matemáticos
let soma = 5 + 3;          // 8
let subtracao = 10 - 4;    // 6
let multiplicacao = 3 * 4; // 12
let divisao = 15 / 3;      // 5

// Comparação
let igual = (5 == "5");    // true (compara valor)
let estritamenteIgual = (5 === "5"); // false (compara valor e tipo)
```

---

## Estruturas de Controle

### Condicionais
```javascript
// If-Else
if (idade >= 18) {
    console.log("Adulto");
} else {
    console.log("Menor");
}

// Switch
switch (diaDaSemana) {
    case "Segunda":
        console.log("Início da semana");
        break;
    case "Sexta":
        console.log("Quase fim de semana");
        break;
    default:
        console.log("Dia normal");
}
```

### Loops
```javascript
// For tradicional
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// For...of (Arrays)
let frutas = ["maçã", "banana", "laranja"];
for (let fruta of frutas) {
    console.log(fruta);
}

// For...in (Objetos)
let pessoa = {nome: "João", idade: 25};
for (let propriedade in pessoa) {
    console.log(propriedade + ": " + pessoa[propriedade]);
}
```

---

## Funções

### Declarações
```javascript
// Função tradicional
function somar(a, b) {
    return a + b;
}

// Arrow Function
const multiplicar = (a, b) => a * b;

// Função com parâmetro padrão
function saudacao(nome = "Visitante") {
    return `Olá, ${nome}!`;
}
```

## Manipulação de Arrays

### Métodos Essenciais
```javascript
let numeros = [1, 2, 3, 4, 5];

// Adicionar/Remover
numeros.push(6);       // Adiciona no final
numeros.pop();         // Remove do final

// Transformação
let dobrado = numeros.map(x => x * 2);
let filtrado = numeros.filter(x => x > 3);
```

---

## Programação Assíncrona

### Promises
```javascript
// Forma básica
function buscarDados() {
    return new Promise((resolve, reject) => {
        // Simulando busca de dados
        let sucesso = true;
        if (sucesso) {
            resolve("Dados carregados");
        } else {
            reject("Erro na busca");
        }
    });
}

// Usando async/await
async function exemplo() {
    try {
        let resultado = await buscarDados();
        console.log(resultado);
    } catch (erro) {
        console.error(erro);
    }
}
```

---

## Links Úteis 🌐

### Documentação e Aprendizado
- [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
- [JavaScript.info](https://javascript.info/)
- [W3Schools JavaScript](https://www.w3schools.com/js/)
- [FreeCodeCamp](https://www.freecodecamp.org/)

### Comunidades
- [Stack Overflow](https://stackoverflow.com/questions/tagged/javascript)
- [Dev.to JavaScript](https://dev.to/t/javascript)

---

## Boas Práticas

### Dicas de Estilo
- Use `camelCase` para variáveis e funções
- Evite variáveis globais
- Use `const` por padrão
- Prefira arrow functions
- Use template literals para strings complexas

## Frameworks e Bibliotecas
- React
- Vue.js
- Angular
- Node.js
- Express.js

## Ferramentas de Desenvolvimento
- Chrome DevTools
- VS Code
- ESLint
- Babel
- Webpack