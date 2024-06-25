# Elementos Iniciais: Tag `<body>`

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
