## Versões do HTTP

## **Discutindo a evolução da web e do HTTP**

Quando a web foi idealizada, ela não foi concebida para suportar o que vemos hoje. Atualmente, temos uma vasta gama de serviços rodando na internet, como *streamings*, jogos online e muitos processos que operam de forma assíncrona. Esses serviços escalam para milhões ou bilhões de usuários, e todas as alterações necessárias para suportar esse tipo de aplicação precisaram ser implementadas na internet e nos protocolos HTTP, permitindo que a internet crescesse até a magnitude que possui atualmente.

Assim como várias aplicações passam por atualizações, o HTTP também passou por certas atualizações, assim como a infraestrutura da web inteira. Podemos pensar na evolução das redes móveis, como o 3G, 4G e agora o 5G, com discussões contínuas sobre formas de tornar a internet mais rápida. Tanto a infraestrutura física quanto a lógica da internet passam por mudanças.

## **Explorando as versões do HTTP**

Podemos dividir as principais versões do HTTP em três categorias: HTTP, que engloba as versões 1 e 2, usadas por padrão hoje em dia; HTTPS, que é o HTTP com uma camada de segurança através de criptografia e certificados digitais; e HTTP 3, que está sendo introduzido em vários servidores para permitir o uso de tecnologias mais modernas, visando um ganho de performance em aplicações críticas ao desenvolvimento de software atual.

Vamos entender as diferenças principais entre essas três versões de HTTP. A questão da segurança é a mais importante. O HTTP, por padrão, não é seguro, pois possui vulnerabilidades que tornam os dados públicos, permitindo que qualquer pessoa os rastreie. Alterações foram feitas no protocolo para garantir segurança no envio de dados. Por muito tempo, não era possível realizar pagamentos de maneira segura na web até a introdução do HTTPS, que trouxe certificados digitais e criptografia. O HTTP 3 já é seguro por padrão, com mecanismos nativos para impedir vulnerabilidades, ao contrário do HTTPS, que foi uma adaptação do HTTP.

## **Comparando protocolos de transporte e multiplexação**

Quanto ao protocolo de transporte, o HTTP e o HTTPS ainda utilizam o protocolo TCP, enquanto o HTTP 3 opera através de uma versão diferente, não utilizando o TCP. Isso permite uma transferência de informações mais rápida, embora ainda exista a questão dos problemas de pacotes entre TCP e UDP.

A multiplexação, que permite várias requisições simultâneas em uma mesma conexão, é suportada pelo HTTP e HTTPS, mas com certos limites. O HTTP 3, pensado para acessos simultâneos, é bem suportado pelo UDP, permitindo múltiplos acessos ao mesmo tempo.

## **Avaliando o desempenho e a adoção do HTTP/3**

Em termos de desempenho, o HTTP e o HTTPS possuem limitações, especialmente em acessos extensos de dados. O HTTP 3, por outro lado, foi projetado para ter uma alta margem de transferência de dados, aprimorando o desempenho. É interessante notar que, em versões antigas do HTTP, não se transferia mais do que quilobytes de informação, o que era o máximo necessário na época.

Atualmente, observamos que uma série ou um vídeo no YouTube pode ter mais de 30 gigabytes, e um jogo inteiro para download pode ultrapassar 100 gigabytes. Os protocolos antigos do HTTP não são mais adequados para esse volume de dados e transferência de informações. O HTTP/3 surge para resolver esse tipo de problema. A adoção do HTTP/3 é um ponto importante. Quando utilizamos URLs ou mesmo requisições no Postman, ainda se usa muito o HTTP, que é o padrão da web 1.1. Ele já realiza todas as requisições necessárias. As versões do HTTPS e do HTTP são amplamente adotadas na internet e continuarão a ser até que não suportem mais o volume de dados ou o modelo de protocolo atual.

## **Testando diferentes versões do HTTP com curl**

O HTTP/3 está em processo de adoção. Algumas empresas já utilizam o HTTP/3 por padrão, mas nem todos os servidores de hospedagem trabalham com ele por padrão. Em algum momento, ele será amplamente adotado. Vamos agora explorar como testar essas diferentes versões do HTTP utilizando, por exemplo, o curl.

Para começar, podemos testar como fazer uma requisição na web de um site utilizando o HTTP/3. No terminal, utilizamos o seguinte comando:

Copiar

curl \--http3 \-I http://www.cloudflare.com

Ao digitar esse comando, a requisição é feita no HTTP/3, mas a resposta é devolvida no HTTP/1.1. Isso ocorre porque, ao usar a versão HTTP, é normal que a resposta seja redirecionada para o HTTPS, como indicado pelo status code 301 (movido permanentemente).

## **Comparando tempos de resposta entre versões do HTTP**

Com essa versão do curl, podemos testar tanto o HTTP/3 quanto outras versões do HTTP. Por exemplo, para testar o HTTP/2, podemos usar:

Copiar

curl \--http2 \-I http://www.cloudflare.com

Ao repetir o comando, podemos substituir o HTTP/3 pelo HTTP/2, obtendo a mesma resposta e status code. É importante notar que o protocolo utilizado em cada consulta é diferente, mesmo que a resposta mantenha o HTTP/1.1.

Podemos verificar o tempo de cada requisição para diferentes versões do HTTP. Por exemplo, ao executar uma consulta no site usando HTTP/1.1, utilizamos o seguinte comando:

Copiar

curl \--http1.1 \-w "Time: %{time\_total}s\\n" \-o /dev/null \-s https://api.scryfall.com/cards/random

O tempo foi de 0,61 segundos. Ao trocar para HTTP/2, o comando é:

Copiar

curl \--http2 \-w "Time: %{time\_total}s\\n" \-o /dev/null \-s https://api.scryfall.com/cards/random

E o tempo foi de 0,78 segundos. Com o HTTP/3, observamos algumas diferenças ao usar:

Copiar

curl \--http3 \-w "Time: %{time\_total}s\\n" \-o /dev/null \-s https://api.scryfall.com/cards/random

O HTTP/1.1 é o mais rápido porque não realiza verificações de segurança antes da requisição, não havendo processo de criptografia. Já o HTTP/2, com 0,78 segundos, envolve mais segurança, especialmente com o HTTPS, realizando verificações que o HTTP/1.1 não faz. O HTTP/3, por ser seguro por padrão, é mais demorado. Embora o HTTP/3 seja mais rápido em desempenho, ele ainda não é amplamente utilizado. As requisições padrão são feitas no HTTP/2, e a necessidade de trocar a versão do protocolo torna a requisição mais demorada. A vantagem do HTTP/3 é que ele é seguro por definição, diferentemente do HTTP/2 e do HTTP/1.1.

