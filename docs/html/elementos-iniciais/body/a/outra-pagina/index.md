# Elementos Iniciais: Body

### Link para outra página `<a>`

Um dos aspectos poderosos do HTML (e da Internet) é a capacidade de vincular a outras páginas da web.

Você pode adicionar links a uma página da web adicionando um elemento âncora `<a>` e incluindo o texto do link entre as tags de abertura e fechamento.

`<a>Este é um link para a Wikipédia</a>`

Espere um minuto! Tecnicamente, o link do exemplo acima está incompleto. Como exatamente o link acima deve funcionar se não houver um URL que leve os usuários à página real da Wikipedia?

O elemento âncora no exemplo acima está incompleto sem o atributo href. Este atributo significa referência de hipertexto e é usado para vincular a um caminho ou endereço onde um arquivo está localizado (seja no seu computador ou em outro local). Os caminhos fornecidos para o atributo href geralmente são URLs.

`<a href="https://www.wikipedia.org/">Este é um link para a Wikipédia</a>`

No exemplo acima, o atributo href foi definido como o valor da URL https://www.wikipedia.org/. O exemplo agora mostra o uso correto de um elemento âncora.

Ao ler a documentação técnica, você pode encontrar o termo hiperlink. Não se preocupe, este é simplesmente o termo técnico para link. Esses termos são frequentemente usados ​​de forma intercambiável.

#### Abrir link em outra aba

Você já clicou em um link e observou a página da web resultante aberta em uma nova janela do navegador? Nesse caso, você pode agradecer ao atributo `target` do elemento `<a>`.

O atributo `target` especifica como um link deve ser aberto.

É possível que um ou mais links em sua página da web direcionem para um site totalmente diferente. Nesse caso, você pode querer que os usuários leiam o site vinculado, mas espere que eles retornem à sua página da web. É exatamente nesse momento que o atributo `target` é útil!

Para que um link seja aberto em uma nova janela, o atributo `target` requer um valor `_blank`. O atributo `target` pode ser adicionado diretamente à tag de abertura do elemento âncora, assim como o atributo `href`.

`<a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">O urso pardo</a>`

No exemplo acima, definir o atributo target como `_blank` instrui o navegador a abrir a página relevante da Wikipedia em uma nova janela.
