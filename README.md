# RAPSXLoader

Script Node.js para automatizar o download dos jogos de Playstation 1 compatíveis com conquistas no Retroachievements.

## Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:
* Instalar a versão mais atual do NodeJS;
* Executar ```npm install --global``` na raíz do projeto;

## Executando

Para executar o projeto, execute o seguinte comando na diretório raiz do projeto:
```npm start```

## Como funciona

Por não possuir uma API para os downloads das ISOs, é feito o download das páginas do archive.org contendo os links para as ISOs.


Utilizando busca por seletores de classes CSS (```querySelector```), as URLs são guardadas em um array.


O mesmo processo é feito na página que contém a lista de jogos com conquistas no Retroachievements.


É feita uma comparação: Para cada item na lista de conquistas, compara-se o nome do jogo com o do link do archive.org, filtando caracteres especiais e fragmentos de texto.


Por último, é verificado se na raíz do projeto já existe um arquivo com aquele mesmo nome; caso não exista, vai realizar o donwload.

## Melhorias

O projeto é inicial e funcional; mas as seguintes melhorias estão sendo focadas:

- [x] Fazer o download da ISO do jogo vindo do archive.org
- [x] Criar filtros que permitam fazer o "match" entre jogo e conquista de pelo menos 50% da lista de jogos com conquista
- [x] Fazer o download das coleções do archive.org que tenham várias páginas, permitindo a leitura de ISO de diferentes regiões
- [ ] Criar uma interface gráfica
- [ ] Parametrizar o projeto para fazer o match de mais consoles

## Aspectos legais

É de inteira responsabilidade sua baixar e executar o script. Apenas o implementei com a finalidade de exercitar os meus conhecimentos os relacionando com o meu hobby. Manter ISOs e executar jogos os quais você não possui pode implicar em sansões legais.