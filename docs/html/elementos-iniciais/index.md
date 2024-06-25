# Elementos Iniciais

## Para Tag `<head>`

### Título da Página `<title>`

Que tipo de metadados sobre a página da web o elemento `<head>` pode conter?

Se você navegar até o catálogo da Codecademy e olhar na parte superior do seu navegador, notará as palavras Todos os cursos e tutoriais | Codecademy, que é o título da página web.

A guia do navegador exibe o título especificado na tag `<title>`. A tag `<title>` está sempre dentro do `<head>`.

```
<!DOCTYPEhtml>
<html>
  <cabeça>
    <title>Meu diário de codificação</title>
  </head>
</html>
```

Se abríssemos um arquivo contendo o código HTML do exemplo acima, o navegador exibiria as palavras My Coding Journal na barra de título (ou no título da guia).

## Para Tag `<body>`

### Títulos `<h#>`

Os títulos em HTML são semelhantes aos títulos de outros tipos de mídia. Por exemplo, em jornais, títulos grandes são normalmente usados ​​para captar a atenção do leitor. Outras vezes, os títulos são usados ​​para descrever o conteúdo, como o título de um filme ou de um artigo educacional.

HTML segue um padrão semelhante. Em HTML, existem seis títulos ou elementos de título diferentes. Os títulos podem ser usados ​​para diversos fins, como títulos de seções, artigos ou outras formas de conteúdo.

A seguir está a lista de elementos de título disponíveis em HTML. Eles são ordenados do maior para o menor tamanho.

```
<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
```

### Divisão `<div>`

Um dos elementos mais populares em HTML é o elemento `<div>`. `<div>` é a abreviação de “divisão” ou um contêiner que divide a página em seções. Essas seções são muito úteis para agrupar elementos em seu HTML.

```
<div>
  <div>
    <h1>Por que usar divs?</h1>
    <p>Ótimo para agrupar elementos!</p>
  </div>
</body>
```

`<div>`s não possuem inerentemente uma representação visual, mas são muito úteis quando queremos aplicar estilos personalizados aos nossos elementos HTML. `<div>`s nos permitem agrupar elementos HTML para aplicar os mesmos estilos a todos os elementos HTML internos. Também podemos estilizar o elemento `<div>` como um todo. Você pode ver como isso pode ser feito no curso Aprenda CSS.

`<div>`s podem conter qualquer texto ou outros elementos HTML, como links, imagens ou vídeos. Lembre-se de sempre adicionar dois espaços de recuo ao aninhar elementos dentro de `<div>`s para melhor legibilidade.

### Atributos

Se quisermos expandir a tag de um elemento, podemos fazer isso usando um atributo. Atributos são conteúdos adicionados à tag de abertura de um elemento e podem ser usados ​​de diversas maneiras, desde fornecer informações até alterar o estilo. Os atributos são compostos pelas duas partes a seguir:

- O nome do atributo
- O valor do atributo

Um atributo comumente usado é o id. Podemos usar o atributo id para especificar conteúdos diferentes (como `<div>`s) e é realmente útil quando você usa um elemento mais de uma vez. Os ids têm vários propósitos diferentes em HTML, mas por enquanto, vamos nos concentrar em como eles podem nos ajudar a identificar o conteúdo da nossa página.

Quando adicionamos um id a um `<div>`, colocamos ele na tag de abertura:

```
<div id="intro">
  <h1>Introdução</h1>
</div>
```

### Textos `<p>` / Intervalo `<span>`

Se quiser exibir texto em HTML, você pode usar um parágrafo ou intervalo:

Parágrafos `<p>` contêm um bloco de texto simples.
`<span>` contém pequenos trechos de texto ou outro HTML. Eles são usados ​​para separar pequenos pedaços de conteúdo que estão na mesma linha de outro conteúdo.
Dê uma olhada em cada um desses elementos em ação abaixo:

```
<div>
  <h1>Tecnologia</h1>
</div>
<div>
  Prevê-se que <p><span>carros autônomos</span> substituam até 2 milhões
  de empregos nas próximas duas décadas.</p>
</div>
```

No exemplo acima, existem dois `<div>` diferentes. O segundo `<div>` contém um `<p>` com `<span>`Carros autônomos`</span>`. Este elemento `<span>` separa “Carros autônomos” do restante do texto do parágrafo.

É melhor usar um elemento `<span>` quando você deseja direcionar um conteúdo específico que está embutido ou na mesma linha de outro texto. Se você quiser dividir seu conteúdo em blocos, é melhor usar um `<div>`.

### Estilizando Textos

Você também pode estilizar o texto usando tags HTML. A tag `<em>` enfatiza o texto, enquanto a tag `<strong>` destaca o texto importante.

Mais tarde, quando começar a estilizar sites, você decidirá como deseja que os navegadores exibam o conteúdo nas tags `<em>` e `<strong>`. Os navegadores, no entanto, possuem folhas de estilo integradas que geralmente estilizam essas tags das seguintes maneiras:

- A tag `<em>` geralmente será renderizada com ênfase em itálico.
- O `<strong>` geralmente será renderizado com ênfase em negrito.
  Dê uma olhada em cada estilo em ação:

```
<p>
  <strong>O Rio Nilo</strong> é o <em>maior</em> rio do mundo, medindo
  mais de 6.850 quilômetros de extensão (aproximadamente 4.260 milhas).
</p>
```

Neste exemplo, as tags `<strong>` e `<em>` são usadas para enfatizar o texto e produzir o seguinte:

<p>
  <strong>O Rio Nilo</strong> é o <em>maior</em> rio do mundo, medindo mais de 6.850 quilômetros de extensão (aproximadamente 4.260 milhas).
</p>

Como podemos ver, “O Rio Nilo” está em negrito e “maior” está em itálico.

### Pular Linha `<br>`

O espaçamento entre os códigos em um arquivo HTML não afeta o posicionamento dos elementos no navegador. Se estiver interessado em modificar o espaçamento no navegador, você pode usar o elemento de quebra de linha do HTML: `<br>`.

O elemento de quebra de linha é único porque é composto apenas por uma tag inicial. Você pode usá-lo em qualquer lugar do seu código HTML e uma quebra de linha será mostrada no navegador.

```
<p>
  O Rio Nilo é o maior rio <br> do mundo, medindo mais de 6.850 <br>
  quilômetros de extensão (aproximadamente 4.260 <br> milhas).
</p>
```

O código no exemplo acima resultará em uma saída semelhante a esta:

<p>O Rio Nilo é o maior rio <br> do mundo, medindo mais de 6.850 <br>
quilômetros de extensão (aproximadamente 4.260 <br> milhas).</p>

### Lista Não Ordenada `<ul>`

Além de organizar o texto em forma de parágrafo, você também pode exibir o conteúdo em uma lista de fácil leitura.

Em HTML, você pode usar uma tag de lista não ordenada `<ul>` para criar uma lista de itens sem nenhuma ordem específica. Uma lista não ordenada descreve itens individuais da lista com um marcador.

O elemento `<ul>` não deve conter texto bruto e não formatará automaticamente o texto bruto em uma lista não ordenada de itens. Itens individuais da lista devem ser adicionados à lista não ordenada usando a tag `<li>`. A tag `<li>` ou item de lista é usada para descrever um item em uma lista.

```
<ul>
  <li>Limas</li>
  <li>Tortilhas</li>
  <li>Frango</li>
</ul>
```

No exemplo acima, a lista foi criada usando a tag `<ul>` e todos os itens individuais da lista foram adicionados usando as tags `<li>`.

A saída ficará assim:

<ul>
  <li>Limas</li>
  <li>Tortilhas</li>
  <li>Frango</li>
</ul>

### Lista Ordenada `<ol>`

Listas ordenadas `<ol>` são como listas não ordenadas, exceto que cada item da lista é numerado. Eles são úteis quando você precisa listar diferentes etapas de um processo ou classificar os itens do primeiro ao último.

Você pode criar a lista ordenada com a tag `<ol>` e, em seguida, adicionar itens de lista individuais à lista usando tags `<li>`.

```
<ol>
  <li>Pré-aqueça o forno a 350 graus.</li>
  <li>Misture farinha de trigo integral, bicarbonato de sódio e sal.</li>
  <li>Bata a manteiga e o açúcar em uma tigela separada.</li>
  <li>Adicione os ovos e o extrato de baunilha à tigela.</li>
</ol>
```

A saída ficará assim:

<ol>
  <li>Pré-aqueça o forno a 350 graus.</li>
  <li>Misture farinha de trigo integral, bicarbonato de sódio e sal.</li>
  <li>Bata a manteiga e o açúcar em uma tigela separada.</li>
  <li>Adicione os ovos e o extrato de baunilha à tigela.</li>
</ol>

### Imagens `<img>`

Todos os elementos que você aprendeu até agora (títulos, parágrafos, listas e trechos) têm uma coisa em comum: são compostos inteiramente de texto! E se você quiser adicionar conteúdo à sua página da web que não seja composto de texto, como imagens?

A tag `<img>` permite adicionar uma imagem a uma página da web. A maioria dos elementos requer tags de abertura e fechamento, mas a tag `<img>` é uma tag de fechamento automático. Observe que o final da tag `<img>` possui uma barra /. Tags de fechamento automático podem incluir ou omitir a barra final — ambas serão renderizadas corretamente.

`<img src="image-localizacao.jpg" />`

A tag `<img>` possui um atributo obrigatório chamado src. O atributo src deve ser definido como a origem da imagem ou o local da imagem. Nesse caso, o valor de src deve ser o localizador uniforme de recursos (URL) da imagem. Um URL é o endereço da web ou endereço local onde um arquivo está armazenado.

### Imagem Alt

Parte de ser um desenvolvedor web excepcional é tornar seu site acessível a usuários de todas as origens. Para tornar a Web mais inclusiva, precisamos de considerar o que acontece quando tecnologias de apoio, como leitores de ecrã, se deparam com etiquetas de imagem.

O atributo alt, que significa texto alternativo, traz significado às imagens de nossos sites. O atributo alt pode ser adicionado à tag da imagem assim como o atributo src. O valor de alt deve ser uma descrição da imagem.

`<img src="#" alt="Um campo de girassóis amarelos" />`

O atributo alt também serve aos seguintes propósitos:

Se uma imagem não for carregada em uma página da web, o usuário poderá passar o mouse sobre a área originalmente destinada à imagem e ler uma breve descrição da imagem. Isso é possível pela descrição que você fornece no atributo alt.
Usuários com deficiência visual geralmente navegam na web com a ajuda de softwares de leitura de tela. Ao incluir o atributo alt, o software de leitura de tela pode ler a descrição da imagem em voz alta para o usuário com deficiência visual.
O atributo alt também desempenha um papel na otimização de mecanismos de pesquisa (SEO), porque os mecanismos de pesquisa não podem “ver” as imagens nos sites enquanto rastreiam a Internet. Ter atributos alternativos descritivos pode melhorar a classificação do seu site.
Se a imagem na página da web não transmitir qualquer informação significativa para um usuário (deficiente visual ou não), o atributo alt deve ser deixado em branco.

### Videos `<video>`

Além de imagens, o HTML também oferece suporte à exibição de vídeos. Assim como o elemento `<img>`, o elemento `<video>` requer um atributo src com um link para a fonte do vídeo. Ao contrário do elemento `<img>`, entretanto, o elemento `<video>` requer uma tag de abertura e uma tag de fechamento.

```
<video src="myVideo.mp4" width="320" height="240" controles>
  Vídeo não suportado
</vídeo>
```

Neste exemplo, a fonte de vídeo (src) é “myVideo.mp4”. A fonte pode ser um arquivo de vídeo hospedado junto com sua página da web ou um URL que aponta para um arquivo de vídeo hospedado em outra página da web.

Após o atributo src, os atributos width e height são usados ​​para definir o tamanho do vídeo exibido no navegador. O atributo de controles instrui o navegador a incluir controles básicos de vídeo, como pausar e reproduzir.

O texto Vídeo não suportado entre as tags de abertura e fechamento do vídeo só será exibido se o navegador não conseguir carregar o vídeo.

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

### Link em outros elementos

Você provavelmente já visitou sites onde nem todos os links eram compostos de texto. Talvez os links em que você clicou fossem imagens ou alguma outra forma de conteúdo.

Até agora, adicionamos links compostos apenas de texto, como o seguinte:

`<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank">Espinhoso</a>`

Links somente de texto, entretanto, diminuiriam significativamente sua flexibilidade como desenvolvedor web!

Felizmente, o HTML permite transformar praticamente qualquer elemento em um link, envolvendo esse elemento com um elemento âncora. Com esta técnica, é possível transformar imagens em links simplesmente envolvendo o elemento `<img>` com um elemento `<a>`.

`<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank"><img src="https://www.Prickly_Pear_Closeup.jpg" alt="Uma fruta vermelha de pera espinhosa"/> </a>`

No exemplo acima, a imagem de uma pera espinhosa foi transformada em um link envolvendo a parte externa do elemento `<img>` com um elemento `<a>`.

### Link para item da página

Neste ponto, temos todo o conteúdo que queremos em nossa página. Como temos tanto conteúdo, nem tudo cabe na tela. Como tornamos mais fácil para um usuário ir para diferentes partes de nossa página?

Quando os usuários visitam nosso site, queremos que eles possam clicar em um link e fazer com que a página role automaticamente para uma seção específica.

Para vincular a um alvo na mesma página, devemos dar um ID ao alvo, como este:

```
<p id="top">Este é o topo da página!</p>
<h1 id="bottom">Este é o fundo! </h1>
```

Neste exemplo, o elemento `<p>` recebe um id `top` e o elemento `<h1>` recebe `bottom`. Um ID pode ser adicionado à maioria dos elementos de uma página da web.

Um id deve ser descritivo para facilitar a lembrança da finalidade de um link. O link de destino é uma string contendo o caractere # e o id do elemento de destino.

```
<ol>
 <li><a href="#top">Principal</a></li>
 <li><a href="#bottom">Inferior</a></li>
</ol>
```

No exemplo acima, os links para `<p id="top">` e `<h1 id="bottom">` estão incorporados em uma lista ordenada. Esses links aparecem no navegador como uma lista numerada de links. Um id é especialmente útil para organizar conteúdo pertencente a um div!
