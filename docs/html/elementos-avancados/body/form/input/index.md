# Elementos Avançados: Body

## Input Base

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

## Label

O elemento `<label>` possui uma tag de abertura e fechamento e exibe o texto que está escrito entre as tags de abertura e fechamento. Para associar um `<label>` e um `<input>`, o `<input>` precisa de um atributo id. Em seguida, atribuímos o atributo for do elemento `<label>` com o valor do atributo id de `<input>`, assim:

```
<form>
  <label for="refeicao">O que você quer comer?</label>
  <br>
  <input type="text" name="comida" id="refeicao">
</form>
```

<form>
  <label for="refeicao">O que você quer comer?</label>
  <br>
  <input class="border" type="text" name="comida" id="refeicao">
</form>

O formulário renderizado com campo de texto rotulado.

Agora os usuários sabem para que serve o elemento `<input>`! Outro benefício de usar o elemento `<label>` é que quando este elemento é clicado, o `<input>` correspondente é destacado/selecionado.

## Input Tipo Senha

Pense em todas as vezes que tivemos que colocar informações confidenciais, como uma senha ou PIN, em um `<form>`. Não queremos que nossas informações sejam vistas por ninguém que esteja espiando por cima do nosso ombro! Felizmente, temos o atributo `type="password"` para `<input>`!

Um elemento `<input type ="password">` substituirá o texto de entrada por outro caractere como um asterisco (\*) ou um ponto (•). O código abaixo fornece um exemplo de como criar um campo de senha:

```
<form>
  <label for="senha-usuario">Senha: </label>
  <input type="password" id="senha-usuario" name="senha-usuario">
</form>
```

<form>
  <label for="senha-usuario">Senha: </label>
  <input class="border" type="password" id="senha-usuario" name="senha-usuario">
</form>

Mesmo que o campo de senha oculte o texto da senha, quando o formulário é enviado, o valor do texto é enviado. Ou seja, se for digitado `senha123` no campo de senha, `senha-usuario=senha123` será enviado junto com as demais informações do formulário.

## Input Tipo Número

Agora examinamos dois atributos de tipo para `<input>` relacionados ao texto. Mas, podemos querer que nossos usuários digitem um número — nesse caso, podemos definir o atributo type como number!

Ao definir `type="number"` para um `<input>` podemos restringir o que os usuários digitam no campo de entrada apenas para números (e alguns caracteres especiais como -, + e .). Também podemos fornecer um atributo step que cria setas dentro do campo de entrada para aumentar ou diminuir o valor do atributo step. Abaixo está o código necessário para renderizar um campo de entrada para números:

```
<form>
  <label for="anos"> Idade: </label>
  <input id="anos" name="anos" type="number" step="1">
</form>
```

<form>
  <label for="anos"> Idade: </label>
  <input class="border" id="anos" name="anos" type="number" step="1">
</form>
O campo de entrada de número renderizado com setas no lado direito do campo.

## Input Tipo Intervalo

Usar um `<input type="number">` é ótimo se quisermos permitir que os usuários digitem qualquer número de sua escolha. Mas, se quiséssemos limitar quais números nossos usuários poderiam digitar, poderíamos considerar o uso de um valor de tipo diferente. Outra opção que poderíamos usar é definir o tipo como `range`, o que cria um controle deslizante.

Para definir os valores mínimo e máximo do controle deslizante, atribuímos valores aos atributos min e max do `<input>`. Também poderíamos controlar o quão suave e fluido o controle deslizante funciona, atribuindo um valor ao atributo step. Valores de passos menores farão com que o controle deslizante se mova com mais fluidez, enquanto valores de passos maiores farão com que o controle deslizante se mova de maneira mais perceptível. Dê uma olhada no código para criar um controle deslizante:

```
<form>
  <label for="volume"> Controle de volume</label>
  <input id="volume" name="volume" type="range" min="0" max="100" step="1">
</form>
```

<form>
  <label for="volume">Controle de volume:</label>
  <input class="border" id="volume" name="volume" type="range" min="0" max="100" step="1">
</form>

No exemplo acima, cada vez que o controle deslizante se move um, o valor do atributo de valor de `<input>` muda.

## Input Tipo Caixa Multi Seleção

Até agora, os tipos de entradas que permitimos eram todas escolhas únicas. Mas, e se apresentássemos múltiplas opções aos usuários e permitíssemos que eles selecionassem qualquer número de opções? Parece que poderíamos usar caixas de seleção! Em um `<form>` usaríamos o elemento `<input>` e definiríamos type="checkbox". Examine o código usado para criar várias caixas de seleção:

```
<form>
  <p>Escolha o recheio da sua pizza:</p>
  <label for="cheese">Queijo extra</label>
  <input id="queijo" name="topping" type="checkbox" value="queijo">
  <br>
  <label for="calabresa">Calabresa</label>
  <input id="calabresa" name="topping" type="checkbox" value="calabresa">
  <br>
  <label for="presunto">Presunto</label>
  <input id="presunto" name="topping" type="checkbox" value="presunto">
</form>
```

<form>
  <p>Escolha o recheio da sua pizza:</p>
  <label for="cheese">Queijo</label>
  <input class="border" id="queijo" name="recheio" type="checkbox" value="queijo">
  <br>
  <label for="calabresa">Calabresa</label>
  <input class="border" id="calabresa" name="recheio" type="checkbox" value="calabresa">
  <br>
  <label for="presunto">Presunto</label>
  <input class="border" id="presunto" name="recheio" type="checkbox" value="presunto">
</form>

Existem valores atribuídos ao atributo de valor das caixas de seleção.

Esses valores não são visíveis no próprio formulário, por isso é importante utilizarmos um `<label>` associado para identificar o checkbox.
cada `<input>` tem o mesmo valor para o atributo name. Usar o mesmo nome para cada caixa de seleção agrupa os `<input>s`. No entanto, cada `<input>` possui um ID exclusivo para emparelhar com um `<label>`.

## Input Tipo Caixa Única Seleção

As caixas de seleção funcionam bem se quisermos apresentar aos usuários múltiplas opções e deixá-los escolher uma ou mais opções. No entanto, há casos em que queremos apresentar múltiplas opções e permitir apenas uma seleção — como perguntar aos usuários se eles concordam ou discordam dos termos e condições. Vejamos o código usado para criar botões de opção:

```
<form>
  <p>Qual ​​é a soma de 1 + 1?</p>
  <input type="radio" id="dois" name="resposta" valor="2">
  <label for="dois">2</label>
  <br>
  <input type="radio" id="eleven" name="resposta" value="11">
  <label for="onze">11</label>
</form>
```

<form>
  <p>Qual ​​é a soma de 1 + 1?</p>
  <input class="border" type="radio" id="dois" name="resposta" valor="2">
  <label for="dois">2</label>
  <br>
  <input class="border" type="radio" id="onze" name="resposta" value="11">
  <label for="onze">11</label>
</form>

O formulário renderizado contendo botões de opção.

Observe no trecho de código que os botões de opção (como caixas de seleção) não exibem seu valor. Temos um `<label>` associado para representar o valor do botão de opção. Para agrupar botões de opção, atribuímos a eles o mesmo nome e apenas um botão de opção desse grupo pode ser selecionado.
