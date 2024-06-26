# Elementos Iniciais: Body

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
