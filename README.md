# React Props: Uma Introdução

## 🌟 O que são Props?

**Props**, abreviação de "propriedades", são uma maneira de passar dados de um componente pai para um componente filho no React. Ao usar props, você pode alimentar diferentes informações para o mesmo componente, tornando-o reutilizável e dinâmico sem a necessidade de alterar o código interno do componente.

## 🚀 Para o que elas servem?

- **Reutilização de Componentes:** As props permitem que você utilize um único componente em várias situações, adaptando seus valores e dados conforme for necessário.
- **Comunicação entre Componentes:** Elas estabelecem uma ponte de comunicação, onde um componente pai pode enviar informações para um componente filho.

## 🧠 Como elas funcionam?

### Passando Props

Você passa props para um componente assim como define atributos em elementos HTML:

```javascript
<MeuComponente propriedade="valor" />
```

## Acessando Props em Componentes de Função

Dentro do componente de função, você acessa as props diretamente através do argumento. Por exemplo:

```javascript
export default function MeuComponente(props) {
    return <h1>{props.propriedade}</h1>;
}
```

Ou usando a desestruturação (forma mais fácil):



```javascript
export default function MeuComponente({ propriedade }) {
    return <h1>{propriedade}</h1>;
}
```

E para usar as props devemos importar no App.jsx e colocar o valor que ela irá receber:

```javascript
export default function App() {
    return (
        <>
            <MeuComponente propriedade="espetinho" />
        </>
    );
}
```
Dessa forma, a informação "espetinho" será mostrada no ```<h1></h1>``` dentro de MeuComponente.

# 🎓 Prática em aula

- Projeto de componentes - Fazer uma página com algum tema (cinema,comida, jogos...) utilizando props para que os alunos consigam entender seu funcionamento na prática, criando um único componente apenas, esse componente irá receber os valores através das props exemplo: <a href="https://codesandbox.io/s/inspiring-hugle-ntcv57?file=/src/App.js">Código Componente com Props</a>