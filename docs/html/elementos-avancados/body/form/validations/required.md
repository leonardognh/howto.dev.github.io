# Elementos Avançados: Body

## Validações Inputs: Required

<style>
.button {
  border: 1px solid black;
  
  transition-duration: 0.1s;
}
.button:hover {
  background-color: #A6F4FF; 
  border: 1px solid #26A0DA;
}
.border {
  border: 1px solid black
}
</style>

Às vezes temos campos em nossos `<form>s` que não são opcionais, ou seja, devem ser fornecidas informações antes de podermos enviá-las. Para fazer cumprir esta regra, podemos adicionar o atributo obrigatório a um elemento `<input>`.

Considere por exemplo:

```
<form>
  <label for="alergias">Você tem alguma restrição alimentar?</label>
  <br>
  <input id="alergias" name="alergias" tipo="text" required>
  <br>
  <input type="submit" value="Enviar">
</form>
```

<form>
  <label for="alergias">Você tem alguma restrição alimentar?</label>
  <br>
  <input class="border" id="alergias" name="alergias" tipo="text" required>
  <br>
  <input class="button" type="submit" value="Enviar">
</form>

O estilo da mensagem varia de navegador para navegador.
