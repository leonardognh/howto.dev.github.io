# RegExp

O objeto `RegExp` é usado para correspondência de strings com Expressões Regulares. Uma Expressão Regular é uma string especial, chamada de padrão, que usa várias sequências de caracteres para definir as características a serem correspondidas em uma sequência de caracteres dentro de outra string.

Um objeto `RegExp` também pode ter flags configuradas junto com um padrão para mudar como as correspondências são realizadas.

## Sintaxe

Existem dois métodos para criar um objeto `RegExp`. O primeiro método é a notação literal usando barras para delimitar o padrão, seguido por quaisquer flags. O segundo método usa o construtor `RegExp`, que leva o padrão como o primeiro argumento e quaisquer flags como o segundo.

```
// Usando notação literal
let re1 = /foo?/i;

// Usando o construtor RegExp
let re2 = new RegExp('foo?', 'i');

// Ambos criam um objeto RegExp com um padrão = "foo?" e uma flag = "i"
```

Há uma diferença entre os métodos. A notação literal compila quando a expressão é avaliada. Ela deve ser usada quando o padrão permanecerá constante, para não ser recompilada desnecessariamente, como em um loop.

Usar o construtor de objeto significa que a expressão será compilada em tempo de execução. Deve ser usado quando o padrão do objeto RegExp estiver sujeito a mudanças, ou o padrão for obtido em tempo de execução, como de uma entrada do usuário.

### Propriedades do RegExp

| Propriedade | Descrição                                                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| .flags      | Retorna uma string contendo as flags do objeto RegExp.                                                                                     |
| .dotAll     | O . corresponde a novas linhas ou não?                                                                                                     |
| .global     | O objeto RegExp testa todas as correspondências em uma string ou apenas a primeira?                                                        |
| .hasIndices | O resultado da Expressão Regular expõe os índices de início e fim das substrings capturadas?                                               |
| .ignoreCase | O objeto RegExp ignora maiúsculas e minúsculas ao realizar uma correspondência?                                                            |
| .multiline  | O objeto RegExp realiza correspondências em várias linhas?                                                                                 |
| .source     | O texto do padrão usado pelo objeto RegExp.                                                                                                |
| .sticky     | A pesquisa é rígida? (A próxima correspondência tem que ocorrer em lastIndex ou podemos corresponder a próxima ocorrência após lastIndex?) |
| .unicode    | Os recursos Unicode estão habilitados?                                                                                                     |
| .lastIndex  | O índice no qual começar a próxima correspondência.                                                                                        |

### Métodos do RegExp

| Método     | Descrição                                |
| ---------- | ---------------------------------------- |
| .exec(str) | Executa uma busca na string str.         |
| .test(str) | Testa uma correspondência na string str. |

### Métodos da String que Podem Usar Objetos RegExp

Nos exemplos abaixo, re é um objeto RegExp.

| Método               | Descrição                                                                  |
| -------------------- | -------------------------------------------------------------------------- |
| .match(re)           | Retorna o array resultado das correspondências na string.                  |
| .matchAll(re)        | Retorna um iterador de todas as correspondências encontradas na string.\*  |
| .replace(re, substr) | Substitui correspondências na string por uma substring dada, substr.       |
| .search(re)          | Retorna o índice da primeira correspondência na string.                    |
| .split(re)           | Divide a string em um array usando as correspondências como delimitadores. |

O objeto RegExp deve ter a flag g definida ou uma exceção é lançada.

### Flags do RegExp

Quando especificadas, essas flags mudam o comportamento padrão da correspondência do objeto RegExp.

| Flag | Descrição                                                                                                        |
| ---- | ---------------------------------------------------------------------------------------------------------------- |
| g    | Realiza uma correspondência global, encontrando todas as correspondências em vez de apenas a primeira.           |
| i    | Torna as correspondências insensíveis a maiúsculas e minúsculas. Corresponde tanto maiúsculas quanto minúsculas. |
| m    | Realiza correspondências em várias linhas. (Muda o comportamento de ^,$)                                         |
| s    | Permite que . corresponda a caracteres de nova linha.                                                            |
| u    | Habilita suporte a Unicode.                                                                                      |
| y    | As correspondências são rígidas, procurando apenas na posição exata no texto.                                    |

Uso:

```
let re1 = /foo?/gim;

let re2 = new RegExp('foo?', 'gim');

// Cria um objeto RegExp que realiza uma busca global, insensível a maiúsculas e minúsculas, em várias linhas
```

## Expressões Regulares

Os seguintes caracteres são usados para definir uma string de Expressão Regular.

### Aserções

Os seguintes correspondem às fronteiras entre caracteres, não aos próprios caracteres.

| Caracteres | Significado                                                                                                                                                                                                     |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ^          | Corresponde ao início da entrada. Em busca de várias linhas, corresponde imediatamente após um caractere de quebra de linha.                                                                                    |
| $          | Corresponde ao final da entrada. Em busca de várias linhas, corresponde imediatamente antes de um caractere de quebra de linha.                                                                                 |
| \b         | Corresponde a uma fronteira de palavra. Ponto onde um caractere de palavra não é seguido por outro caractere de palavra ou o ponto onde um caractere de palavra não é precedido por outro caractere de palavra. |
| \B         | Corresponde a uma fronteira não-palavra. Ponto onde o caractere precedente e o seguinte são do mesmo tipo.                                                                                                      |

Os seguintes correspondem a um caractere ou expressão com base no que segue ou precede.

| Caracteres | Significado                                                                                                         |
| ---------- | ------------------------------------------------------------------------------------------------------------------- |
| x(?=y)     | Corresponde x apenas se x for seguido imediatamente por y. y não faz parte dos resultados da correspondência.       |
| x(?!y)     | Corresponde x apenas se x não for seguido imediatamente por y. y não faz parte dos resultados da correspondência.   |
| (?<=y)x    | Corresponde x apenas se x for precedido imediatamente por y. y não faz parte dos resultados da correspondência.     |
| (?<!y)x    | Corresponde x apenas se x não for precedido imediatamente por y. y não faz parte dos resultados da correspondência. |

Exemplos

```
let str = 'Sally sells seashells by the seashore';
let re = /s(?=e)/gi;
console.log(str.replace(re, 'x'));
// Saída: Sally xells xeashells by the xeashore

re = /s(?!e)/gi;
console.log(str.replace(re, 'x'));
// Saída: xally sellx seaxhellx by the seaxhore

re = /^s/gi;
console.log(str.replace(re, 'x'));
// Saída: xally sells seashells by the seashore

re = /\Bs/gi;
console.log(str.replace(re, 'x'));
// Saída: Sally sellx seaxhellx by the seaxhore
```

### Classes de Caracteres

Classes de caracteres especificam um tipo de caractere a ser correspondido.

| Caracteres | Significado                                                                                                                               |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| .          | Corresponde a qualquer caractere exceto terminadores de linha. Quando a flag s está definida, também corresponde a terminadores de linha. |
| \d         | Corresponde a qualquer dígito (número arábico).                                                                                           |
| \D         | Corresponde a qualquer caractere que não seja um dígito (número arábico).                                                                 |
| \w         | Corresponde a qualquer caractere alfanumérico do alfabeto latino, incluindo sublinhado.                                                   |
| \W         | Corresponde a qualquer caractere que não seja um caractere alfanumérico do alfabeto latino ou sublinhado.                                 |
| \s         | Corresponde a qualquer caractere de espaço em branco (espaço, tabulação, nova linha, espaço não separável e similares).                   |
| \S         | Corresponde a qualquer caractere que não seja um caractere de espaço em branco.                                                           |
| \t         | Corresponde a uma tabulação horizontal.                                                                                                   |
| \r         | Corresponde a um retorno de carro.                                                                                                        |
| \n         | Corresponde a uma alimentação de linha.                                                                                                   |
| \v         | Corresponde a uma tabulação vertical.                                                                                                     |
| \f         | Corresponde a uma alimentação de formulário.                                                                                              |
| \b         | Corresponde a um backspace.                                                                                                               |
| \0         | Corresponde a um caractere NUL (quando não seguido por outro dígito).                                                                     |
| \xnn       | Corresponde ao código de caractere nn (dois dígitos hexadecimais).                                                                        |
| \unnnn     | Corresponde a uma unidade de código UTF-16 com o valor nnnn (quatro dígitos hexadecimais).                                                |
| \          | Seguido por um caractere especial, significa que o caractere deve ser correspondido literalmente.                                         |

Exemplo

```
let str = '2001: A Space Odyssey';

let re = /\W/gi;
console.log(str.replace(re, 'x'));
// Saída: 2001xxAxSpacexOdyssey

re = /\d/gi;
console.log(str.replace(re, 'x'));
// Saída: xxxx: A Space Odyssey

re = /\d\D/gi;
console.log(str.replace(re, 'x'));
// Saída: 200x A Space Odyssey
```

### Grupos e Intervalos

Indica grupos e intervalos de caracteres para combinar.

| Caracteres   | Significado                                                                                                                    |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `x (pipe) y` | Combina x ou y.                                                                                                                |
| `[xyz]`      | Combina o caractere x, y ou z.                                                                                                 |
| `[a-c]`      | Combina o caractere que está entre a e c inclusive (a, b e c).                                                                 |
| `[^xyz]`     | Combina o caractere que não é x, y ou z.                                                                                       |
| `[^a-c]`     | Combina o caractere que não está entre a e c inclusive (não a, b ou c).                                                        |
| `(x)`        | Combina x e lembra o resultado, capturando o grupo.                                                                            |
| `\n`         | Onde n é um inteiro positivo, representa uma referência inversa à última substring que corresponde ao n-ésimo grupo capturado. |
| `(?<Name>x)` | Combina x e armazena no objeto de grupos das correspondências retornadas sob o nome Nome.                                      |
| `\k<Name>`   | Representa uma referência inversa à última substring correspondente no grupo de captura nomeado especificado por Nome.         |
| `(?)`        | Representa um grupo de não captura. Combina x, mas não lembra o resultado.                                                     |

\* (pipe) significa |

Se o hífen estiver no início ou no final da sequência entre colchetes, é tratado como um hífen literal.

Exemplo

```
let str = 'Peter Piper picked a peck of pickled peppers.';

let re = /[aeiou]/gi;
console.log(str.replace(re, 'x'));
// Saída: Pxtxr Pxpxr pxckxd x pxck xf pxcklxd pxppxrs.

re = /[^p]/gi;
console.log(str.replace(re, 'x'));
// Saída: PxxxxxPxpxxxpxxxxxxxxpxxxxxxxpxxxxxxxpxppxxxx

re = /pi(ck|pe)/gi;
console.log(str.replace(re, 'x'));
// Saída: Peter xr xed a peck of xled peppers.

```

### Quantificadores

Os quantificadores especificam o número de caracteres ou expressões a serem combinados.

| Caracteres | Significado                                                                                                              |
| ---------- | ------------------------------------------------------------------------------------------------------------------------ |
| x\*        | Combina o item precedente x zero ou mais vezes.                                                                          |
| x+         | Combina o item precedente x uma ou mais vezes.                                                                           |
| x?         | Combina o item precedente x zero ou uma vez.                                                                             |
| x{n}       | Combina o item precedente x n vezes, onde n é um inteiro positivo.                                                       |
| x{n,}      | Combina o item precedente x n ou mais vezes, onde n é um inteiro positivo.                                               |
| x{n,m}     | Combina o item precedente x pelo menos n vezes e no máximo m vezes, onde n e m são inteiros positivos e n é menor que m. |

Por padrão, esses quantificadores são gananciosos, correspondendo o máximo possível da string. Seguindo o quantificador com `? (x\*?)`, a correspondência será interrompida em sua primeira ocorrência.

Exemplo

```
let str = 'Billy bought a bushel of blue balloons.';

let re = /b.?l+/gi;
console.log(str.replace(re, 'x'));
// Saída: xy bought a bushel of xue xoons.

re = /[olu]{2}/gi;
console.log(str.replace(re, 'x'));
// Saída: Bixy bxght a bushel of bxe baxxns.

re = /l\w*/gi;
console.log(str.replace(re, 'x'));
// Saída: Bix bought a bushex of bx bax.

re = /o\w+?/gi;
console.log(str.replace(re, 'x'));
// Saída: Billy bxght a bushel x blue balxns.
```
