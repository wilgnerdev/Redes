## Ferramentas e depuração

## **Explorando ferramentas para infraestrutura da web**

Existem diversas ferramentas para entender e trabalhar com a infraestrutura da web. Vamos explorar como essas ferramentas são utilizadas, começando com o DevTools e passando por clientes HTTP e ferramentas de linha de comando como o curl.

Enquanto tentávamos entender como a web funciona, percebemos que uma série de ferramentas se tornou necessária para verificar vários aspectos da infraestrutura da web. Utilizamos desde o terminal até aplicações que operam no navegador, e é importante compreender como cada uma delas funciona e como são úteis no nosso dia a dia.

## **Utilizando o DevTools para depuração**

A principal dessas ferramentas é o DevTools, que é a ferramenta de depuração que usamos para verificar qualquer coisa na internet. Ao acessar o navegador e pressionar F12, podemos inspecionar o HTML e visualizar diversos recursos que permitem a inspeção de como a web está funcionando, como uma determinada aplicação está operando e quais informações estamos recebendo. Para aplicações web, o navegador é a fonte final de verdade, mostrando como a informação está sendo transmitida para cada cliente.

Devemos entender que o DevTools não é apenas uma ferramenta, mas um conjunto de ferramentas que trabalha em conjunto com o navegador para compreender o comportamento das nossas aplicações. Ele permite verificar a rede para acessar todas as informações disponíveis, inspecionar cookies no navegador, analisar requisições para entender o protocolo HTTP e verificar as respostas recebidas. A inspeção de HTML também é uma função importante. Todas essas ferramentas estão agrupadas no DevTools.

## **Inspecionando HTML e realizando *debug***

Geralmente, usamos o DevTools principalmente para inspecionar HTML e realizar *debug* para verificar se o JavaScript está funcionando corretamente, se o CSS foi carregado adequadamente ou se as imagens estão no formato correto. Toda a visão detalhada do código do *front-end* está relacionada às versões HTML, CSS, JavaScript e qualquer outra função que possa ser inspecionada pelo navegador.

## **Compreendendo clientes HTTP e suas aplicações**

Além disso, temos os clientes HTTP, que são essenciais para entender o funcionamento da web, especialmente no que diz respeito às APIs. Ao longo dos vídeos, discutimos sobre APIs, e em breve abordaremos o que de fato é uma API. Os clientes HTTP são fundamentais para testar modelos de aplicações que trabalham com a diferença entre *back-end* e *front-end*, que são as APIs.

Existem vários clientes HTTP, sendo o mais famoso o Postman, mas também temos o Insomnia e o Thunderclient, que é uma extensão do Visual Studio Code que simula um cliente HTTP. O próprio cURL pode ser considerado um cliente HTTP, mas aqui nos referimos a clientes com interface, um ambiente mais completo para testar nossas aplicações. A vantagem de usar esse tipo de ferramenta é que podemos criar uma plataforma colaborativa. Assim, podemos estruturar requisições que uma organização pode acompanhar, controlar, testar e alterar, tudo isso graças a essas plataformas.

## **Facilitando testes colaborativos com Postman**

Imagine que temos uma empresa com várias aplicações, e essas aplicações possuem diversas rotas que precisam ser testadas continuamente. Seria complicado se cada pessoa criasse seu próprio projeto para fazer requisições web utilizando clientes HTTP, ou se cada uma configurasse seu Postman da maneira que achasse melhor. Para isso, o Postman oferece ferramentas para que todo o time, com acesso a um *workspace* (espaço de trabalho), possa configurar de forma aceitável esses testes, tornando-se o melhor cliente HTTP para as aplicações.

Os principais clientes HTTP utilizados são o Postman, Insomnia, Thunderclient, entre outros. Sempre surgem novos modelos, *open source* ou não, cada um com suas diferenças e particularidades que podem ser mais proveitosas, dependendo da aplicação que está sendo testada.

## **Utilizando curl e ferramentas de linha de comando**

No lado do terminal, em um nível mais baixo, trabalhamos com recursos do sistema operacional, como o curl, um programa utilizado em aplicações de console (CLI). Utilizamos o curl para tarefas intensivas, como rodar scripts em Bash ou Python, ou agentes de IA na linha de comando. Atualmente, temos o Codex CLI, Dantropic, Cloud Code, e outras ferramentas de IA que operam com agentes no computador. Essas ferramentas precisam executar comandos no sistema operacional, e o curl é um dos comandos mais utilizados para testar APIs ou acessos a aplicações web, verificando o comportamento esperado, se o *status code* está correto, e se a informação está sendo enviada corretamente em HTML.

## **Exemplificando o uso do curl**

Para ilustrar como o curl pode ser utilizado, vejamos um exemplo de requisição HTTP para obter um card aleatório da API Scryfall:

Copiar

curl \-X GET \\  
  'https://api.scryfall.com/cards/random' \\  
  \--header 'Accept: \*/\*' \\  
  \--header 'User-Agent: Thunder Client'

Esse comando curl faz uma requisição GET para a API Scryfall, especificando cabeçalhos para aceitar qualquer tipo de resposta e identificando o cliente como Thunder Client. Isso demonstra como podemos usar o curl para interagir com APIs diretamente do terminal.

## **Incorporando ferramentas CLI em scripts**

Essas ferramentas CLI estão sendo cada vez mais incorporadas e utilizadas por agentes de IA, e são úteis para nós ao criar scripts ou testar no terminal, pois o curl permite realizar testes de forma pura, garantindo que o cliente HTTP está sendo executado corretamente. Com o curl, podemos transferir informações de maneira simples pelas URLs, suportando diversos protocolos, não apenas o HTTP. A web funciona com outros protocolos, como SMTP para e-mails e FTP para arquivos. Embora o HTTP seja o protocolo mais comum em aplicações web, outros protocolos também precisam ser verificados, dependendo da aplicação.

## **Concluindo sobre ferramentas para desenvolvedores**

A web oferece uma série de ferramentas que facilitam nosso trabalho, cada uma com sua responsabilidade. Existem várias ferramentas que podem ser utilizadas para auxiliar nosso trabalho como pessoas desenvolvedoras. Aqui estão as principais que utilizamos no dia a dia. Cada empresa tem suas particularidades, mas geralmente seguem esse padrão ao lidar com aplicações web.