# Trabalho prático de Desenvolvimento Reativo

## Objetivo
Identificar pelo menos 3 problemas/melhorias em uma [aplicação React](https://codesandbox.io/s/trabalho-pratico-rea-5ggeg?file=/src/App.js) e documentar o problema e a solução.
 
<hr>

### Problemas identificados em App.js:

- Os elementos de lista não tinham a prop key definida, adicionei `key={game.description}`
- A contagem de caracteres não estava retornando o número de caracteres, mas a palavra. Corrigido com um `.length`
- Lista de jogos retornava 1 item a mais porque estava selecionando index menor ou igual ao número definido no range. Deixando apenas `index < numberOfGames` esse problema é corrigido
- A função `getDefaultText` estava sendo executada com o uso de "()" a cada render. Removendo os parênteses a função não é re-executada, mas referenciada

### Extra:

- O componente Timer não tinha `return` dentro do `useEffect`, dando erro no unmount toda vez que desmarcamos o cronômetro. Corrigi em Timer.js adicionando `return` antes do `setInterval`
