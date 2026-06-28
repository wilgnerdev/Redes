# Sistema de Nomes de Domínio (DNS)

## Sistema de Nomes de Domínio (DNS)

## **Explicando a resolução de DNS**

Agora que passamos pela parte de endereçamento e entendemos como o computador utiliza o endereço de IP para chegar a um destino, precisamos compreender que, para o computador, o funcionamento se dá através do endereço de IP. No entanto, para nós, seria muito difícil memorizar todos os IPs de todos os computadores e saber a ordem numérica do que estamos buscando. Para resolver esse problema, existe a resolução de DNS, ou a resolução de nomes por DNS.

O que é essa resolução de DNS? A internet desenvolveu um sistema que possui um servidor responsável por armazenar os endereços de IP e vinculá-los aos nomes de domínio. Esses nomes de domínio são, na verdade, o DNS que temos para o nome de nossa aplicação. Na internet, existem servidores que cuidam de associar o nome de uma aplicação, como Google, Amazon, Spotify ou Alura, a um IP. É esse sistema que nos informa a diferença entre o nome de uma URL que digitamos e o IP correspondente. É semelhante à diferença entre o CEP e o endereço completo. Não sabemos o CEP de todos, mas conhecemos o endereço completo de uma pessoa, incluindo o nome da rua, número e complemento. O DNS seria como esse endereço completo, enquanto o endereço IP seria o CEP vinculado àquela pessoa.

## **Comparando DNS e endereços postais**

Para nós, é mais comum procurar alguém pelo endereço completo. Já para sistemas como correios ou aplicações como o Google Maps, é mais intuitivo procurar pelo CEP, que é um número mais fácil de identificar e geralmente único. Podemos ter o mesmo nome de rua em diferentes cidades, mas o CEP é único em todos os lugares. Assim, o CEP é o endereço único, e o endereço completo é o que entendemos por DNS.

Por fim, temos os servidores DNS, que são aplicações na internet responsáveis por manter uma lista ou tabela que verifica se um endereço de IP está vinculado a um nome específico. Toda URL que digitamos no navegador para acessar um site possui um número de IP vinculado a ela. Durante o tráfego, como no *TraceSearch*, algum servidor de DNS é encontrado e direciona para o próximo servidor com o DNS resolvido.

## **Funcionamento do processo de resolução de DNS**

Vamos entender de maneira geral como esse processo funciona. No navegador, digitamos o nome do domínio que queremos acessar, como Google, Amazon, Spotify ou Netflix. O navegador envia uma consulta de DNS porque não sabe qual é o IP vinculado ao DNS, a menos que essa informação já esteja registrada. Se acessamos um site recentemente e pedimos para atualizar, o navegador pode guardar essa informação e saber qual IP precisa diretamente. Mas, se for a primeira vez que acessamos um site, ele precisará consultar diretamente.

Dentro do servidor, verifica-se se a informação está disponível. Caso não haja correspondência entre a URL digitada e um IP específico, o servidor perguntará a outros servidores de DNS até encontrar um que possua essa informação. Uma vez encontrado o endereço, o IP é retornado ao navegador. Com o IP, o navegador consulta o local correto e, a partir do IP correto, o recurso é respondido, permitindo que saibamos exatamente onde nos conectar.

## **Exemplificando a resolução de DNS com URLs**

Vamos entender como isso funciona no navegador ao encontrar os IPs. Se digitarmos um site, por exemplo, alura.com.br, temos a resolução do nome do DNS alura.com.br através dessa URL. A URL é o que digitamos no navegador e compõe o endereço que queremos acessar. Toda vez que acessamos a barra de endereços do navegador, estamos lidando com uma URL.

Basicamente, o domínio que estamos acessando na URL completa é alura.com.br. Este é o DNS, alura.com.br, e esse endereço completo é a URL. Podemos observar algumas características, como o .br, que indica que o site é brasileiro ou, pelo menos, que a parte de endereçamento é brasileira. Se quisermos acessar outro site, podemos usar, por exemplo, amazon.es, que nos leva à Amazon na versão da Espanha, diferente da versão no Brasil. Para acessar a Amazon do Brasil, utilizamos amazon.com.br. Assim, podemos ver a diferença entre a Amazon Espanha e a Amazon Brasil, que possuem IPs diferentes. A resolução do DNS apresentará informações distintas; na Amazon Espanha, provavelmente, as informações estarão em espanhol, enquanto no Brasil, estarão em português. Isso demonstra que a resolução de nomes impacta o comportamento da aplicação e do HTML, transmitindo informações específicas. O idioma é um dos aspectos mais importantes quando falamos de DNS.

## **Explorando domínios específicos e suas regras**

Outro detalhe sobre DNS é que existem DNS específicos para determinadas aplicações. Por exemplo, sites governamentais possuem o .gov. Se utilizarmos .gov, temos várias aplicações vinculadas ao governo, sendo o mais tradicional o .gov.br, específico para sites governamentais. Não podemos usar .gov em uma URL pessoal; apenas entidades governamentais têm essa permissão. O .br indica o país ao qual o site governamental pertence.

Outro tipo de site comum é o .edu, voltado para universidades. Por exemplo, ao buscar MIT edu no Google, encontramos o site do MIT com o .edu, indicando que estamos acessando o site institucional da universidade. Toda universidade ou instituição educacional pode ter o .edu, uma URL específica para instituições educacionais.

## **Concluindo o entendimento sobre DNS e infraestrutura da internet**

Uma vantagem dos DNS com domínios diferentes é que eles seguem regras específicas de cada instituição. Se alguém tentasse criar um site falso do MIT, dificilmente conseguiria a mesma resolução de DNS. A menos que estivesse em uma instituição, não poderia usar MIT.edu, precisando de outra URL para simular o site do MIT. O mesmo ocorre com sites governamentais. Os subdomínios ajudam a identificar se um site é verdadeiro ou falso, pois um site falso não pode usar .gov para se passar por governamental.

Com isso, concluímos um entendimento sobre a infraestrutura da internet. É importante compreender o caminho que nos leva de um endereço a outro, o que nos ajuda a criar aplicações que entendam esse processo. A partir daqui, temos uma base para entender não apenas aplicações de console, mas também como construir aplicações web, que possuem comportamentos e particularidades diferentes. Aplicações web funcionam por tempo indeterminado, enquanto aplicações de console podem ser encerradas ao fechar o programa. Precisamos entender essas particularidades, pois elas compõem uma série de regras que diferenciam as aplicações web. É isso que exploraremos nas próximas aulas.

### Resumo

Olá\! Compreendo que você gostaria de um resumo da aula.

Nesta aula, exploramos o Sistema de Nomes de Domínio (DNS). Entendemos que, embora os computadores utilizem endereços IP para se comunicar, para nós, humanos, é muito mais fácil memorizar nomes de domínio, como "google.com" ou "alura.com.br".

O DNS atua como um "tradutor", associando esses nomes de domínio aos seus respectivos endereços IP. Fizemos uma analogia com endereços postais: o nome de domínio seria o endereço completo (rua, número), enquanto o IP seria o CEP, um identificador único para os sistemas.

Vimos como funciona o processo de resolução de DNS: quando você digita uma URL no navegador, ele consulta servidores DNS para descobrir o IP correspondente. Se o IP não estiver no cache, o navegador pergunta a outros servidores até encontrar a informação. Uma vez que o IP é obtido, o navegador consegue se conectar ao servidor correto e carregar o conteúdo.

Também abordamos a estrutura das URLs e a importância dos domínios, como o ".br" para sites brasileiros, ".es" para espanhóis, ".gov" para governamentais e ".edu" para instituições educacionais. Esses domínios específicos ajudam na identificação e segurança, pois seguem regras que dificultam a criação de sites falsos.

Em resumo, o DNS é fundamental para a navegação na internet, tornando-a mais acessível e segura para os usuários.

# Comandos

