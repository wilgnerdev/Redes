## O conceito de API

## **Explicando a estrutura das aplicações web**

Quando falamos de aplicações web, é importante nos atentarmos ao fato de que, ao acessarmos e consultarmos uma informação na internet, como em páginas da Amazon, Alura ou Netflix, recebemos apenas a informação completa do HTML. No entanto, uma aplicação web, especialmente nos modelos atuais, é geralmente dividida em dois componentes: o *front-end*, que inclui HTML, CSS, JavaScript ou uma aplicação móvel, e o *back-end*, onde ocorre todo o processamento das informações que serão armazenadas. O *back-end* é a parte do servidor, conforme discutido anteriormente no modelo cliente-servidor.

Existem aplicações integradas, geralmente desenvolvidas por pessoas desenvolvedoras *full-stack*, que trabalham em ambas as partes simultaneamente. Contudo, na maioria dos casos, as aplicações são separadas devido à complexidade. O *back-end*, por não exigir uma interface gráfica, precisa se comunicar adequadamente com uma aplicação *front-end* ou móvel. Além disso, os serviços do *back-end* podem ser públicos e consumidos por outros clientes.

## **Definindo o conceito de API**

Esse modelo de aplicação é conhecido como API (*Application Program Interface*), que é uma interface voltada para a comunicação entre diferentes aplicações. Uma API permite que um ou mais softwares se comuniquem e compartilhem dados entre si. Por exemplo, em uma aplicação móvel, muitos serviços são compartilhados entre si. A aplicação móvel não possui todo o *back-end*; muitos serviços são de terceiros e gerenciados por outras entidades.

Esses serviços de terceiros podem incluir comunicação por e-mail ou SMS, onde um servidor fornece a interface para que o dispositivo móvel se comunique com o *back-end*. O mesmo se aplica a conteúdo multimídia, como imagens e vídeos, que geralmente são armazenados em servidores na Amazon, Microsoft Azure ou Google Cloud. Para armazenamento na nuvem, quando precisamos guardar dados específicos, utilizamos bancos de dados com interfaces próprias.

## **Explorando o uso de APIs em diferentes serviços**

Na análise de dados, a ciência de dados e a geração de relatórios podem ser geridos por serviços separados. Redes sociais como Twitter, Facebook e Instagram possuem APIs específicas para comunicação e operações relacionadas. Isso também é comum em aplicações de pagamento, onde serviços de terceiros, como Mercado Pago e PagBank, fornecem meios de pagamento para as aplicações.

A geolocalização é outro exemplo, com a API do Google Maps sendo amplamente utilizada por aplicativos de GPS, como Waze e Uber, e por aplicações de logística. Notificações, como as recebidas no celular, são geridas por APIs externas. O gerenciamento de dados, segurança e autenticação também são vinculados a APIs ou serviços externos.

## **Exemplificando o uso de APIs em aplicações web**

Cada um desses serviços pode ser uma API separada, compondo a aplicação final. Por exemplo, uma aplicação web como o Scryfall, que exibe informações de cartas de Magic, é voltada para o usuário final. Ao clicar em uma coleção, a aplicação carrega informações e imagens em HTML. No entanto, outra aplicação, como o Moxfield, que cria decks, pode utilizar os serviços do Scryfall para obter informações de cartas e imagens.

O Scryfall possui uma documentação de API que permite a consulta de informações sem carregar o HTML completo. Em vez disso, ele gera um JSON que pode ser consumido por outras aplicações para carregar um HTML diferente. Essa diferença entre uma API e uma aplicação web tradicional permite que informações sejam compartilhadas entre aplicações.

## **Introduzindo os tipos de APIs**

Agora, vamos discutir os tipos de APIs.

Desde que o conceito de API foi desenvolvido, ele foi inicialmente pensado em um modelo chamado SOA, que por sua vez sucedeu outro modelo. O raciocínio de ter serviços compartilhados existe há muito tempo. No entanto, o conceito de API se popularizou principalmente com a definição das APIs REST ou APIs RESTful. Isso ocorre porque elas seguem o padrão REST, que é o principal protocolo utilizado atualmente para comunicação entre serviços web completamente distribuídos ou separados.

## **Comparando diferentes modelos de APIs**

Quando mencionamos gateways de pagamento, notificações *push* e até mesmo alguns protocolos que envolvem aplicações de IA, percebemos que eles utilizam bastante a API REST. Isso se deve ao fato de ser o modelo mais simples e comum, amplamente difundido pela comunidade. Portanto, a API REST é o modelo padrão utilizado. A própria API do SquareFolk, mencionada anteriormente, segue o padrão RESTful.

Há também um modelo mais antigo, as APIs SOAP, que operavam com um modelo mais rígido de transferência de informações. O SOAP não utilizava JSON, mas sim XML, o que resultava em uma transferência de dados mais volumosa e, consequentemente, em problemas. Um JSON requer apenas chaves, parênteses e dois pontos para estruturar chave-valor, formando uma estrutura de árvore mais condensada. Já o SOAP, com suas tags XML, podia apresentar problemas se uma tag fosse enviada incorretamente. Embora ainda utilizado por sistemas legados, o SOAP foi substituído pelo padrão API REST, que é mais eficiente e possui um padrão de comunicação definido pela OpenAPI, uma organização que promove APIs abertas.

## **Explorando novos modelos de APIs**

Outro modelo é o GraphQL, uma ferramenta criada pelo Facebook que permite um modelo de API mais flexível, baseado em consultas personalizadas para cada usuário. Embora comparado a uma consulta SQL na web, o GraphQL permite que se faça uma consulta dentro da requisição, solicitando dados de forma dinâmica conforme as definições feitas. Isso proporciona uma flexibilidade que outras APIs não possuem, pois as APIs REST são voltadas a contratos, exigindo um corpo de requisição específico para obter uma resposta específica. O GraphQL, por outro lado, permite especificar exatamente os campos desejados na resposta.

Temos também o modelo de APIs WebSocket, voltado para aplicações em tempo real, como jogos online, gráficos e bolsas de valores. Diferente dos outros modelos, onde é necessário enviar requisições constantemente, o WebSocket estabelece um canal de comunicação contínuo entre as extremidades, permitindo uma transferência constante de informações.

O gRPC é um modelo mais recente de comunicação adotado por APIs, que, ao contrário dos outros modelos, não utiliza JSON, mas sim informações binárias convertidas e enviadas. Isso torna o gRPC mais rápido na entrega de informações em comparação com a API REST, que ainda utiliza JSON. Devido à sua velocidade, o gRPC é preferido em aplicações que exigem alta performance.

## **Discutindo APIs abertas e seus usos**

Existem APIs abertas, como a do SquareFolk, que qualquer pessoa pode acessar, desde que siga as regras estipuladas na documentação. APIs abertas não significam necessariamente uso gratuito, mas sim que não é necessário se cadastrar como uma entidade para acessá-las. Existem várias APIs abertas no mundo, oferecendo funcionalidades em diversas categorias, como a NASA API, que fornece dados de pesquisas, ou a Open Weather Map, que disponibiliza informações de previsão do tempo.

Um projeto interessante no GitHub é o "Public APIs", que apresenta uma série de APIs públicas e abertas para teste e uso. Ele abrange diversas categorias, como APIs de animais, animes, livros, calendário, e-mail, finanças, comidas, jogos, geolocalização, governo, saúde, trabalhos, música e notícias. Essas APIs abertas podem estar disponíveis ou não, mas oferecem várias opções e até mesmo APIs de reserva para garantir o funcionamento contínuo das aplicações. Quando falamos de uma aplicação web que consome APIs, se não for um serviço pago, geralmente há APIs de backup para garantir a continuidade do serviço.