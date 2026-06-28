## Métodos HTTP

## **Explicando a analogia com os correios**

Agora que entendemos que precisamos ter uma informação base que será o nosso cabeçalho da requisição, podemos fazer uma analogia com os correios. Assim como precisamos deixar em cima de um pacote a informação de para quem será enviado e de onde veio, também precisamos declarar o que estamos enviando. Dessa forma, temos o corpo da requisição, que é de fato o pacote que está sendo enviado.

Precisamos entender que existem métodos que devem ser enviados em cada requisição. Assim como nos correios, é necessário definir qual é o tipo de método de envio que será utilizado quando compramos ou enviamos algo. Ao enviar algo pelo correio, é preciso declarar o tipo de envio, o que ajuda a definir se o pacote que estamos utilizando pode ou não seguir as regras de envio selecionadas. Da mesma forma, trabalhamos com o HTTP ao pensar no envio de uma requisição.

## **Introduzindo os métodos HTTP**

Existem alguns métodos que definem o tipo de requisição que estamos fazendo. Vimos anteriormente os métodos GET e POST, que são os mais comuns, mas é interessante conhecermos os outros métodos e como funcionam.

Entre os métodos HTTP, começamos pelo GET, localizado no canto superior esquerdo. O método GET é o padrão. Quando digitamos uma informação na URL do navegador, toda requisição é um GET. Toda solicitação de informação pela URL é um método GET. Ele é o método padrão utilizado para buscar qualquer outra informação. Ao abrir um navegador e buscar uma requisição, independentemente da página web que estamos acessando, estamos utilizando um método GET.

## **Explorando os métodos POST, PUT e PATCH**

No canto superior direito, temos o método POST, que é amplamente utilizado para formulários ou para criar um recurso. Por exemplo, ao adicionar um produto ao carrinho em um site como a Amazon, ocorre um POST. Quando removemos algo do carrinho, também pode ocorrer um POST. Ao preencher um formulário para assinar uma newsletter ou clicar em "play" em um curso, qualquer solicitação que modifique algo no servidor é feita através de um POST.

No canto inferior direito, temos o método PUT, que, junto com o PATCH, realiza modificações em um recurso. Por exemplo, se quisermos atualizar um carrinho na Amazon, podemos usar o PUT para substituir todo o carrinho. Se desejarmos apenas alterar a quantidade de um produto específico, utilizamos o PATCH, que atualiza apenas a quantidade desse produto. Essa é a diferença entre PUT e PATCH.

## **Descrevendo os métodos DELETE, OPTIONS e HEAD**

No canto inferior esquerdo, temos o método DELETE, que serve para remover um recurso. Caso queiramos eliminar um recurso do servidor, utilizamos o DELETE. Os métodos mais utilizados são GET, POST, PUT, DELETE e PATCH.

Além desses, temos o OPTIONS e o HEAD, que são menos utilizados. O método HEAD retorna apenas o cabeçalho de qualquer requisição, sem o recurso solicitado. Por exemplo, ao usar o HEAD em uma página web, recebemos apenas o cabeçalho. O método OPTIONS apresenta as opções disponíveis para solicitar um recurso, indicando quais métodos podem ser utilizados, como GET, POST, PUT, PATCH, DELETE ou HEAD. Ele define o que é permitido ou não em uma página.

## **Ressaltando a importância dos métodos HTTP**

É importante entender que os métodos HTTP devem ser seguidos corretamente para garantir o funcionamento adequado de uma aplicação web. Existem recursos que facilitam a adesão às convenções do protocolo HTTP, como acompanhar os métodos HTTP. Posteriormente, abordaremos os STATUS CODE, que são parte da resposta de uma requisição e nos fornecem um status que podemos usar para monitorar a requisição.

