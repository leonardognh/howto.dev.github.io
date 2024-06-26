# Elementos Avançados: Body

## Tabela Muitos Dados `<table> <thead> <tbody> <tfooter>`

Com o tempo, uma tabela pode crescer e conter muitos dados e tornar-se muito longa. Quando isso acontece, a tabela pode ser seccionada para facilitar o gerenciamento.

Tabelas longas podem ser seccionadas usando o elemento do corpo da tabela: `<tbody>`.

O elemento `<tbody>` deve conter todos os dados da tabela, excluindo os títulos da tabela.

```
<table>
  <tbody>
    <tr>
      <th></th>
      <th>Sábado</th>
      <th>Domingo</th>
    </tr>
    <tr>
      <th>Manhã</th>
      <td rowspan="2">Trabalho</td>
      <td rowspan="3">Relaxe</td>
    </tr>
    <tr>
     <th>Tarde</th>
    </tr>
    <tr>
      <th>Noite</th>
      <td>Jantar</td>
    </tr>
  </tbody>
</table>
```

No exemplo acima, todos os dados da tabela estão contidos em um elemento do corpo da tabela. Observe, porém, que os títulos também foram mantidos no corpo da tabela.

```
<table>
  <thead>
    <tr>
      <th></th>
      <th scope="col">Sábado</th>
      <th scope="col">Domingo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Manhã</th>
      <td rowspan="2">Trabalho</td>
      <td rowspan="3">Relaxe</td>
    </tr>
    <tr>
     <th scope="row">Tarde</th>
    </tr>
    <tr>
      <th scope="row">Noite</th>
      <td>Jantar</td>
    </tr>
  </tbody>
</table>
```

No exemplo acima, o único elemento novo é `<thead>`. Os títulos da tabela estão contidos neste elemento. Observe que o cabeçalho da tabela ainda requer uma linha para conter os títulos da tabela.

Além disso, apenas os títulos das colunas ficam abaixo do elemento `<thead>`. Podemos usar o atributo scope em elementos `<th>` para indicar se um elemento `<th>` está sendo usado como título de "col" ou "row".

A parte inferior de uma tabela longa também pode ser seccionada usando o elemento `<tfoot>`.

```
<table>
  <thead>
    <tr>
      <th>Trimestre</th>
      <th>Receita</th>
      <th>Custos</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1º trimestre</th>
      <td>US$ 10 milhões</td>
      <td>US$ 7,5 milhões</td>
    </tr>
    <tr>
      <th>2º trimestre</th>
      <td>US$ 12 milhões</td>
      <td>US$ 5 milhões</td>
    </tr>
  </tbody>
  <tfooter>
    <tr>
      <th>Total</th>
      <td>US$ 22 milhões</td>
      <td>US$ 12,5 milhões</td>
    </tr>
  </tfoot>
</table>
```

No exemplo acima, o rodapé contém os totais dos dados da tabela. Os rodapés costumam ser usados ​​para conter somas, diferenças e outros resultados de dados.

<table>
  <thead>
    <tr>
      <th>Trimestre</th>
      <th>Receita</th>
      <th>Custos</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1º trimestre</th>
      <td>US$ 10 milhões</td>
      <td>US$ 7,5 milhões</td>
    </tr>
    <tr>
      <th>2º trimestre</th>
      <td>US$ 12 milhões</td>
      <td>US$ 5 milhões</td>
    </tr>
  </tbody>
  <tfooter>
    <tr>
      <th>Total</th>
      <td>US$ 22 milhões</td>
      <td>US$ 12,5 milhões</td>
    </tr>
  </tfoot>
</table>
