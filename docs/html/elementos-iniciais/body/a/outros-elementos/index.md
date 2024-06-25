# Elementos Iniciais: Tag `<body>`

### Link em outros elementos

Você provavelmente já visitou sites onde nem todos os links eram compostos de texto. Talvez os links em que você clicou fossem imagens ou alguma outra forma de conteúdo.

Até agora, adicionamos links compostos apenas de texto, como o seguinte:

`<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank">Espinhoso</a>`

Links somente de texto, entretanto, diminuiriam significativamente sua flexibilidade como desenvolvedor web!

Felizmente, o HTML permite transformar praticamente qualquer elemento em um link, envolvendo esse elemento com um elemento âncora. Com esta técnica, é possível transformar imagens em links simplesmente envolvendo o elemento `<img>` com um elemento `<a>`.

`<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank"><img src="https://www.Prickly_Pear_Closeup.jpg" alt="Uma fruta vermelha de pera espinhosa"/> </a>`

No exemplo acima, a imagem de uma pera espinhosa foi transformada em um link envolvendo a parte externa do elemento `<img>` com um elemento `<a>`.
