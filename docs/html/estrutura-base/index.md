# Estrutura Base

Os arquivos HTML requerem certos elementos para configurar o documento corretamente. Podemos informar aos navegadores que estamos usando HTML iniciando nosso documento com uma declaração de tipo de documento.

A declaração fica assim:

`<!DOCTYPE html>`

Esta declaração é uma instrução e deve ser a primeira linha do código do seu documento HTML. Ele informa ao navegador que tipo de documento esperar, juntamente com qual versão do HTML está sendo usada no documento. Por enquanto, o navegador assumirá corretamente que o html em `<!DOCTYPE html>` se refere ao HTML5, pois é o padrão atual.

No futuro, porém, um novo padrão substituirá o HTML5. Para garantir que seu documento seja sempre interpretado corretamente, sempre inclua `<!DOCTYPE html>` no início de seus documentos HTML.

Por último, o código HTML é sempre salvo em um arquivo com extensão .html.

## Tag `<html>`

A declaração `<!DOCTYPE html>` fornece ao navegador duas informações (o tipo de documento e a versão HTML esperada), mas na verdade não adiciona nenhuma estrutura ou conteúdo HTML.

Para criar estrutura e conteúdo HTML, devemos adicionar tags de abertura e fechamento `<html>` após declarar `<!DOCTYPE html>`:

```
<!DOCTYPE html>
<html>

</html>
```

Qualquer coisa entre as tags de abertura `<html>` e de fechamento `</html>` será interpretada como código HTML. Sem essas tags, é possível que os navegadores interpretem incorretamente o seu código HTML.

## Tag `<head>`

O elemento `<head>` faz parte desta metáfora HTML. Vai acima do nosso elemento `<body>`.

O elemento `<head>` contém os metadados de uma página web. Metadados são informações sobre a página que não são exibidas diretamente na página da web. Ao contrário das informações contidas na tag `<body>`, os metadados no cabeçalho são informações sobre a própria página. Você verá um exemplo disso no próximo exercício.

As tags head de abertura e fechamento normalmente aparecem como o primeiro item após sua primeira tag HTML:

```
<head>
</head>
```

## Tag `<body>`

Um dos principais elementos HTML que usamos para construir uma página da web é o elemento body. Somente o conteúdo dentro das tags body de abertura e fechamento pode ser exibido na tela. Esta é a aparência das tags body de abertura e fechamento:

```
<body>
</body>
```

Depois que o arquivo tiver um body, muitos tipos diferentes de conteúdo – incluindo texto, imagens e botões – podem ser adicionados ao body.
