# Elementos Iniciais: Body

### Textos `<p>` / Intervalo `<span>`

Se quiser exibir texto em HTML, você pode usar um parágrafo ou intervalo:

Parágrafos `<p>` contêm um bloco de texto simples.
`<span>` contém pequenos trechos de texto ou outro HTML. Eles são usados ​​para separar pequenos pedaços de conteúdo que estão na mesma linha de outro conteúdo.
Dê uma olhada em cada um desses elementos em ação abaixo:

```
<div>
  <h1>Tecnologia</h1>
</div>
<div>
  Prevê-se que <p><span>carros autônomos</span> substituam até 2 milhões
  de empregos nas próximas duas décadas.</p>
</div>
```

No exemplo acima, existem dois `<div>` diferentes. O segundo `<div>` contém um `<p>` com `<span>`Carros autônomos`</span>`. Este elemento `<span>` separa “Carros autônomos” do restante do texto do parágrafo.

É melhor usar um elemento `<span>` quando você deseja direcionar um conteúdo específico que está embutido ou na mesma linha de outro texto. Se você quiser dividir seu conteúdo em blocos, é melhor usar um `<div>`.
