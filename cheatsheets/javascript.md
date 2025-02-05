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

**Explicação Detalhada dos Operadores**:

#### Operadores Matemáticos
- **O que acontece**: 
  - Realiza operações matemáticas básicas
  - Segue ordem matemática tradicional
  - Permite cálculos simples entre números
- **Exemplos de Uso**:
  - `5 + 3` resulta em `8`
  - `10 - 4` resulta em `6`
  - `3 * 4` resulta em `12`
  - `15 / 3` resulta em `5`

#### Operadores de Comparação
- **O que acontece**:
  - `==` compara apenas o valor, fazendo conversão de tipo
  - `===` compara valor e tipo, sem conversão
  - Útil para validações precisas
- **Comportamento**:
  - `5 == "5"` retorna `true` (compara valor)
  - `5 === "5"` retorna `false` (compara valor e tipo)

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

**Explicação Detalhada das Condicionais**:

#### If-Else
- **O que acontece**:
  - Testa uma condição específica
  - Executa código baseado no resultado da condição
  - Permite criar fluxos de decisão
- **Exemplo**:
  - Se a idade for maior ou igual a 18, mostra "Adulto"
  - Caso contrário, mostra "Menor"

#### Switch
- **O que acontece**:
  - Compara um valor contra múltiplos casos possíveis
  - Executa código específico para cada caso
  - `break` impede execução dos próximos casos
  - `default` captura situações não especificadas previamente
- **Comportamento**:
  - Para "Segunda": mostra "Início da semana"
  - Para "Sexta": mostra "Quase fim de semana"
  - Para outros dias: mostra "Dia normal"

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

**Explicação Detalhada dos Loops**:

#### For Tradicional
- **O que acontece**:
  - Executa bloco de código número definido de vezes
  - `i = 0`: Começa no zero
  - `i < 5`: Continua enquanto menor que 5
  - `i++`: Incrementa 1 a cada iteração
- **Resultado Esperado**:
  - Imprime números: 0, 1, 2, 3, 4

#### For...of (Arrays)
- **O que acontece**:
  - Percorre todos elementos de um array
  - Captura valor de cada elemento
  - Simplicidade na iteração
- **Resultado Esperado**:
  - Imprime: "maçã", "banana", "laranja"

#### For...in (Objetos)
- **O que acontece**:
  - Percorre todas propriedades de um objeto
  - Permite acessar chaves e valores
  - Útil para explorar estruturas de dados
- **Resultado Esperado**:
  - Imprime: "nome: João", "idade: 25"

## Funções: Blocos de Código Reutilizáveis

```javascript
// Função tradicional
function somar(a, b) {
    return a + b;  // Resultado: soma de a + b
}

// Arrow Function
const multiplicar = (a, b) => a * b;  // Multiplica a * b

// Função com parâmetro padrão
function saudacao(nome = "Visitante") {
    return `Olá, ${nome}!`;  // Resultado: "Olá, [nome]!"
}
```

**Explicação Detalhada das Funções**:

#### Função Tradicional
- **O que acontece**:
  - Cria bloco de código reutilizável
  - Recebe parâmetros de entrada
  - Retorna um resultado específico
- **Exemplo**:
  - `somar(2, 3)` retorna `5`

#### Arrow Function
- **O que acontece**:
  - Sintaxe compacta para funções
  - Mantém a mesma lógica de funções tradicionais
  - Ideal para funções curtas
- **Exemplo**:
  - `multiplicar(4, 5)` retorna `20`

#### Função com Parâmetro Padrão
- **O que acontece**:
  - Define valor padrão se nenhum argumento for passado
  - Aumenta flexibilidade da função
- **Comportamento**:
  - `saudacao()` retorna "Olá, Visitante!"
  - `saudacao("Maria")` retorna "Olá, Maria!"

## Manipulação de Arrays

```javascript
let numeros = [1, 2, 3, 4, 5];

numeros.push(6);       // Adiciona 6, resultado: [1,2,3,4,5,6]
numeros.pop();         // Remove último, resultado: [1,2,3,4,5]

let dobrado = numeros.map(x => x * 2);  
// Resultado: [2,4,6,8,10]

let filtrado = numeros.filter(x => x > 3);  
// Resultado: [4,5]
```

**Explicação Detalhada de Manipulação de Arrays**:

#### Métodos Básicos
- **`push()`**:
  - Adiciona elemento no final do array
  - Aumenta o tamanho do array

- **`pop()`**:
  - Remove o último elemento do array
  - Reduz o tamanho do array

#### Métodos Avançados
- **`map()`**:
  - Transforma cada elemento do array
  - Cria novo array com resultados
  - Não modifica array original

- **`filter()`**:
  - Cria novo array com elementos que passam no teste
  - Mantém apenas elementos que atendem condição específica

## Programação Assíncrona

```javascript
// Promise simula operação que leva tempo
function buscarDados() {
    return new Promise((resolve, reject) => {
        let sucesso = true;
        if (sucesso) {
            resolve("Dados carregados");  // Caso sucesso
        } else {
            reject("Erro na busca");      // Caso falha
        }
    });
}

// Async/Await simplifica tratamento
async function exemplo() {
    try {
        let resultado = await buscarDados();
        console.log(resultado);  // "Dados carregados"
    } catch (erro) {
        console.error(erro);     // Tratamento de erro
    }
}
```

**Explicação Detalhada de Programação Assíncrona**:

#### Promises
- **O que são**:
  - Representam valor futuro de operação assíncrona
  - Podem estar pendente, resolvida ou rejeitada
- **Estados**:
  - `resolve`: Operação concluída com sucesso
  - `reject`: Operação falhou

#### Async/Await
- **O que acontece**:
  - Simplifica trabalho com Promises
  - Torna código assíncrono mais síncrono
  - Facilita tratamento de erros
- **Comportamento**:
  - `await`: Pausa execução até Promise ser resolvida
  - `try/catch`: Captura erros de forma elegante

## Links Úteis 🌐

### Documentação e Aprendizado
- [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
- [JavaScript.info](https://javascript.info/)
- [W3Schools JavaScript](https://www.w3schools.com/js/)
- [FreeCodeCamp](https://www.freecodecamp.org/)

### Comunidades
- [Stack Overflow](https://stackoverflow.com/questions/tagged/javascript)
- [Dev.to JavaScript](https://dev.to/t/javascript)

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