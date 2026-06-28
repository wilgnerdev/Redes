## Status **Introduzindo os status codes do HTTP**

## Agora que já entendemos mais sobre como funciona a base do protocolo HTTP com os métodos e a parte de requisição e resposta, precisamos compreender alguns detalhes que são apresentados no momento em que fazemos uma requisição e obtemos uma resposta. Podemos começar com um dos pontos mais importantes, principalmente no desenvolvimento de aplicações: os *status codes* do HTTP.

## Quando seguimos um protocolo, especialmente os protocolos web, é importante entender que toda requisição obterá, antes do corpo da resposta, um status daquela resposta. Existe uma série de *status codes* que o HTTP possui, os quais podem nos ajudar a entender determinadas informações. Um dos *status codes* mais comuns que já devemos ter visto é o 404, "não encontrado". Isso ocorre, por exemplo, quando estamos acessando uma página na web e a conexão com a internet cai. O navegador não consegue retornar o site procurado e, por isso, devolve um *status code* indicando que o recurso não foi encontrado, devido a uma falha na infraestrutura. Isso ajuda o navegador a entender que, naquele momento, estamos sem conexão com a internet.

## **Explorando as categorias dos status codes HTTP**

## Da mesma forma, alguns aplicativos conseguem avisar quando estamos sem conexão, seja por ativar o modo avião ou por estar em um local sem internet. Quem garante isso são certos *status codes* do HTTP, que permitem enviar um status indicando que o recurso não foi encontrado.

## Vamos explorar as categorias dos *status codes* HTTP para entender os tipos de respostas que podemos ter a partir de cada tipo de *status code*. Quando fazemos uma solicitação, podemos obter uma série de categorias ordenadas por números. A categoria de número 100, que vai de 100 até 199, é a categoria informativa. Ou seja, a solicitação enviada devolverá uma resposta cujo objetivo é fornecer alguma informação sobre o recurso solicitado. Pode ser algo relacionado ao servidor ou a alguma configuração interna que desejamos obter. Não se trata necessariamente de obter um HTML, um JSON ou um recurso específico, mas sim de obter alguma informação sobre o recurso.

## **Detalhando os status codes informativos**

## Alguns códigos dessa faixa, de 100 a 199, incluem o *status code* "continue", que indica que podemos continuar a operação a partir daquele ponto, sendo muito usado para microserviços. Outro exemplo é o código 103, "processing", utilizado para mostrar que a solicitação ainda está em processamento, como em casos de pagamento, onde é necessário informar que a requisição ainda está em processamento.

## Agora, passando para os *status codes* que vão de 200 a 299, essa faixa é voltada para resultados corretos ou de sucesso. Geralmente, quando acessamos uma página da web e ela é carregada corretamente, obtemos o *status code* 200, que é o "OK". Esse código é utilizado para a maioria das requisições bem-sucedidas, quando o serviço consegue devolver a informação solicitada. Outros códigos dessa faixa incluem o 201, "created", muito utilizado quando enviamos informações ou fazemos um *post* na web. Há também o *status code* "accepted", que significa que a requisição foi aceita e podemos continuar. Existem detalhes específicos para cada *status code*, mas o importante é entender que a faixa de 200 a 299 representa tipos de sucesso.

## **Compreendendo os status codes de redirecionamento**

## Em seguida, temos os *status codes* de 300 a 399, que são de redirecionamento. Quando acessamos um recurso HTTP, é comum que algumas páginas sejam redirecionadas. Um exemplo simples é quando acessamos o site da Amazon digitando amazon.com e somos redirecionados para o site da Amazon Brasil. Isso ocorre em e-commerces ou páginas web com versões em vários países, onde, a partir do nosso IP, somos redirecionados para o país onde o serviço é mais otimizado. Por exemplo, podemos fazer uma compra no site da Amazon nos Estados Unidos, mas há restrições. O ideal é comprar no site da Amazon Brasil. Para esses cenários, existem códigos que indicam redirecionamento, apontando para a página correta.

## Depois, temos os *status codes* de 400, que são erros voltados à parte do cliente. Esses erros podem ocorrer por vários fatores, como digitar uma URL errada, resultando em um 404, "not found". Isso acontece quando digitamos incorretamente o endereço do site no navegador. Outros *status codes* dessa faixa incluem "não autorizado", "proibido", "requisição muito grande" ou "URL muito longa". São erros que ocorrem devido a problemas na solicitação do cliente.

## **Analisando os status codes de erro do servidor**

## Por último, temos os erros 500, que são erros de servidor. Nesse caso, a culpa não é do cliente, mas sim de um erro interno na aplicação que impede a obtenção da solicitação. Isso pode ocorrer por diversos fatores, como um bug interno ou um método ainda não construído. Esses problemas resultam em um erro 500\. É comum encontrar sites mais antigos que não escondem esses *status codes* dos clientes e apresentam "internal server error", erro 500\. Isso indica um erro interno no servidor, e é necessário aguardar uma correção para acessar o recurso adequadamente.

## Agora, vamos explorar em mais detalhes como funcionam alguns dos códigos mais utilizados pelo HTTP. Como mencionado anteriormente, temos o *status code* "continue", código 100, que indica que o servidor recebeu a solicitação e podemos continuar a partir dali. Esse código é utilizado para indicar que podemos prosseguir após uma etapa.

## **Detalhando os status codes de sucesso**

## Temos o 101, que é a troca de protocolos. Por exemplo, a troca de HTTP para HTTPS, geralmente feita por redirecionamento. Se não houver redirecionamento, o código 101 pode indicar a troca de protocolos.

## Em seguida, temos o 103\. Peço desculpas pela confusão anterior: o 102 é "processing" e o 103 é "early hints". O "early hints" apresenta os cabeçalhos que algumas requisições podem informar. Por exemplo, ao usar o método HEAD para obter informações sobre cabeçalhos de uma requisição, podemos receber o código de status 200, indicando "OK", ou o 103, que apresenta cabeçalhos de respostas antes do HTTP final.

## Agora, vamos para os *status codes* de sucesso. O principal deles é o 200, "OK", que é o mais comum. Qualquer solicitação bem-sucedida resulta em um status 200, além da resposta da requisição, que pode ser um HTML, uma imagem ou um JSON. O 201, "created", é utilizado para quando criamos um novo recurso, como adicionar um produto ao carrinho ou um novo endereço. O 204, "no content", indica que a solicitação foi bem-sucedida, mas não houve devolutiva de conteúdo. Isso é comum em atualizações *put* ou *delete*, onde não há retorno de informação. O 206, "partial content", ocorre quando apenas parte do recurso é devolvida, como em downloads ou serviços de streaming.

## **Explicando os status codes de redirecionamento**

## Agora, vamos para os *status codes* da faixa de 300\. O 301, "moved permanently", indica que um recurso foi movido permanentemente para outra página. O 302, "found", é utilizado para indicar que um recurso foi encontrado, mas geralmente não é o *status code* final. O 304, "not modified", é utilizado para verificar o status de um recurso que não foi modificado.

## Pode ser necessário, em alguns casos, ter dois campos para gerenciar o tempo de processamento. Um campo indicaria o status, para saber se o valor já foi alterado ou não, e outro mostraria em que estágio de processamento o recurso se encontra. Sabemos que existem vários *status codes* diferentes, mas eles representam coisas distintas. O processo indica que algo está em andamento, enquanto o *not modified* representa um resultado final, indicando que nada foi alterado.

## **Abordando os status codes de erro do cliente**

## Agora, vamos abordar os *status codes* de erros, 400 e 500\. Começando pelo 400, o *Bad Request* ocorre quando uma solicitação é feita de forma incorreta, o que pode acontecer por diversos motivos. Geralmente, o *Bad Request* é utilizado quando enviamos um *POST* e o corpo da requisição não corresponde ao que deveria ser enviado. Isso pode ocorrer se o navegador alterar algum recurso inadvertidamente, se uma aplicação no *front-end* fizer uma alteração no *back-end*, ou se o corpo da requisição *JSON* estiver incorreto. Nesses casos, o sistema retornará um *Bad Request*, com o *status code* 400\.

## O *status code* 401 indica que a solicitação não é autorizada. Isso ocorre quando é necessário fazer login. Por exemplo, ao tentar acessar um repositório privado no GitHub sem estar logado, o sistema retornará um 401, indicando que a autorização é necessária. Em alguns casos, o sistema pode redirecionar para a página de login, retornando um 302\. Algumas aplicações informam que o usuário não está autorizado a ver o projeto, enquanto outras redirecionam para a página de login.

## **Explorando os status codes de erro do servidor**

## O *status code* *Forbidden* ocorre quando o login foi realizado, mas o acesso a uma página específica não é permitido. Nesse cenário, o usuário pode ter autorização para acessar a aplicação, mas está proibido de acessar aquele recurso específico. Isso é comum em sistemas com diferentes papéis, como administrador, gerente, coordenador e usuário comum, onde diferentes usuários têm diferentes níveis de acesso.

## O *Not Found*, ou 404, é um clássico. Ele indica que o recurso desejado não foi encontrado. Isso pode ocorrer ao digitar um endereço incorreto na barra de endereços e tentar acessar um site inexistente.

## O *status code* 405 pode parecer que estamos apresentando mais códigos de erro do que outros, mas, de fato, ao desenvolver uma aplicação, é mais comum nos atentarmos a esses tipos de erros. Em projetos de software, há muitas discussões entre sistemas de *back-end* e *front-end* para garantir que a comunicação entre as equipes esteja correta. Os *status codes* do HTTP são fundamentais para assegurar que a comunicação está correta, seja no *front-end* ou no *back-end* da aplicação.

## **Discutindo os status codes de timeout e segurança**

## O *Request Timeout*, ou 408, ocorre quando a internet está fraca, dificultando o acesso a um recurso. Isso pode acontecer se a requisição for muito longa e não houver tempo suficiente para obter a resposta completa. Em tais casos, o sistema entra em *Request Timeout*. Isso é comum no desenvolvimento de aplicações web, onde há valores padrão no servidor para evitar travamentos em requisições muito grandes. Se necessário, o sistema pode devolver um *Timeout* e sugerir que a requisição seja dividida em partes menores.

## O *Payload Too Large*, ou 413, ocorre quando uma requisição é enviada com um *JSON* muito grande ou com muita informação. Um exemplo comum é o envio de imagens de perfil, onde alguns sistemas não conseguem comprimir a imagem e limitam o tamanho permitido. Isso também acontece com e-mails, que não podem ter anexos maiores que 25MB. O *Payload Too Large* indica que a requisição excede o tamanho máximo permitido.

## O *Too Many Requests*, ou 429, é utilizado por questões de segurança, envolvendo *rate limit*. Isso ocorre quando uma página é acessada muitas vezes em um curto período. Em vez de travar ou cortar o acesso, o sistema entra em *Too Many Requests*, indicando que o número de requisições foi excedido. Isso é mais comum em aplicações que fazem muitas requisições, como *web scraping*, ou em casos de bugs que causam múltiplas chamadas a uma API.

## **Concluindo com os status codes de erro do servidor**

## Os erros 500 são erros do servidor, não da aplicação ou do cliente. O erro 500 é o mais tradicional e pode ocorrer por diversos motivos, como bugs na aplicação, excesso de uso de memória, problemas de conexão com o banco de dados, entre outros. Quando uma exceção é lançada, o sistema retorna um erro 500 ao cliente. Se os erros estiverem na faixa dos 400, podemos corrigir a aplicação e enviar a alteração. No entanto, erros 500 dependem do servidor onde a aplicação está hospedada, tornando a correção mais complexa.

## O *Not Implemented*, ou 501, ocorre quando alguns recursos estão habilitados, mas ainda não foram implementados. Isso é comum em testes beta, onde o usuário pode testar até certo ponto, mas algumas funcionalidades ainda estão em desenvolvimento.

## O *Bad Gateway*, ou 502, ocorre quando uma requisição é considerada inválida, seja por uso interno ou externo da rede. Isso pode acontecer devido a configurações incorretas de rede, como endereços IP errados, resultando em um *Bad Gateway*.

## O *Service Unavailable*, ou 503, é utilizado quando um serviço está em manutenção. Serviços web críticos precisam estar disponíveis 99,99% do tempo, o que significa que podem ficar indisponíveis por, no máximo, seis minutos por ano. Durante manutenções programadas, o sistema pode retornar um 503, indicando que o serviço está temporariamente indisponível.

## **Resumindo a importância dos status codes**

## Em resumo, os *status codes* são essenciais para orientar quem está consumindo a aplicação, seja um *front-end* ou alguém acessando a URL diretamente. Eles ajudam a seguir o protocolo HTTP e a garantir que o cliente entenda como a aplicação funciona. Existem guias e boas práticas sobre como cada *endpoint* deve lidar com os *status codes*. A documentação do MDN, mantida pela Mozilla, é uma excelente referência para entender os *status codes* e o protocolo HTTP.