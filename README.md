# Atividade Prática
Este projeto tem como objetivo repnder as questões da atividade.

## 1. Explique o que é JSON e por que ele se tornou tão popular para troca de dados entre aplicações.

>JSON **(JavaScript Object Notation)** é um formato leve de troca de dados, baseado em texto, que utiliza uma estrutura simples de pares chave-valor e listas ordenadas de valores. Ele é amplamente usado para transmitir informações entre aplicações, especialmente entre cliente e servidor na web.

- **Estrutura Basica**
>Um arquivo JSON é composto por:
>>- Objetos → delimitados por { }, contêm pares chave: valor.\
>>- Listas (arrays) → delimitadas por [ ], contêm uma sequência de valores.
>
>Exemplo:

```
{
  "nome": "Enthonielly",
  "idade": 19,
  "profissão": "Estudante"
}
```

- **Caracteristicas Principais**

> Baseado em texto: fácil de ler e escrever, tanto por humanos quanto por máquinas.
>
> Linguagem independente: embora derivado do JavaScript, pode ser usado em praticamente qualquer linguagem de programação (Python, Java, C#, PHP etc.).
>
> Estrutura simples e hierárquica: ideal para representar objetos e coleções de dados.

- **Por que o JSON se tornou tão popular?**

> Simplicidade: a sintaxe é curta e intuitiva — mais leve que XML, por exemplo.
>
> Integração com JavaScript: funciona nativamente em aplicações web (basta JSON.parse() e JSON.stringify() no JavaScript).
>
> Leveza e eficiência: ocupa menos espaço e requer menos processamento para leitura/escrita.
>
> Compatibilidade universal: quase todas as linguagens modernas têm bibliotecas para manipular JSON.
>
> Padrão de fato na web: APIs REST e serviços web usam JSON como formato principal de comunicação.


## 2. Qual a diferença fundamental entre JSON.stringify() e JSON.parse()? Dê um exemplo prático de quando usar cada um.

As funções **JSON.stringify()** e **JSON.parse()** são opostas complementares — uma converte objetos em texto JSON, e a outra faz o caminho inverso, transformando esse texto novamente em um objeto JavaScript.

| **Função** | **O que faz** | **Entrada** | **Saída** |
|--------|-----------|---------|-------|
| JSON.stringify() | Converte um objeto JavaScript em uma string JSON | Objeto | String JSON | 
| JSON.parse() | Converte uma string JSON em um objeto JavaScript | String JSON | Objeto |

- Exemplo:
  
````
// Objeto JavaScript
const usuario = {
  nome: "Enthonielly",
  idade: 19,
  profissão : "Estudante"
};

// Converter o objeto em texto JSON antes de salvar
localStorage.setItem("usuario", JSON.stringify(usuario));

// Recuperar o texto e transformá-lo de volta em objeto
const dados = JSON.parse(localStorage.getItem("usuario"));

console.log(dados.nome);
// Saída: "Enthonielly"
````
- Analogia Simples
>stringify() empacota o objeto para transporte;
>
>parse() desempacota quando ele chega.

## 3. Considerando a string "JavaScript é baseada em ECMA Script", quais métodos você usaria para:
- **Verificar se contém a palavra "Script";**
- **Remover a palavra "JavaScript" e gerar uma nova string;**
- **Substituir "baseada" por "tem origem"**

````
const texto = "JavaScript é baseada em ECMA Script";
````

- Verificar se contém a palavra "Script"

Você pode usar o método includes(), que retorna true ou false.

````
texto.includes("Script"); 
// Retorna: true
````
> **Alternativa**
>>texto.indexOf("Script") !== -1 (forma mais antiga)
>>
>>texto.match(/Script/) (usando expressão regular)

- Remover a palavra "JavaScript" e gerar uma nova string

Use o método replace(), substituindo "JavaScript" por uma string vazia.

````
const novoTexto = texto.replace("JavaScript", "");
console.log(novoTexto);
// Saída: " é baseada em ECMA Script"
````
> Dica: Se a palavra aparecer mais de uma vez e quiser remover todas, use expressão regular com o modificador g:
> ````
> texto.replace(/JavaScript/g, "");
> ````

- Substituir "baseada" por "tem origem"
Mais uma vez, usamos replace():

````
const alterado = texto.replace("baseada", "tem origem");
console.log(alterado);
// Saída: "JavaScript é tem origem em ECMA Script"
````

**Resumo Geral**
| Tarefa| Método | Exemplo | Resutado |
|-------|-------|-------|-------|
| Verificar se contém "Script" | includes() | texto.includes("Script") | true |
| Remover "JavaScript" | replace("JavaScript", "") | "é baseada em ECMA Script" |  |
| Substituir "baseada" por "tem origem" | replace("baseada", "tem origem") | "JavaScript é tem origem em ECMA Script" |  |

## 4. Qual a vantagem de usar template strings (`) em vez de concatenação com + para criar strings complexas
As template strings (também chamadas de template literals) foram introduzidas no ES6 (ECMAScript 2015) e trouxeram uma forma muito mais simples, legível e poderosa de criar strings dinâmicas em JavaScript.

- **Diferença principal**

Forma antiga — concatenação com +:
````
const nome = "Enthonielly";
const idade = 19;

const mensagem = "Olá, meu nome é " + nome + " e eu tenho " + idade + " anos.";
console.log(mensagem);
// "Olá, meu nome é Enthonielly e eu tenho 19 anos."
````
Forma moderna — template string:
````
const nome = "Enthonielly";
const idade = 25;

const mensagem = `Olá, meu nome é ${nome} e eu tenho ${idade} anos.`;
console.log(mensagem);
// "Olá, meu nome é Enthonielly e eu tenho 25 anos."
````
- **Vantagens das template strings**
> **1.** Sintaxe mais limpa e legível
>> - Evita excesso de + e aspas, tornando o código mais fácil de entender.
>
> **2.** Interpolação direta de variáveis e expressões
>> - Você pode inserir variáveis e até operações:
>> ````
>> `Ano que vem terei ${idade + 1} anos.`
>> ````
>
> **3.** Suporte a múltiplas linhas
>> - Pode quebrar a string sem usar \n:
>> ````
>> const texto = `
>> Nome: ${nome}
>> Idade: ${idade}
>> `;
>> ````
>
> **4.** Menos erros de concatenação
>> -Evita confusões com espaços e aspas, comuns em concatenação com +.
>
> **5.** Melhor manutenção
>> -Facilita editar textos longos, especialmente em mensagens ou HTML dinâmico.

Em Resumo.
| Método | Características |
|-----|-----|
| Concatenação (+) | Verboso, fácil de errar com espaços/aspas |
|Template string (``) | Simples, legível, suporta variáveis, expressões e múltiplas linhas |




