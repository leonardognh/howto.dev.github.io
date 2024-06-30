{!import-css/button.md!}
{!import-css/input.md!}

# Elementos Avançados: Body

## Validações Inputs: Min-Max

Outra validação interna que podemos usar é atribuir um valor mínimo ou máximo para um campo numérico, por exemplo, `<input type="number">` e `<input type="range">`. Para definir um valor mínimo aceitável, usamos o atributo min e atribuímos um valor. Por outro lado, para definir um valor máximo aceitável, atribuímos um valor ao atributo max. Vamos ver isso no código:

```
<form >
  <label for="convidados">Digite o número de convidados:</label>
  <input id="convidados" name="convidados" type="number" min="1" max="4">
  <input type="submit" value="Enviar">
</form>
```

<form >
  <label for="convidados">Digite o número de convidados:</label>
  <input class="border" id="convidados" name="convidados" type="number" min="1" max="4">
  <input class="button" type="submit" value="Enviar">
</form>
Se um usuário tentar enviar uma entrada menor que 1, um aviso aparecerá: prompt em um campo numérico para o usuário inserir um valor maior ou igual a 1

Uma mensagem semelhante aparecerá se um usuário tentar inserir um número maior que 4. Vamos ver agora esta ação.
