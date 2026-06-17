## Protocolo TCP/IP

## 

## **Introduzindo a importância dos protocolos na internet**

Agora que já passamos por uma visão geral sobre o funcionamento da infraestrutura da internet, é importante entendermos como a comunicação entre o navegador e outros serviços da internet ocorre. Para isso, é necessário que uma linguagem comum entre todas as partes da infraestrutura da internet seja estabelecida, garantindo que essa comunicação seja eficiente. Isso é o que chamamos de protocolos quando falamos de internet.

O protocolo talvez mais importante que utilizamos atualmente para nos comunicarmos e usarmos boa parte dos serviços da internet é o protocolo TCP/IP. Ele abrange uma série de camadas dentro da internet, permitindo que cada uma dessas camadas tenha as particularidades do envio de uma mensagem, possibilitando que consigamos acessar informações na internet. Vamos entender então como o protocolo TCP/IP funciona.

## **Explorando as camadas do protocolo TCP/IP**

Devemos compreender que o protocolo TCP/IP opera com uma série de camadas que, juntas, compõem o protocolo inteiro. A primeira camada, ou a camada mais alta do protocolo, é a camada de aplicação, que é basicamente a transmissão da informação que queremos compartilhar. Dentro do protocolo TCP/IP, na camada de aplicação, temos protocolos dentro de outros, como o protocolo HTTP.

Vamos entender melhor como funciona essa parte do HTTP, pelo menos de uma maneira mais geral, para vermos como ele está dentro da parte do TCP. O que seria a camada de aplicação quando falamos do TCP/IP? Vamos considerar o nosso navegador. Quando precisamos digitar um endereço, por exemplo, o endereço da Alura, digitamos no Google "Alura" e clicamos no link. Mesmo que o link mostre apenas "alura.com.br", se formos com a seta na barra de endereços do navegador até o início, conseguimos ver "HTTPS". Ou seja, dentro do navegador, para fazermos a transmissão de uma página web, utilizamos o HTTP na camada de aplicação.

## **Inspecionando a comunicação HTTP**

Se inspecionarmos essa página e acessarmos a parte de rede, ao atualizar a página, conseguimos ver todos os pacotes que serão transferidos. Observamos uma série de pacotes, incluindo imagens, GIFs, sons, se necessário, e links. Há uma transmissão significativa de informação. No primeiro item, que é a atualização da página, verificamos que a requisição foi feita através do HTTPS, que foi a página que acessamos para obter a informação da página HTML da Alura. Nesse exemplo, temos um exemplo claro da camada de aplicação do TCP/IP, que opera sobre o HTTP.

Embora pareça haver muita informação, não se preocupe. Vamos detalhar todas as particularidades da parte do HTTP, pois além do TCP, essa pequena parte do protocolo inteiro, que é o HTTP, é fundamental para entendermos como funcionam aplicações web. Isso será explicado posteriormente.

## **Compreendendo a camada de transporte**

Continuando com as camadas do TCP/IP, vamos para a camada de transporte, que é a camada anterior à do HTTP. Ela gerencia a transmissão de dados utilizando outros dois protocolos possíveis: o TCP e o UDP. Não devemos confundir TCP/IP com TCP. Muitas vezes, há uma confusão inicial que leva a crer que os dois são a mesma coisa, mas não são. TCP/IP é todo esse conjunto que abrange todas as camadas de comunicação da internet com as quais trabalhamos. Dentro do TCP/IP, temos a camada de transporte que pode transferir informações por TCP ou UDP. Portanto, TCP/IP e TCP são coisas diferentes.

## **Explorando ferramentas de rede no Windows**

Agora, vamos olhar para uma questão mais interna do computador e entender como o próprio sistema operacional do Windows possui ferramentas que nos permitem verificar algumas questões da rede do nosso computador. Por exemplo, se quisermos verificar usando o TCP, já que vimos a camada de aplicação, não precisamos ver o HTTP no momento. Vamos focar apenas no TCP. Para testar o TCP no Windows, podemos digitar no terminal telnet alura.com.br e pressionar "Enter". Ele se conectará com o ambiente da Alura, e o comando que inserimos desaparecerá.

Copiar

telnet alura.com.br

Ao pressionarmos "Ctrl+C" e interrompermos a conexão, o sistema indicará que a conexão foi fechada. Ele apresentará um resultado, mostrando que tentamos nos conectar a outro servidor, exibindo ainda o HTTP utilizado, incluindo a versão. Essa tentativa foi feita por meio de uma conexão TCP, que é o *telnet*. Assim, conseguimos observar o uso de duas partes da camada do TCP/IP: a camada TCP, quando solicitamos o *telnet*, e a camada de aplicação, que nos devolveu o HTTP.

## **Utilizando o comando curl para visualizar a camada de aplicação**

Vamos agora explorar como visualizar a camada de aplicação do TCP/IP diretamente pelo terminal. Ao digitar o comando curl, que é um comando do Windows, podemos utilizá-lo como um cliente HTTP para consumir informações da internet via protocolo HTTP. Utilizamos a opção "-v" para tornar a informação mais descritiva, caso contrário, ele informará apenas o geral da requisição. Ao inserir https://alura.com.br, ele apresenta toda a questão da conexão com o site da Alura e todos os parâmetros necessários para essa conexão.

Copiar

curl \-v https://alura.com.br

Posteriormente, entenderemos várias das informações apresentadas. Algumas delas já podemos verificar, como a apresentação do HTTP na versão 1.1. Veremos também outras versões do HTTP. Ele também mostra o *host* que estamos tentando acessar, que é o alura.com.br.

## **Analisando as camadas de rede e interface de rede**

Agora, vamos analisar as outras camadas que compõem o TCP/IP. Após a camada de transporte, passamos para a camada de rede. A camada de rede é responsável pelo roteamento, identificando o caminho necessário para alcançar o destino desejado. Funciona como um GPS da internet, ajudando a determinar a rota que a comunicação deve seguir.

Por último, temos a camada de interface de rede, que lida com a transmissão elétrica dos sinais necessários para a comunicação. Essa parte está mais próxima da engenharia elétrica e dos componentes que compõem a internet. A comunicação nessa camada é feita principalmente por meio de um endereço, que entenderemos melhor mais adiante, conhecido como MAC address.

No computador, ao digitar ipconfig /all, podemos visualizar todas as informações da rede, tanto local quanto da internet. Um campo específico para a camada física do TCP/IP é o endereço físico, que é um código alfanumérico vinculado ao hardware do computador. Cada dispositivo que utiliza a internet, como computadores, roteadores, celulares, modems, ou consoles de videogame, possui esse endereço físico, que é reconhecido pelo protocolo TCP/IP.

Copiar

ipconfig /all

## **Concluindo a visão geral do protocolo TCP/IP**

Com isso, já temos uma visão geral de como funciona o protocolo TCP/IP. É importante entender as características de algumas dessas camadas para manipular adequadamente as informações, fazer pedidos corretos e interpretar as respostas recebidas. A partir daqui, vamos explorar a camada de transporte e entender as diferenças entre TCP e UDP. É essencial saber diferenciar o que cada um faz, pois existem duas opções dentro da camada de transporte. Começaremos a ver essas diferenças entre TCP e UDP.

