{!import-css/input.md!}

# Elementos Avançados: Body

## Textarea

Um elemento `<input>` com `type="text"` cria um campo de entrada de linha única para os usuários digitarem informações. No entanto, há casos em que os usuários precisam escrever mais informações, como uma postagem de blog. Nesses casos, em vez de usar um `<input>`, poderíamos usar `<textarea>`.

O elemento `<textarea>` é usado para criar um campo de texto maior para os usuários escreverem mais texto. Podemos adicionar os atributos rows e cols para determinar a quantidade de linhas e colunas da `<textarea>`. Dê uma olhada:

```
<form>
  <label for="blog">Nova postagem no blog: </label>
  <br>
  <textarea id="blog" name="blog" rows="5" cols="30">
  </textarea>
</form>
```

<form>
  <label for="blog">Nova postagem no blog: </label>
  <br>
  <textarea class="border" id="blog" name="blog" rows="5" cols="30">
  </textarea>
</form>

Quando submetemos o formulário, o valor de `<textarea>` é o texto escrito dentro da caixa. Se quisermos adicionar um valor padrão a `<textarea>` nós o incluiremos nas tags de abertura e fechamento da seguinte forma:

```
<textarea>Adicionando texto padrão</textarea>
```

<textarea>Adicionando texto padrão</textarea>
