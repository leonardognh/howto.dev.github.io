<style>
.border {
  border: 1px solid black
}
</style>

Se quisermos criar um campo de entrada em nosso `<form>`, precisaremos da ajuda do elemento `<input>`.

O elemento `<input>` possui um atributo type que determina como ele é renderizado na página da web e que tipo de dados ele pode aceitar.

O primeiro valor para o atributo type que iremos explorar é `text`. Quando criamos um elemento `<input>` com `type="text"`, ele renderiza um campo de texto no qual os usuários podem digitar. Observe que o valor padrão do tipo é `text`. Também é importante incluir um atributo name para `<input>` — sem o atributo name, as informações em `<input>` não serão enviadas quando o `<form>` for enviado. Explicaremos mais sobre envios e o botão enviar em um exercício posterior. Por enquanto, vamos examinar o seguinte código que produz um campo de entrada de texto:

```
<form action="/example.html" method="POST">
  <input type="text" name="first-text-field">
</form>
```

Aqui está uma captura de tela da aparência do formulário renderizado em uma página da web para o navegador Chrome (navegadores diferentes têm renderização padrão diferente). Quando carregado inicialmente, será uma caixa vazia:

<form>
  <input class="border" type="text" name="first-text-field">
</form>

campo de texto vazio renderizado do elemento de entrada `type='text'`
Depois que os usuários digitam no elemento `<input>`, o valor do atributo value se torna o que é digitado no campo de texto. O valor do atributo value é emparelhado com o valor do atributo name e enviado como texto quando o formulário é enviado. Por exemplo, se um usuário digitou “detalhes importantes” no campo de texto criado pelo nosso elemento `<input>`:

<form>
  <input class="border" type="text" name="first-text-field" value="detalhes importantes">
</form>

campo de texto preenchido renderizado que diz 'detalhes importantes'
Quando o formulário é enviado, o texto: `first-text-field=detalhes importantes` é enviado para `/example.html` porque o valor do atributo name é `first-text-field` e o valor do valor é "detalhes importantes".

Também poderíamos atribuir um valor padrão para o atributo value para que os usuários tenham um campo de texto preenchido quando virem o formulário renderizado pela primeira vez, assim:

```
<form action="/example.html" method="POST">
  <input type="text" name="first-text-field" value="já preenchido">
</form>
```

É renderizado caixa de texto preenchida devido ao atributo `value` atribuído:

<form>
  <input class="border" type="text" name="first-text-field" value="já preenchido">
</form>
