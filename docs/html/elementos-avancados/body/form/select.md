# Elementos Avançados: Body

## Lista Suspensa Base

Os botões de opção são ótimos se quisermos que nossos usuários escolham uma opção entre algumas opções visíveis, mas imagine se tivéssemos uma lista completa de opções! Essa situação pode levar rapidamente a muitos botões de opção para monitorar.

Uma solução alternativa é usar uma lista suspensa para permitir que nossos usuários escolham uma opção em uma lista organizada. Aqui está o código para criar um menu suspenso:

```
<form>
  <label for="almoco">O que tem para o almoço?</label>
  <select id="almoco" name="almoço">
    <option value="pizza">Pizza</option>
    <option value="macarrao">Macarrao</option>
    <option value="salada">Salada</option>
    <option value="ramen">Ramen</option>
    <option value="tacos">Tacos</option>
  </select>
</form>
```

<form>
  <label for="almoco">O que tem para o almoço?</label>
  <select id="almoco" name="almoço">
    <option value="pizza">Pizza</option>
    <option value="macarrao">Macarrao</option>
    <option value="salada">Salada</option>
    <option value="ramen">Ramen</option>
    <option value="tacos">Tacos</option>
  </select>
</form>

Observe no código que estamos usando o elemento `<select>` para criar a lista suspensa. Para preencher a lista suspensa, adicionamos vários elementos `<option>`, cada um com um atributo de valor. Por padrão, apenas uma dessas opções pode ser selecionada.

O texto renderizado é o texto incluído entre as tags `<option>` de abertura e fechamento. Porém, é o valor do atributo value que é usado no envio do `<form>` (observe a diferença no texto e na capitalização do valor). Quando o `<form>` for enviado, as informações deste campo de entrada serão enviadas utilizando o nome do `<select>` e o valor da `<option>` escolhida. Por exemplo, se um usuário selecionasse Pizza na lista suspensa, a informação seria enviada como `almoco=pizza`.

## Lista Suspensa Auto Completar

Mesmo se tivermos uma lista suspensa organizada, se a lista tiver muitas opções, pode ser entediante para os usuários percorrerem a lista inteira para localizar uma opção. É aí que o uso do elemento `<datalist>` se torna útil.

O `<datalist>` é usado com um elemento `<input type="text">`. O `<input> `cria um campo de texto onde os usuários podem digitar e filtrar opções do `<datalist>`. Vejamos um exemplo concreto:

```
<form>
  <label for="cidade">Cidade ideal para visitar?</label>
  <input type="text" list="cidades" id="cidade" name="cidade">
  <datalist id="cidades">
    <option value="Cidade de Nova York"></option>
    <option value="Tóquio"></option>
    <option value="Barcelona"></option>
    <option value="Cidade do México"></option>
    <option value="Melbourne"></option>
    <option value="Outro"></option>
  </datalist>
</form>
```

<form>
  <label for="cidade">Cidade ideal para visitar?</label>
  <input class="border" type="text" list="cidades" id="cidade" name="cidade">
  <datalist id="cidades">
    <option value="Cidade de Nova York"></option>
    <option value="Tóquio"></option>
    <option value="Barcelona"></option>
    <option value="Cidade do México"></option>
    <option value="Melbourne"></option>
    <option value="Outro"></option>  
  </datalist>
</form>

Observe que no código acima, temos um `<input>` que possui um atributo de lista. O `<input>` está associado ao `<datalist>` através do atributo de lista do `<input>` e do id do `<datalist>`.

Embora `<select>` e `<datalist>` compartilhem algumas semelhanças, existem algumas diferenças importantes. No elemento `<input>` associado, os usuários podem digitar no campo de entrada para procurar uma opção específica. Se nenhuma das `<option>` corresponder, o usuário ainda poderá usar o que digitou. Quando o formulário for enviado, o valor do nome da `<input>` e o valor da opção selecionada, ou o que o usuário digitou , é enviado como um par.
