# Projeto: Remake de aplicação web simples

Substitua a imagem ao lado por um GIF/WEBP animado mostrando seu projeto


## Acesso

Substitua este texto pela URL para acesso ao seu app publicado. Adicione a URL também na seção "About" do seu repositório no GitHub.


## Desenvolvedor(a)
Nome: Ricardo Facco Pigatto<br>
Curso: Sistemas de Informação


## App original

### Links

- Acesso: https://elc1090.github.io/demo-attendance-indexeddb/
- Repositório: https://github.com/elc1090/demo-attendance-indexeddb

### Descrição

Protótipo client-side para demonstrar IndexedDB em uma aplicação de chamada.
#### Funcionalidades
- importação de turma por CSV;
- CSV com apenas duas colunas: `id` e `nome`;
- suporte a múltiplas turmas;
- criação/abertura de chamada por data;
- todos os estudantes começam como presentes; desmarcar o checkbox registra ausência;
- filtros por status;
- busca de estudante;
- persistência local com IndexedDB;
- exportação em CSV e JSON;
- layout responsivo para desktop e smartphone.
#### Tecnologias
- HTML
- CSS
- JavaScript
- IndexedDB
#### Autor
Andrea Schwertner Charão | [AndreaInfUFSM](https://github.com/AndreaInfUFSM)

## Demanda do(a) cliente

### Cliente
Arthur Moro Fróes

### Demanda

- Menu de visão geral das minhas chamadas, onde posso navegar pelas turmas e ver todas as chamadas realizadas em uma turma. Ao clicar em uma chamada, abrir na tela dela para edição. É ruim ter que navegar nas chamadas pelo calendário, selecionado os dias individuais
- Opção de exportar em PDF (com estética de acordo com o restante da aplicação) ao invés de CSV
- Opção de exportar todas as chamadas de uma turma. Adicionar em páginas dentro de um PDF cada chamada realizada, ordenado por data da mais antiga pra mais recente.
- Visão geral de presenças de uma turma usado gráficos fáceis de entender. Na mesma tela onde vemos todas as chamadas da turma.
- Opção de exportar o relatório de presença de um único aluno durante todo o semestre.


## Desenvolvimento

### Processo

#### Primeira demanda (Visão Geral)
Primeiro, decidi explorar como era feito o botão "Turmas" para poder colocar um botão de visão geral do lado. Tentei copiar e colar o `button` Turmas, mas na página os botões ficavam com um espaçamento muito grande um do outro, em vez de ficarem juntos lado a lado.<br>
Descobri que a classe css que os botões usavam faziam com que a distribuição de elementos em `header` ficassem igualmente espaçados, com `display: flex` e `justify-content: space-between`<br>
Para resolver, coloquei os dois `button` em uma div, então agora são tratados como um elemento só.
O meu próximo passo foi olhar como funcionava o botão de Turmas e como ele se ligava ao JavaScript. Notei que "id" fazia essa ligação, da seguinte maneira:<br>
tal id fica dentro de função no js `bindEvents` cuida de todos os clique e eventos --> quando é clicado, chama outra função (async?) que é onde está a lógica para mostrar as turmas.

Dessa forma, fiz a mesma coisa com o botão Visão Geral, aproveitando o código que Turmas utiliza. Após isso, precisei desenvolver a lógica de "clicar em turma -> mostrar todas as chamadas em lista, de acordo com id da turma e data", e para isso criei uma nova função para cuidar disso. Eu já entendia o que e como queria fazer, porém, o JavaScript é para mim uma linguagem nova, então precisei consultar IA para entender como "escrever em JS" meu objetivo.
Com isso, Visão Geral era funcional, apesar de não muito bonito.

#### Quarta demanda (Gráficos em Visão Geral)
Aqui, decidi primeiramente pesquisar por bibliotecas JavaScript que faziam a construção de gráficos para mim. ...

### Trechos de código

Indique pelo menos 3 trechos de código que você queira destacar para a turma (por exemplo, para contrastar com o código original, para explicar algo que aprendeu, para alertar sobre alguma dificuldade de compreensão, para mostrar uma curiosidade, etc).


## Tecnologias

### Linguagens e afins

Substitua este trecho por uma lista detalhada de tecnologias usadas no remake (tanto as básicas, como HTML, CSS e JavaScript, como alguma específica, por exemplo APIs externas, etc.):
- ...
- ...
-

### Ambiente de desenvolvimento

Substitua este trecho por uma lista detalhada dos ambientes/ferramentas de desenvolvimento que você usou (por exemplo, VS Code + alguma extensão, agentes de IA, etc.)
- ...
- ...

## Referências e créditos

Substitua este trecho por uma lista bem detalhada de todo material que você consultou para ajudar no projeto, por exemplo:  URLs de vídeos ou outro material consultado, créditos para colegas que colaboraram, geradores de código, etc.
- ...
- ...




---
Projeto entregue para a disciplina de [Desenvolvimento de Software para a Web](http://github.com/andreainfufsm/elc1090-2026b) em 2026b