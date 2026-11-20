# Declaração de uso de IA – Grupo SONDER

Nós, do grupo **SONDER**, desenvolvemos o **Projeto RAIZ** na Global Solution 2026 da FIAP (tema CitizenTech). Durante o trabalho, usamos a inteligência artificial (Claude) como **ferramenta de estudo**, principalmente para tirar dúvidas e treinar. Este documento explica como isso aconteceu.

## Sobre o projeto

O RAIZ é um sensor de umidade do solo para pequenos produtores de hortaliça folhosa do cinturão verde da Região Metropolitana de São Paulo, com um app que projeta em quantas horas será preciso irrigar. O projeto se conecta às ODS 2, 9, 10 e 13.

A solução foi dividida em sete entregas (Matemática, UX, Edge/Wokwi, Python CLI, Front-end, Web Dev/JS e Pitch em vídeo), apresentadas como um único projeto.

## Como estudamos com a IA

Quando travávamos em algum assunto, usávamos a IA para estudar. O caminho foi quase sempre este:

1. Pedíamos uma explicação simples do conceito.
2. Víamos um exemplo pequeno.
3. Fazíamos exercícios de treino.
4. Tentávamos resolver por conta própria.
5. Respondíamos às perguntas que ajudavam a achar o erro.
6. Corrigíamos o código e entendíamos por que ele estava errado.

Assim, a IA serviu como apoio para aprender. O código do projeto foi montado, testado e ajustado por nós.

## Uso por entrega

| Entrega | Como usamos a IA | O que foi feito por nós |
| --- | --- | --- |
| Front-end (landing page, CSS) | Aprender conceitos de CSS e pedir pequenas linhas de código como referência | Estrutura da página, adaptação ao visual do projeto e testes no navegador |
| Web Dev (JavaScript) | Treinar a lógica de programação e tirar dúvidas sobre as linhas do formulário de feedback e do carrossel | Escrita da função, testes e correção das linhas |
| MVP simulado (app) | Gerar o protótipo do aplicativo a partir das nossas instruções, declarado como feito por IA | Definição das telas, identidade visual, critérios de acessibilidade, mascotes, testes e publicação |
| Python (CLI) | Tirar dúvidas sobre os conceitos vistos em aula, como `def` e `match/case` | Montagem do programa e resolução dos exercícios da disciplina |

## CSS: o que aprendemos e aplicamos

Aprendemos CSS com a IA e aplicamos os conceitos na landing page, ajustando tudo ao visual do RAIZ. A tabela mostra o que usamos e onde aparece no código.

| Conceito | Onde aparece | O que aprendemos |
| --- | --- | --- |
| Variáveis CSS (`:root`) | Paleta de verdes, fontes e espaçamentos | Mudar uma cor ou medida em um só lugar atualiza o site todo |
| Flexbox | Menu, destaque, seções e rodapé | Alinhar e distribuir elementos em linha ou em coluna |
| `row-reverse` com `nth-of-type(even)` | Seções que alternam ícone e texto | Inverter a ordem visual sem mexer no HTML |
| `clamp()` e `min()` | Título principal e largura do container | Tamanhos que se adaptam à tela sem várias regras |
| `position: sticky` | Cabeçalho fixo no topo | Manter a navegação sempre visível |
| `@media` (820px e 600px) | Menu, destaque e seções no celular | Reorganizar o layout em telas menores |
| `:focus-visible` | Links, botão e campos usados pelo teclado | Deixar o foco visível, pensando em acessibilidade |
| `transition` e `:hover` | Botões e links do menu | Dar retorno visual ao passar o mouse |

## JavaScript: formulário de feedback e carrossel

No JavaScript, treinamos a lógica de programação com perguntas e exercícios e depois corrigimos as linhas que precisavam de ajuste. O resultado é a função `enviarFeedback()`, em `js/script.js`, que roda quando a pessoa envia o formulário, além das funções `updateCarousel()`, `nextSlide()`, `prevSlide()` e `resetAutoPlay()` que estão em `js/carousel.js`.

O que entendemos de cada parte:

- `getElementById(...).value.trim()` lê o campo e tira os espaços das pontas, para que só espaços não contem como texto.
- O `if` com `||` confere se algum campo ficou vazio.
- O `return` dentro do `if` interrompe a função, então o agradecimento não aparece com campos vazios.
- O `alert` final usa o nome digitado para personalizar a resposta.
- O `reset()` limpa o formulário depois do envio.
- O `setInterval()` define que uma função seja repetida em um intervalo definido em milisegundos.

## Acessibilidade: seção "Quatro caminhos para a mesma informação"

O briefing pede para considerar quem pode ter dificuldade para acessar a solução. Como parte de quem planta é analfabeta ou lê com dificuldade, o grupo decidiu o conteúdo da seção: quatro caminhos que existem ao mesmo tempo (interface facilitada, dados por voz, mascote interativo e suporte por equipe). As ilustrações do mascote, com as cinco expressões do estado do solo, foram feitas por nós.

Usamos a IA para tirar dúvidas sobre como deixar a seção acessível e para revisar o HTML e o CSS. A tabela mostra o que aplicamos.

| Critério | Como aplicamos | O que aprendemos |
| --- | --- | --- |
| Texto alternativo (`alt` e `aria-label`) | Cada ícone e cada expressão do mascote | Descrever o que a imagem mostra, e não escrever só "ícone" |
| Contraste | Texto na cor `--texto` e ícones em `--verde-escuro` sobre `--verde-claro` | O texto precisa de contraste mínimo de 4.5:1 e os ícones, de 3:1 |
| Informação além da cor | Cada expressão do mascote tem legenda escrita | Quem não enxerga bem a cor ainda entende o estado do solo |
| Tamanho do texto | Nenhum texto da seção abaixo de 15 px | Texto pequeno demais atrapalha quem lê com dificuldade |
| `:focus-visible` | Links, botão e campos do formulário | Quem usa o teclado precisa ver onde está o foco |
| Ordem de leitura | A ordem do HTML segue a ordem que aparece na tela | Leitores de tela leem na ordem do código |
| CSS Grid com `auto-fit` | Cartões em 2×2 que viram 1 coluna e mascotes que quebram linha | Organizar em grade sem que os textos se sobreponham |

## MVP simulado do aplicativo

Diferente do resto do projeto, o MVP simulado (pasta `app/`) foi **gerado com inteligência artificial**, e isso está escrito no próprio protótipo: uma faixa no topo e no rodapé de todas as telas avisa que ele é um protótipo gerado por IA, com dados fictícios.

O que foi feito pelo grupo:

- Definimos as telas (Início, Canteiros, Histórico e Ajuda) e o que cada uma precisava mostrar.
- Escrevemos as instruções para a IA com a identidade visual do RAIZ (paleta, fontes, cartões e botões) para o app seguir o mesmo visual da landing page.
- Exigimos os mesmos critérios de acessibilidade da seção "Quatro caminhos para a mesma informação": número grande, alvo de toque de 44 px, leitura por voz, mascote com legenda, contraste, foco visível e informação que não depende só de cor.
- Usamos as cinco expressões do mascote que nós desenhamos.
- Testamos as quatro telas, o botão "Simular nova leitura", a leitura por voz e o layout no celular e no computador.
- Publicamos o site e o app na Vercel e ligamos um ao outro: o botão "Ver o app" na landing page e o link "Voltar ao site" no app.

| Recurso do app | Para que serve |
| --- | --- |
| `speechSynthesis` (Web Speech API) | Ler a situação do solo em voz alta, em português |
| `<template>` com os mascotes | Trocar a expressão do mascote sem recarregar a página |
| `hidden` e `aria-selected` nas abas | Mostrar uma tela por vez e avisar o leitor de tela qual está aberta |
| `<details>` e `<summary>` | Esconder o gráfico técnico até a pessoa pedir |
| `prefers-reduced-motion` | Tirar animações para quem configurou isso no sistema |

## Nossa responsabilidade

- Só usamos um trecho depois de entender como ele funciona.
- Testamos o resultado no navegador e corrigimos o que não funcionou.
- Tratamos qualquer resposta da IA como sugestão, porque ela pode errar.
- As decisões do projeto (tema, solução, ODS e público) são do grupo.
- Respondemos pelo conteúdo final de todas as entregas.

## Considerações finais

Usamos a IA para aprender e tirar dúvidas de CSS, JavaScript e Python, e para gerar o MVP simulado do aplicativo, que está identificado como protótipo feito por IA. O projeto, as decisões, a landing page e o conteúdo são trabalho do grupo SONDER.

**Grupo SONDER** · Global Solution 2026 · FIAP
