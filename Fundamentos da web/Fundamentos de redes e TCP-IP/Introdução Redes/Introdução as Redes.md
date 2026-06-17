# Introdução as Redes

## **Introduzindo o compartilhamento de aplicações na web**

Agora que já passamos pelo desenvolvimento de aplicações como o Soli e entendemos como a parte web é estruturada com HTML, CSS e JavaScript, surge a dúvida: como podemos compartilhar nossa aplicação para que o mundo todo possa utilizá-la? Até o momento, conseguimos testar nossas aplicações localmente e verificar como elas funcionam dentro do nosso computador. No entanto, para disponibilizá-las mundialmente, precisamos de mecanismos que permitam o compartilhamento do programa que criamos. Um dos modelos mais comumente usados para essa distribuição é a internet e o desenvolvimento de aplicações web.

A programação é uma parte fundamental da web, especialmente no que diz respeito ao desenvolvimento do *back-end*. Para compartilhar isso globalmente, utilizamos os mecanismos da internet e a infraestrutura global da web. Vamos entender como a web funciona de maneira abrangente. A partir de agora, exploraremos os mecanismos que fazem a internet funcionar como ela é. Usaremos o exemplo comum de acessar uma URL pelo navegador. Quando digitamos um site na barra de endereços, enviamos uma solicitação ao navegador para acessar um determinado site. O navegador, que possui um cliente HTTP, envia essa solicitação pela internet, passando por diversos intermediários até chegar ao servidor da página, como o Google, por exemplo.

## **Explicando o funcionamento das solicitações na web**

Os servidores da web entendem essa solicitação, procuram o site ou página solicitada e, uma vez encontrada, devolvem uma resposta. Essa resposta é processada pelo navegador, que exibe o conteúdo, podendo ser HTML, PDF, imagem, ou JSON. Não estamos limitados apenas a HTML, CSS e JavaScript; existem diversos tipos de dados que podemos receber. Esse é o mecanismo que compõe todas as etapas de uma solicitação comum na web ao digitarmos um endereço de site na barra de endereços. Precisamos entender como esses mecanismos permitem que tenhamos uma infraestrutura capaz de realizar solicitações e obter respostas.

A internet surgiu como um projeto colaborativo entre universidades, com o objetivo de compartilhar rapidamente trabalhos realizados em laboratórios e centros de pesquisa. Isso só seria possível com uma rede global de dispositivos interconectados. Para comunicar-se entre o Brasil e universidades nos EUA, Europa ou Ásia, era necessário ter dispositivos espalhados pelo mundo, servindo como intermediários entre pontos distantes. Assim como um avião faz paradas em sua rota, a internet também possui pontos de parada para que a informação chegue de um ponto a outro.

## **Comparando LAN e WAN**

Para disponibilizar recursos, era necessário uma linguagem comum, que conseguimos através dos protocolos. A internet é um modelo global de compartilhamento de recursos, mas existem redes menores, como a LAN, que são usadas em empresas ou no cotidiano para permitir o compartilhamento de recursos de forma controlada. A LAN é um modelo local, como um interfone em um prédio, enquanto a WAN é mais abrangente, como um telefone comum que permite ligações nacionais sem a necessidade de um DDI.

A diferença entre LAN e WAN está na abrangência geográfica e no controle de acesso à informação. A LAN é restrita a um estabelecimento ou alguns andares de um prédio, enquanto a WAN pode abranger uma empresa com várias filiais, permitindo o compartilhamento de informações internas. A internet, por sua vez, é um modelo mundial de compartilhamento interconectado entre dispositivos.

## **Discutindo o acesso público e privado na internet**

Além disso, a LAN é considerada privada, sem acesso externo, enquanto a WAN pode ter dados públicos ou privados. A internet, por ser global, permite o compartilhamento de informações públicas e privadas, dependendo da configuração de acesso.

Um exemplo de uma WAN pode ser pública ou privada. Consideremos uma universidade que deseja disponibilizar algumas informações, como o calendário escolar. Essa informação pode ser pública, permitindo que qualquer pessoa acesse o calendário. No entanto, informações como notas são mais privadas e, nesse cenário, provavelmente desejamos mantê-las internas. Assim, podemos configurar a rede para que apenas aqueles conectados à rede local da universidade possam acessar certas páginas, enquanto outras informações ficam disponíveis na rede pública. A universidade pode usar a mesma infraestrutura da internet para transmitir informações públicas, enquanto as informações privadas são acessíveis apenas localmente, em alguns polos da universidade, para acessar recursos como notas ou faltas.

## **Explorando as características de LAN, WAN e internet**

A internet, por padrão, é pública e não possui restrições nativas de acesso. Todos os mecanismos que permitem um acesso mais restrito são implementados por meio de aplicações. Para acessar um recurso específico, basta conhecer o endereço e, dependendo da aplicação, um login pode ser necessário. A questão de público e privado nas redes se dá pelo acesso. LANs e WANs tendem a ser restritas, permitindo acesso apenas a quem está dentro da rede. Na LAN, todos os conectados têm acesso aos recursos, e o mesmo vale para a WAN, geralmente voltada para uma instituição.

A internet é aberta, permitindo que qualquer pessoa que conheça a URL acesse o recurso, seja uma página web ou uma foto, sem restrições de acesso. Por isso, quando estamos na internet, estamos em um ambiente aberto, sem restrições de acesso, a menos que a aplicação tenha particularidades. LANs e WANs, por serem redes mais controladas, são geralmente mais rápidas que a internet. Em uma LAN, o tráfego é local e rápido, funcionando quase instantaneamente. Já a internet pode ter várias etapas de comunicação, o que pode afetar a velocidade.

## **Analisando latência, custo e confiabilidade**

A latência, ou tempo de resposta, é uma característica importante. Na internet, a latência pode ser alta devido ao tempo de requisição até o servidor e a resposta. Quando uma página é carregada novamente, o cache do navegador torna o processo mais rápido, semelhante a uma LAN, onde a latência é baixa. A WAN pode ter variações de velocidade dependendo dos locais.

O custo é outro fator a considerar. Implementar uma LAN tem um custo baixo, enquanto a internet e a WAN têm custos mais altos devido à infraestrutura necessária. A internet funciona globalmente porque os países compartilham os custos operacionais, desde redes locais até cabos submarinos.

A confiabilidade é alta em LANs, com poucas interferências na comunicação. Em WANs, a confiabilidade pode variar devido a fatores regionais. A internet, sendo compartilhada, tem várias etapas intermediárias que podem afetar a confiabilidade, dependendo do local de acesso e dos intermediários envolvidos.

## **Concluindo a compreensão dos mecanismos da internet**

A internet é vasta e entender todos os seus mecanismos não é trivial. Existem muitas etapas e divisões que nos ajudam a compreender seu funcionamento. Já abordamos como a internet funciona de maneira abrangente, os tipos principais de redes (internet, LAN e WAN) e suas diferenças. Agora, vamos explorar como elas se comunicam por meio de protocolos que permitem o acesso a recursos em diferentes locais.

