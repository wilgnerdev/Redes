## Requisições e respostas

## **Explicando a importância do protocolo HTTP**

A necessidade de utilizar o protocolo HTTP é fundamental para que possamos criar aplicações funcionais na internet. Quando falamos sobre a utilização do protocolo HTTP, precisamos entender que é necessário sempre comunicar uma requisição e obter uma resposta. Para isso, as requisições possuem um formato que precisa ser enviado adequadamente. Vamos entender um exemplo de requisição HTTP. Já vimos anteriormente como trabalhar com uma requisição utilizando uma URL, mas aqui temos outro exemplo de como funciona estruturalmente uma requisição HTTP.

Basicamente, a requisição HTTP funciona através de um cliente HTTP que envia a mensagem. Temos aqui o método GET e a URI que está sendo enviada para aquele recurso. É importante saber a diferença entre URI e URL. Aqui temos o nosso host, que é a composição do host com o endereço que vem em seguida. Essa é a URL de fato, mas temos a composição do host e da URI, além do protocolo utilizado, que é o HTTP 1.1, e o *user agent*, que é basicamente o que estamos utilizando para fazer a requisição. Anteriormente, estávamos usando a URL e ela mostrou que era um agente diferente. Aqui, utilizamos uma extensão do Visual Studio chamada Thunder Client, que permite simular um cliente HTTP dentro da nossa aplicação.

## **Demonstrando requisições HTTP com Thunder Client**

Para ilustrar, veja o exemplo de uma requisição GET utilizando o Thunder Client:

Copiar

GET /sets/2ec77b94-6d47-4891-a480-5d0b4e5c9372 HTTP/1.1

Host: api.scryfall.com

User-Agent: Thunder Client (https://www.thunderclient.com)

Vamos entender como funciona essa parte da requisição HTTP dentro do navegador e quais outras ferramentas podemos utilizar para entender melhor o funcionamento de uma requisição. No navegador, podemos inspecionar o site da Alura. Ao acessar a rede, podemos limpar e atualizar a requisição, carregando todos os pacotes necessários para a página. Ao clicar em Alura, podemos ver no DevTools algumas informações, principalmente os cabeçalhos de requisição, que permitem enviar a mensagem e obter uma resposta. Conseguimos ver informações como a URL requisitada, o método e o código de status. Isso será melhor explicado quando falarmos sobre respostas HTTP, mas já conseguimos obter algumas informações da requisição.

## **Explorando ferramentas para requisições HTTP**

Se quisermos entender melhor, o DevTools apresenta uma visão ampla de tudo que foi requisitado e respondido, mas não fica tão claro como enviar de fato aquele cabeçalho HTTP com as informações necessárias. Vamos usar uma ferramenta diferente que ajuda a ver o mínimo necessário para fazer uma requisição HTTP: o Postman. O Postman é uma das ferramentas mais utilizadas como cliente HTTP, permitindo testar sites, APIs ou outros tipos de aplicações que trabalham com a internet, testando nos mínimos detalhes o comportamento do protocolo HTTP.

No Postman, ao criar uma nova requisição, podemos escrever a URL desejada, como http://www.alura.com.br, e clicar em enviar. Ele fará a requisição e devolverá o HTML daquela requisição. No botão de *preview*, podemos ver o HTML, mas ele não é renderizado completamente, pois no momento da requisição, o *preview* não carrega todos os pacotes de CSS, JavaScript e imagens, apenas o HTML puro. Os outros pacotes vêm em sequência. Por isso, comentamos que a transferência de dados precisa ser ordenada, recebendo primeiro o HTML e depois as outras informações.

## **Utilizando o Postman para requisições HTTP**

No canto superior direito, há um símbolo de código, semelhante a uma tag HTML. Ao clicar nele, podemos ver como executar essa requisição através de outros mecanismos. O principal mostrado é o *curl*, que usamos no terminal. Podemos copiar esse comando e executá-lo no terminal para obter o mesmo resultado. No entanto, o *curl* não é o ponto mais importante. Acima da linha que apresenta o *curl*, há um *drop-down* com várias linguagens de programação, como C\#, Java, JavaScript, Kotlin, Node.js, entre outras. O mais importante no momento é o HTTP, pois ao clicar nele, conseguimos ver a requisição HTTP mais pura possível. Com isso, vemos exatamente o exemplo de mensagem solicitado anteriormente:

Copiar

GET / HTTP/1.1

Host: www.alura.com.br

Já entendemos como funciona o mínimo para fazer uma requisição HTTP. A partir dessa requisição, podemos obter os recursos necessários a partir de um endereço específico. Precisamos entender algumas coisas sobre o cabeçalho da requisição HTTP. Primeiro, indicamos o método. Existem outros tipos de métodos HTTP, como GET, POST, PUT e DELETE. Mais adiante, explicaremos o que cada um faz. Fazemos uma solicitação através de uma URI, que é o detalhamento do recurso da URL completa que estamos requisitando. Estávamos pegando algumas páginas que já são o índice de uma página HTML, como www.alura.com.br, que nos leva à página principal. Claro que existem outras páginas que compõem o site inteiro da Alura, e essas outras páginas fazem parte da URI, entrando em subpáginas dentro da aplicação da Alura.

## **Diferenciando URL e URI**

Vou mostrar um exemplo sobre a diferença entre URL e URI. No navegador, verificamos o site inicial da Alura, ou seja, o índice do HTML da Alura. Ao clicar em qualquer link, como "programação", aparece outra seção da aplicação da Alura, com o caminho /escola/programacao. Essa é uma URI que vem da URL www.alura.com.br. No DevTools, ao verificar a requisição dessa página, vemos que o *request URL* foi www.alura.com.br/escola/programacao. Vou copiar essa URI e colá-la no Postman, substituindo a URL anterior. Ao enviar e ver como isso funciona no HTTP, o GET busca agora a URI /escola/programacao com o host www.alura.com.br. Para o HTTP, há uma distinção entre o que é o host e o que é a URI, que vem após o .com.br.

Copiar

GET /escola-programacao HTTP/1.1

Host: www.alura.com.br

## **Explorando requisições POST**

Além das requisições onde solicitamos informações, existem requisições onde enviamos informações. Aqui, vemos outro tipo de requisição HTTP, com duas propriedades para trabalhar com o protocolo HTTP. Temos outro método, o POST, com os mesmos parâmetros.

Copiar

POST /api/v1/usuarios HTTP/1.1

**Host: exemplo.com**

**Content-Type: application/json**

**Authorization: Bearer token-exemplo**

**Content-Length: 49**

{

    "nome": "João",

    "idade": 30,

    "cidade": "São Paulo"

}

Temos a URI, o host e a versão. Além disso, há informações adicionais que fazem parte do cabeçalho. Não é necessário saber todas elas de imediato, pois com o tempo entenderemos o significado de cada uma dentro dos *headers* HTTP. O mais importante é compreender que agora estamos enviando um corpo na requisição. Este corpo é o que permite atualizar ou enviar informações ao servidor, solicitando alguma alteração.

## **Exemplificando o uso do método POST**

Vamos exemplificar como o método POST funciona. No site da Amazon, ao selecionar um produto qualquer, podemos inspecionar o *DevTools* para observar o comportamento de um POST. Ao adicionar um produto ao carrinho, enviamos um POST na requisição. Isso ocorre porque estamos solicitando ao servidor da Amazon que registre a adição do produto ao carrinho. Nesse momento, deixamos de ser apenas consumidores de informação e também enviamos dados para o servidor processar. O corpo da requisição, que utilizamos, está no *payload*, onde podemos ver todas as informações enviadas ao servidor da Amazon, compondo a requisição junto com o cabeçalho.

É importante destacar que o corpo da mensagem é opcional. Dependendo da solicitação HTTP, não é necessário enviar o corpo da mensagem. Ele é geralmente reservado para métodos que atualizam ou enviam algo ao servidor, como POST ou PUT, que veremos posteriormente.

## **Analisando respostas de requisições HTTP**

Podemos verificar como funciona a resposta de uma requisição HTTP. Basicamente, ela indica algumas informações, como o status, que retorna o número 200 quando a requisição é bem-sucedida, o tipo de conteúdo devolvido, que pode ser um JSON, e a formatação desse JSON, que utiliza *UTF-8*. É importante entender o que é o *content-type* e o conteúdo devolvido em uma resposta.

Copiar

HTTP 200 success

Content-Type: application/json; charset=utf-8

{

    "object": "set",

    "id": "2ec77b94-6d47-4891-a480-5d0b4e5c9372",

    "code": "uma",

    "mtgo\_code": "uma",

    "arena\_code": "uma",

    "tcgplayer\_id": 2360,

    "name": "Ultimate Masters",

    "uri": "https://api.scryfall.com/sets/2ec77b94-6d47-4891-a480-5d0b4e5c9372",

    "scryfall\_uri": "https://scryfall.com/sets/uma",

    "search\_uri": "https://api.scryfall.com/cards/search?include\_extras=true\&include\_variations=true\&order=set\&q=e%3Auma\&unique=prints",

    "released\_at": "2018-12-07",

    "set\_type": "masters",

    "card\_count": 254,

    "printed\_size": 254,

    "digital": false,

    "nonfoil\_only": false,

    "foil\_only": false,

    "icon\_svg\_uri": "https://svgs.scryfall.io/sets/uma.svg?1754280000"

}

No Postman, ao fazer uma solicitação no site da Alura, podemos ver cabeçalhos de requisição e resposta. A resposta geralmente inclui a data, o tipo de conteúdo, que pode ser um HTML, e o *charset*, que é a formatação do HTML. Assim, várias informações compõem a resposta de um cabeçalho HTTP. O mais importante é que no final temos o corpo da requisição, que pode ser HTML ou outro tipo de informação.

## **Explorando diferentes tipos de conteúdo em respostas HTTP**

No navegador, ao buscar imagens do Google e abrir uma imagem em uma nova guia, podemos inspecionar os cabeçalhos e ver que o *content-type* é diferente do solicitado no Postman. No caso, é uma imagem JPEG, diferente do texto HTML devolvido anteriormente. Diversos tipos de dados podem ser trafegados, como imagem, áudio, vídeo ou texto.

Copiar

Content-Type: image/jpeg

Vamos mostrar um tipo diferente de resposta que o HTTP pode fornecer. Além de imagem e HTML, existem outros formatos importantes. No site Scryfall, que apresenta cartas de Magic, ao clicar em uma coleção, podemos ver as cartas e suas descrições. Ao clicar no link CopyPaste.json, vemos uma formatação de dados textual em JSON, muito utilizada por JavaScript e APIs. Ao inspecionar a página, podemos verificar os *headers* das requisições, onde o *content-type* é application-json, um tipo específico de formatação de dados.

Copiar

application/json; charset=utf-8

## **Concluindo sobre o protocolo HTTP e suas funcionalidades**

Todos esses formatos têm um propósito específico. Se a aplicação não indicar na resposta que se trata de um JSON, HTML, texto ou imagem, o navegador pode não renderizar corretamente o dado. No Scryfall, ao devolver um JSON, podemos formatá-lo no navegador, pois ele segue uma estrutura comum. Se não indicarmos que é um JSON, mesmo recebendo a informação, não poderíamos formatá-la. Isso vale para áudio, imagem e vídeo. O navegador precisa saber o padrão devolvido na resposta do serviço consumido.

Entendemos como funciona o protocolo HTTP a partir da requisição e da resposta. Precisamos compreender melhor os tipos de requisição que podemos fazer. Mencionamos anteriormente os métodos GET, POST, PUT, DELETE, PATCH, OPTIONS, entre outros. Esses métodos HTTP são essenciais para o funcionamento correto da aplicação. Na próxima aula, exploraremos como esses métodos funcionam e como interagem com o HTTP.

### Resumo

Nesta aula, você aprendeu sobre a importância do protocolo HTTP para a criação de aplicações web funcionais. Vimos que toda comunicação HTTP envolve uma requisição e uma resposta.

\*\*Requisições HTTP:\*\*  
\*   \*\*Estrutura:\*\* Uma requisição HTTP é enviada por um cliente e inclui o método (como GET ou POST), a URI (o recurso específico que está sendo solicitado), o host (o endereço do servidor), a versão do protocolo HTTP e, opcionalmente, um \*user agent\* e outros cabeçalhos.  
\*   \*\*Ferramentas:\*\* Foram apresentadas ferramentas como o Thunder Client (extensão do Visual Studio Code), o DevTools do navegador e o Postman para simular e inspecionar requisições HTTP.  
\*   \*\*Métodos:\*\*  
    \*   \*\*GET:\*\* Usado para solicitar informações de um servidor. Exemplos incluem acessar uma página web ou buscar dados de uma API.  
    \*   \*\*POST:\*\* Usado para enviar informações ao servidor, como preencher um formulário ou adicionar um item ao carrinho de compras. Requisições POST geralmente incluem um corpo (payload) com os dados a serem enviados.  
\*   \*\*URI vs. URL:\*\* Foi destacada a diferença entre URL (o endereço completo) e URI (o caminho específico do recurso dentro da URL).

\*\*Respostas HTTP:\*\*  
\*   \*\*Estrutura:\*\* Uma resposta HTTP inclui um código de status (indicando o sucesso ou falha da requisição, como 200 para sucesso), o tipo de conteúdo devolvido (\*Content-Type\*, como \`application/json\`, \`text/html\` ou \`image/jpeg\`) e o corpo da resposta (os dados solicitados, como HTML, JSON, imagem, etc.).  
\*   \*\*Importância do \*Content-Type\*:\*\* O \*Content-Type\* é crucial para que o navegador ou cliente saiba como interpretar e renderizar corretamente os dados recebidos.

Em resumo, a aula detalhou como as requisições e respostas HTTP são estruturadas e como diferentes ferramentas podem ser usadas para entender e interagir com esse protocolo fundamental da web.