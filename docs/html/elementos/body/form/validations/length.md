{!import-css/button.md!}
{!import-css/input.md!}

# Elementos Avançados: Body

## Validações Inputs: MinLength e MaxLength

No exercício anterior, conseguimos usar min e max para definir valores mínimos e máximos aceitáveis ​​em um campo numérico. Mas e quanto aos campos de texto? Certamente há casos em que não queremos que nossos usuários digitem mais do que um certo número de caracteres (pense no limite de caracteres para mensagens no Twitter). Podemos até querer definir um número mínimo de caracteres. Convenientemente, há validações HTML5 integradas para essas situações.

Para definir um número mínimo de caracteres para um campo de texto, adicionamos o atributo minlength e um valor para definir um valor mínimo. Da mesma forma, para definir o número máximo de caracteres para um campo de texto, usamos o atributo maxlength e definimos um valor máximo. Vamos dar uma olhada nesses atributos no código:

```
<form>
  <label for="resumo">Exemplo até 10 caracteres</label>
  <input id="resumo" name="resumo" type="text" minlength="5" maxlength="10" required>
  <input type="submit" value="Enviar">
</form>
```

<form>
  <label for="resumo">Exemplo até 10 caracteres</label>
  <input class="border" id="resumo" name="resumo" type="text" minlength="5" maxlength="10" required>
  <input class="button" type="submit" value="Enviar">
</form>

Se um usuário tentar enviar o `<form>` com menos do que o mínimo definido, uma mensagem irá aparecer pedindo que insira a quantidade mínima de caracteres.

E se um usuário tentar digitar mais do que o número máximo permitido de caracteres, ele não receberá uma mensagem de aviso, mas não poderá digitar mais!
