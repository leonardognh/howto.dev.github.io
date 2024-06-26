# Elementos Avançados: Tag `<body>`

## Formulário `<form>`

Podemos pensar na internet como uma rede de computadores que enviam e recebem informações. Os computadores precisam de uma solicitação HTTP para saber como se comunicar. A solicitação HTTP instrui o computador receptor sobre como lidar com as informações recebidas. Mais informações podem ser encontradas em nosso artigo sobre solicitações HTTP.

O elemento `<form>` é uma ótima ferramenta para coletar informações, mas então precisamos enviar essas informações para outro lugar para processamento. Precisamos fornecer ao elemento `<form>` o local para onde vão as informações do `<form>` e qual solicitação HTTP fazer. Dê uma olhada no exemplo `<form>` abaixo:

```
<form action="/example.html" método="POST">
</form>
```

No exemplo acima, criamos o esqueleto de um `<form>` que enviará informações para example.html como uma solicitação POST:

O atributo action determina para onde as informações são enviadas.
O atributo method recebe um verbo HTTP que está incluído na solicitação HTTP.
Observação: verbos HTTP como POST não precisam estar em letras maiúsculas para que a solicitação funcione, mas isso é feito fora da convenção. No exemplo acima poderíamos ter escrito method="post" e ainda funcionaria.

O elemento `<form>` também pode conter elementos filhos. Por exemplo, seria útil fornecer um cabeçalho para que os usuários saibam do que se trata este `<form>`. Também poderíamos adicionar um parágrafo para fornecer ainda mais detalhes. Vamos ver um exemplo disso no código:

```
<form action="/example.html" método="POST">
  <h1>Criando um formulário</h1>
  <p>Parece que você quer aprender como criar um formulário HTML. Bem, a melhor maneira de aprender é brincar com isso.</p>
</form>
```

O exemplo acima não coleta nenhuma entrada do usuário, mas faremos isso no próximo exercício. Por enquanto, vamos praticar a criação da base de um `<form>` HTML!
