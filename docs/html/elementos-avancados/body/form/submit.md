# Elementos Avançados: Body

## Botão Submit Formulário

<style>
.button {
  border: 1px solid black;
  
  transition-duration: 0.1s;
}
.button:hover {
  background-color: #A6F4FF; 
  border: 1px solid #26A0DA;
}
</style>

Lembre-se de que o objetivo de um formulário é coletar informações que serão enviadas. Essa é a função do botão enviar – os usuários clicam nele quando terminam de preencher as informações no `<form>` e estão prontos para enviá-las. Agora que já vimos como criar vários elementos de entrada, vamos ver como criar um botão de envio!

Para fazer um botão de envio em um `<form>`, usaremos o elemento `<input>` confiável e definiremos o tipo como "enviar". Por exemplo:

```
<form>
  <input type="submit" value="Enviar">
</form>
```

<form>
  <input class="button" type="submit" value="Enviar">
</form>

Observe no trecho de código que o valor atribuído ao `<input>` aparece como texto no botão enviar. Se não houver um atributo de valor, o texto padrão, Enviar, aparecerá no botão.
