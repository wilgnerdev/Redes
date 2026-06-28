## Modelo cliente-servidor

## **Compreendendo a infraestrutura da web**

Já compreendemos como funciona toda a infraestrutura da web, desde o processo em que uma solicitação do navegador chega ao servidor e retorna como uma resposta. Exploramos diversos aspectos desse processo, incluindo o funcionamento dos modelos de rede, o protocolo TCP/IP, a resolução de DNS, entre outros. Para que tudo isso funcione adequadamente, as aplicações que desenvolvemos para a internet precisam estar alinhadas com essas funcionalidades.

O modelo de aplicação web possui particularidades distintas de uma aplicação console ou desktop, pois precisa operar em conjunto com a internet. Vamos explorar a construção dessas aplicações. Em geral, as aplicações seguem um modelo chamado cliente-servidor. Este modelo é composto por um cliente, que solicita os recursos, e um servidor, que disponibiliza esses recursos para a aplicação.

## **Exemplificando o modelo cliente-servidor**

Um exemplo comum de projeto que utiliza o modelo cliente-servidor são os jogos online. Quando baixamos e jogamos um jogo como Fortnite, por exemplo, o cliente é a parte que está instalada em nossos dispositivos, enquanto o servidor gerencia o jogo para todos os jogadores simultaneamente. Essa distinção entre uma aplicação local que se comunica pela internet e um repositório central que gerencia tudo é o que chamamos de aplicação cliente-servidor.

É comum ouvirmos que um jogo "caiu" quando a empresa responsável desativa os servidores, fazendo com que o jogo online deixe de funcionar, pois os recursos online não estão mais disponíveis. No modelo cliente-servidor, o servidor, geralmente controlado pela empresa desenvolvedora do jogo, é responsável por manter o funcionamento dos recursos online.

## **Funcionamento do modelo cliente-servidor**

Resumidamente, o modelo cliente-servidor é uma forma de criar aplicações onde existem dois atores principais: o cliente, que consome os serviços e solicita sua disponibilização, e o servidor, que fornece esses serviços. Isso pode ocorrer em um navegador, em uma aplicação móvel ou desktop que utiliza recursos da internet.

Vamos entender melhor como o modelo cliente-servidor funciona. Basicamente, ele não difere muito do processo de uma aplicação web ou do funcionamento geral da internet.

## **Hospedando uma aplicação web**

Temos a possibilidade de o usuário digitar uma URL ou acessar uma página da aplicação móvel, o que desencadeará o efeito de o recurso ser solicitado a um servidor. Esse servidor processará a solicitação e enviará uma resposta de volta, seja no navegador ou no aplicativo.

Agora, vamos hospedar uma aplicação para entender como funciona a questão de uma aplicação cliente-servidor. Estamos utilizando um HTML padrão, index.html, com uma aplicação simples, apenas um HTML com um CSS mínimo, contendo a mensagem "Hello World". Nada muito diferente do que já vimos em *front-end*. A única preocupação aqui é o uso de uma extensão que permitirá hospedar esta aplicação.

## **Visualizando o código HTML**

Para ilustrar isso, vamos ver o código HTML que estamos utilizando:

Copiar

\<\!DOCTYPE html\>  
\<html lang\="pt-BR"\>  
\<head\>  
    \<meta charset\="UTF-8"\>  
    \<meta name\="viewport" content\="width=device-width, initial-scale=1.0"\>  
    \<title\>Olá, Mundo\!\</title\>  
    \<style\>  
        body {  
            display: flex;  
            justify-content: center;  
            align-items: center;  
            height: 100vh;  
            margin: 0;  
            background-color: \#f0f0f0;  
            font-family: Arial, sans-serif;  
        }

        h1 {  
            color: \#333;  
            font-size: 3rem;  
        }  
    \</style\>  
\</head\>  
\<body\>  
    \<h1\>Olá, Mundo\!\</h1\>  
\</body\>  
\</html\>

## **Explicando o conceito de hospedagem**

O que significa hospedar esta aplicação? Diferentemente de uma aplicação *desktop*, que é instalada, uma aplicação web é hospedada. Isso significa que ela será colocada dentro de um servidor, que gerenciará os recursos necessários para disponibilizar o serviço da aplicação.

Vamos entender isso melhor. Temos um HTML que é o conteúdo que queremos disponibilizar para que os clientes vejam. Se clicarmos no Visual Studio, no canto superior direito, em "Show Preview", que vem da extensão *Live Preview*, comumente utilizada para testar aplicações web no Visual Studio Code, ele apresentará um navegador mais simples. Poderíamos pegar esse endereço e colocá-lo no Chrome, sem problemas. Aqui, ele indica que a aplicação está hospedada em um endereço específico e em uma porta.

## **Detalhando o uso de portas e protocolos**

O protocolo utilizado é o HTTP, e ele mostra o endereço local, localhost 127.0.0.1, nosso IP. Utiliza a porta 3000, e é importante saber que há uma diferença entre uma porta local e a porta externa, que é a porta 80 do HTTP. Não devemos confundir isso. Quando falamos de porta local, não há problema em não ser a porta 80\. Na internet, devemos usar a porta 80 para HTTP ou a porta 443 para HTTPS.

O navegador está sendo o cliente que acessa o servidor hospedado neste endereço, que devolverá um conteúdo. A resposta desse conteúdo, além da mensagem definida pelo protocolo HTTP, inclui o HTML e o conteúdo processado por este HTML renderizado pelo navegador.

## **Concluindo sobre o modelo cliente-servidor**

Devemos entender que, nesse modelo, não há instalação de aplicações. Não há o modelo de baixar um aplicativo. Temos um modelo de cliente e servidor, onde o cliente solicita um serviço através da URL, e um serviço hospedado devolve o recurso solicitado.

Para que essa comunicação entre cliente e servidor funcione com todos os tipos de aplicações, precisamos de um meio comum que permita solicitar um recurso e recebê-lo no formato correto para processamento nos navegadores. Isso é possível graças ao protocolo HTTP, que veremos com mais detalhes agora.

