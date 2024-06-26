# Estrutura Base

## HMTL

Os arquivos HTML requerem certos elementos para configurar o documento corretamente. Podemos informar aos navegadores que estamos usando HTML iniciando nosso documento com uma declaração de tipo de documento.

A declaração fica assim:

`<!DOCTYPE html>`

Esta declaração é uma instrução e deve ser a primeira linha do código do seu documento HTML. Ele informa ao navegador que tipo de documento esperar, juntamente com qual versão do HTML está sendo usada no documento. Por enquanto, o navegador assumirá corretamente que o html em `<!DOCTYPE html>` se refere ao HTML5, pois é o padrão atual.

No futuro, porém, um novo padrão substituirá o HTML5. Para garantir que seu documento seja sempre interpretado corretamente, sempre inclua `<!DOCTYPE html>` no início de seus documentos HTML.

Por último, o código HTML é sempre salvo em um arquivo com extensão .html.

Para criar estrutura e conteúdo HTML, devemos adicionar tags de abertura e fechamento `<html>` após declarar `<!DOCTYPE html>`:

```
<!DOCTYPE html>
<html>

</html>
```

Qualquer coisa entre as tags de abertura `<html>` e de fechamento `</html>` será interpretada como código HTML. Sem essas tags, é possível que os navegadores interpretem incorretamente o seu código HTML.
