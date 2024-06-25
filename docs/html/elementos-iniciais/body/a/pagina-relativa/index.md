# Elementos Iniciais: Tag `<body>`

### Link para página relativa

Até agora você aprendeu como criar links para páginas da web externas. Muitos sites também possuem links para páginas internas da web, como Home, About e Contact.

Antes de aprendermos como vincular páginas internas, vamos estabelecer onde nossos arquivos estão armazenados. Ao criar sites estáticos de várias páginas, os desenvolvedores da web geralmente armazenam arquivos HTML no diretório raiz ou em uma pasta principal onde todos os arquivos do projeto são armazenados. À medida que o tamanho dos projetos criados aumenta, você pode usar pastas adicionais dentro da pasta principal do projeto para organizar seu código.

```
pasta de projeto/
|—— sobre.html
|—— contato.html
|—— índice.html
```

O exemplo acima mostra três arquivos diferentes – <strong>about.html</strong>, <strong>contact.html</strong> e <strong>index.html</strong> em uma pasta.

Os arquivos HTML geralmente são armazenados na mesma pasta, conforme mostrado no exemplo acima. Se o navegador estiver exibindo index.html, ele também saberá que about.html e contact.html estão na mesma pasta. Como os arquivos são armazenados na mesma pasta, podemos vincular páginas da web usando um caminho relativo.

`<a href="./contact.html">Contato</a>`

Neste exemplo, a tag `<a>` é usada com um caminho relativo para vincular o arquivo HTML atual ao arquivo contact.html na mesma pasta. Na página da web, Contato aparecerá como um link.

Um caminho relativo é um nome de arquivo que mostra o caminho para um arquivo local (um arquivo no mesmo site, como `./index.html`) versus um caminho absoluto (um URL completo, como `https://www.google.com/search/howto-html` que está armazenado em uma pasta diferente). O `./` em `./index.html` diz ao navegador para procurar o arquivo na pasta atual.
