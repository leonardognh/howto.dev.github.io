# Elementos Avançados: Body

Existem muitos sites na Internet que exibem informações como preços de ações, resultados esportivos, dados de faturas e muito mais. Esses dados são de natureza tabular, o que significa que uma tabela geralmente é a melhor maneira de apresentar os dados.

Antes de exibir os dados, devemos primeiro criar a tabela que conterá os dados usando o elemento `<table>`.

```
<table>

</table>
```

O elemento `<table>` conterá todos os dados tabulares que planejamos exibir.

Em muitos programas que usam tabelas, a tabela já está predefinida para você, o que significa que ela contém as linhas, colunas e células que conterão os dados. Em HTML, todos esses componentes devem ser criados.

A primeira etapa para inserir dados na tabela é adicionar linhas usando o elemento de linha da tabela: `<tr>`.

```
<table>
  <tr>
  </tr>
  <tr>
  </tr>
</table>
```

As linhas não são suficientes para adicionar dados a uma tabela. Cada elemento da célula também deve ser definido. Em HTML, você pode adicionar dados usando o elemento de dados da tabela: `<td>`.

```
<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```

No exemplo acima, dois pontos de dados (73 e 81) foram inseridos na única linha que existe. Ao adicionar dois pontos de dados, criamos duas células de dados.

<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

Os dados da tabela não fazem muito sentido sem títulos para descrever o que os dados representam.

Para adicionar títulos a linhas e colunas, você pode usar o elemento de cabeçalho da tabela: `<th>`.

O elemento de cabeçalho da tabela é usado como um elemento de dados de tabela, exceto com um título relevante. Assim como os dados da tabela, o cabeçalho da tabela deve ser colocado dentro de uma linha da tabela.

```
<table>
  <tr>
    <th></th>
    <th scope="col">Sábado</th>
    <th scope="col">Domingo</th>
  </tr>
  <tr>
    <th scope="row">Temperatura</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```

Uma nova linha foi adicionada para conter os três títulos: um título em branco, um título de sábado e um título de domingo. O cabeçalho em branco cria a célula extra da tabela necessária para alinhar corretamente os títulos da tabela sobre os dados aos quais correspondem.

Na segunda linha, um cabeçalho de tabela foi adicionado como título de linha: Temperatura.

Quando renderizado, este código aparecerá semelhante à tabela abaixo:

<table>
  <tr>
    <th></th>
    <th scope="col">Sábado</th>
    <th scope="col">Domingo</th>
  </tr>
  <tr>
    <th scope="row">Temperatura</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

Observe, também, o uso do atributo scope, que pode assumir um de dois valores:

linha - este valor deixa claro que o título é para uma linha.

col - este valor deixa claro que o título é para uma coluna.

O código HTML para tabelas pode parecer um pouco estranho no início, mas analisá-lo peça por peça ajuda a tornar o código mais compreensível.
