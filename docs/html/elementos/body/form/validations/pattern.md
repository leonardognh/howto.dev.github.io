{!import-css/button.md!}
{!import-css/input.md!}

# Elementos Avançados: Body

## Validações Inputs: Pattern

Além de verificar o comprimento de um texto, também poderíamos adicionar uma validação para verificar como o texto foi fornecido. Para casos em que queremos que a entrada do usuário siga diretrizes específicas, usamos o atributo pattern e atribuímos a ele uma expressão regular, ou regex. Expressões regulares são uma sequência de caracteres que compõem um padrão de pesquisa. Se a entrada corresponder à regex, o formulário pode ser enviado.

Digamos que queremos verificar um número de cartão de crédito válido (um número de 14 a 16 dígitos). Poderíamos usar a regex: [0-9]{14,16} que verifica se o usuário forneceu apenas números e que ele inseriu pelo menos 14 dígitos e no máximo 16 dígitos.

Para adicionar isso a um formulário:

```
<form>
  <label for="pagamento">Número do telefone (sem espaços):</label>
  <br>
  <input id="pagamento" name="pagamento" type="text" required pattern="[0-9]{8,9}">
  <input type="submit" value="Enviar">
</form>
```

<form>
  <label for="pagamento">Número do telefone (sem espaços):</label>
  <br>
  <input class="border" id="pagamento" name="pagamento" type="text" required pattern="[0-9]{8,9}">
  <input class="button" type="submit" value="Enviar">
</form>

Com o padrão em vigor, os usuários não podem enviar o `<form>` com um número que não siga o regex. Quando eles tentarem, verão uma mensagem de validação.

Se você quiser saber mais sobre o Regex, [clique aqui](regex.md).
