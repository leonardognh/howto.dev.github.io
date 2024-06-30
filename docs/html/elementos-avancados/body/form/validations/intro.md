# Elementos Avançados: Body

## Validações

Você já se perguntou como uma página de login realmente funciona? Ou por que a combinação de nome de usuário e senha concede acesso a um site? As respostas estão na validação. Validação é o conceito de verificar os dados fornecidos pelo usuário em relação aos dados necessários.

Existem diferentes tipos de validação. Um tipo é a validação do lado do servidor, que acontece quando os dados são enviados para outra máquina (normalmente um servidor) para validação. Um exemplo desse tipo de validação é a utilização de uma página de login. O formulário na página de login aceita a entrada de nome de usuário e senha e, em seguida, envia os dados para um servidor que verifica se o par corresponde corretamente.

Por outro lado, usamos a validação do lado do cliente se quisermos verificar os dados no navegador (o cliente). Essa validação ocorre antes dos dados serem enviados ao servidor. Navegadores diferentes implementam a validação do lado do cliente de maneira diferente, mas levam ao mesmo resultado.

Compartilhados entre os diferentes navegadores estão os benefícios de usar a validação integrada do lado do cliente do HTML5. Isso nos poupa tempo de ter que enviar informações ao servidor e esperar que o servidor envie de volta a confirmação ou rejeição dos dados. Isso também pode nos ajudar a proteger nosso servidor contra códigos maliciosos ou dados de um usuário mal-intencionado. Também nos permite fornecer feedback rapidamente aos usuários sobre campos específicos, em vez de fazê-los preencher um formulário novamente se os dados inseridos no formulário forem rejeitados.

Nesta lição, aprenderemos como adicionar algumas verificações de validação aos nossos `<form>s`!
