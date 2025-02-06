# ⚛️ React Cheat Sheet

## 🚀 Introdução ao React

React é uma biblioteca JavaScript para criar interfaces de usuário interativas e reutilizáveis.

---

## 📥 Instalação

### 1️⃣ Criando um projeto React com Vite (Recomendado)
```sh
npm create vite@latest my-app --template react
cd my-app
npm install
npm run dev
```

### 2️⃣ Criando um projeto React com Create React App
```sh
npx create-react-app my-app
cd my-app
npm start
```

### 3️⃣ Adicionando React a um projeto existente
```sh
npm install react react-dom
```

---

## 📂 Estrutura de Arquivos

```
my-app/
├── src/
│   ├── components/
│   ├── App.jsx
│   ├── main.jsx
│   ├── index.css
├── public/
├── package.json
```

---

## 🏗️ Criando um Componente Simples
```jsx
function Welcome(props) {
  return <h1>Olá, {props.name}!</h1>;
}

export default Welcome;
```

### Usando o Componente
```jsx
import Welcome from "./Welcome";

function App() {
  return <Welcome name="João" />;
}

export default App;
```

---

## 🎯 Hooks Principais

### useState - Estado no React
```jsx
import { useState } from "react";

function Contador() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>Contagem: {count}</p>
      <button onClick={() => setCount(count + 1)}>Incrementar</button>
    </div>
  );
}
```

### useEffect - Efeitos colaterais
```jsx
import { useEffect, useState } from "react";

function App() {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/todos/1")
      .then(response => response.json())
      .then(json => setData(json));
  }, []);

  return <pre>{JSON.stringify(data, null, 2)}</pre>;
}
```

---

## 📡 Comunicação entre Componentes

### Props
```jsx
function Saudacao({ nome }) {
  return <h1>Olá, {nome}!</h1>;
}

function App() {
  return <Saudacao nome="Maria" />;
}
```

### Context API (Gerenciamento de Estado Global)
```jsx
import { createContext, useContext, useState } from "react";

const TemaContext = createContext();

function ProvedorTema({ children }) {
  const [tema, setTema] = useState("claro");
  return (
    <TemaContext.Provider value={{ tema, setTema }}>
      {children}
    </TemaContext.Provider>
  );
}

function BotaoTema() {
  const { tema, setTema } = useContext(TemaContext);
  return <button onClick={() => setTema(tema === "claro" ? "escuro" : "claro")}>Mudar Tema</button>;
}
```

---

## 🏗️ Estilização no React

### CSS Modules
```css
/* styles.module.css */
.botao {
  background-color: blue;
  color: white;
}
```
```jsx
import styles from "./styles.module.css";

function Botao() {
  return <button className={styles.botao}>Clique aqui</button>;
}
```

### Styled Components
```sh
npm install styled-components
```
```jsx
import styled from "styled-components";

const Botao = styled.button`
  background: blue;
  color: white;
`;

function App() {
  return <Botao>Styled Button</Botao>;
}
```

---

## 📖 Links de Referência
- [Documentação Oficial](https://react.dev/)
- [React Hooks](https://react.dev/reference/react)
- [Vite para React](https://vitejs.dev/guide/)
- [Styled Components](https://styled-components.com/)
