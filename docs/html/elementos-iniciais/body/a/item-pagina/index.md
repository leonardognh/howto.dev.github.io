# Elementos Iniciais: Body

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
