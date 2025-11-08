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
  "idade": 25,
  "habilidades": ["Python", "JavaScript", "SQL"],
  "ativo": true
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













