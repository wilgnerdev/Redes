# Endereços IP

# Endereços IP

## **Compreendendo o endereçamento na internet**

Agora que já compreendemos como funciona a parte de transporte e como a viagem de dados ocorre para buscar informações na internet, vamos entender mais sobre endereçamento. Se pensarmos no mundo real, como no envio de pacotes quando compramos algo online, é necessário definir um endereço para que os correios saibam como chegar ao destino. Isso também se aplica à internet, onde temos um sistema de endereçamento que permite registrar e identificar o endereço de uma máquina ou aplicação.

Já vimos um pouco sobre o endereço físico, que está vinculado a cada computador e hardware. Agora, vamos explorar o endereçamento IP, que está relacionado ao protocolo TCP e à identificação de máquinas e aplicações na parte de software. O endereçamento IP é um sistema que cria um valor específico, permitindo identificar um computador ou aplicação dentro de uma rede. Isso é válido para redes locais (LANs) ou dispositivos conectados ao Wi-Fi, como quando imprimimos uma página na impressora através do computador, mesmo sem internet.

## **Explorando o funcionamento do endereço IP**

O endereço IP funciona como um endereço residencial. Por exemplo, o número 104.26.0.70 é um IP. Para saber o IP de um computador, os sistemas têm maneiras de reconhecer esses números. Ao digitar o seguinte comando no terminal, podemos identificar o IP de um site:

Copiar

ping alura.com.br

Esse comando ping utiliza o IP para localizar o endereço, semelhante a um CEP, e verificar se o endereço está correto.

## **Entendendo o papel das portas na comunicação**

Após entender o endereço IP, vamos para a parte de portas. As portas ajudam a identificar o tipo de protocolo e a resposta esperada. Cada aplicação funciona em portas diferentes, com numerações específicas e padrões. Existem entre 0 a 65 mil portas, algumas reservadas para funções específicas. Exemplos incluem a porta HTTP (80) e HTTPS (443) para aplicações web, a porta 25 para e-mails via SMTP, e a porta DNS para endereçamento de URLs.

O endereço completo inclui o IP e a porta utilizada. No terminal, podemos usar comandos para verificar endereços. Por exemplo, para ver todas as conexões TCP estabilizadas pelo HTTPS, podemos usar:

Copiar

netstat \-an | findstr :443

E para verificar as conexões na porta HTTP, utilizamos:

Copiar

netstat \-an | findstr :80

Esses comandos mostram os IPs conectados e seus estados. Ao usar outra porta, como a 80, vemos uma gama diferente de endereços, incluindo endereços locais como 0.0.0.0 e 127.0.0.1, que são vinculados ao nosso computador.

## **Mapeando rotas com comandos de terminal**

Por fim, vamos explorar alguns comandos do Windows para entender melhor o endereçamento e como mapear o caminho até um endereço de destino. Podemos utilizar o terminal para digitar:

Copiar

tracert \-h 60 alura.com.br

Nesse cenário, o comando começa a mapear toda a infraestrutura da internet, funcionando quase como um GPS. Ele identifica cada rota ou endereço de IP necessário para chegar ao destino, que neste caso é o endereço da Alura. Assim, conseguimos visualizar toda a infraestrutura e os dispositivos envolvidos no rastreamento até o destino.

Esse procedimento também é aplicável a endereços fora do Brasil. Por exemplo, ao digitar:

Copiar

tracert \-h 60 amazon.es

Observamos que o número de IP é completamente diferente do da Alura, pois está vinculado à Espanha. O caminho necessário para chegar ao endereço da Amazon na Espanha é diferente, passando por rotas distintas. Em alguns momentos, algumas rotas podem estar obstruídas, resultando em um tempo limite esgotado. Isso indica que houve uma tentativa de alcançar o endereço, mas não foi possível devido a alguma obstrução, como problemas de rede. Nesses casos, o sistema tenta encontrar um desvio nas rotas disponíveis na internet até chegar ao site da Amazon na Espanha.

## **Explorando o conceito de sockets e a transição para IPv6**

Passando para a parte de *sockets*, é importante entender que um *socket* é a combinação entre um endereço de IP e uma porta. Existem rastreamentos que dependem de uma porta específica e outros que não exigem a especificação da porta. É importante saber que existem ambas as possibilidades, pois podemos ter o mesmo endereço de IP, mas com portas diferentes para acessar aplicações distintas.

Ao falar de endereços de IP, estamos nos referindo ao IPv4. O IPv4 é uma faixa de IPs, ou seja, um conjunto de números de IPs que podem ser registrados na internet. Atualmente, o IPv4 possui um formato de 32 bits, utilizado para criar os endereços de IP mencionados anteriormente. Isso resulta em aproximadamente 4 bilhões de endereços de IP disponíveis na internet. Embora pareça um número grande, não é suficiente para atender à demanda atual. Por isso, está em andamento uma transição para o IPv6, que possui 128 bits e comporta muito mais opções do que os 4,3 bilhões do IPv4.

Essa transição é semelhante à inclusão do número 9 nos números de telefone, que foi necessária para aumentar a quantidade de números disponíveis. O mesmo ocorre com a internet, onde o número de IPs disponíveis não é suficiente para atender à demanda atual de dispositivos. No momento, o IPv4 ainda atende às necessidades, mas, caso não seja mais suficiente, o IPv6 estará disponível como alternativa.

## **Visualizando o uso do IPv4 e a resolução de nomes**

Para visualizar o uso do IPv4, podemos digitar:

Copiar

curl \-4 google.com.br

O Google retorna um resultado a partir dessa consulta, indicando o uso do IPv4. O "-4" força o uso do IPv4, mas é o padrão do curl, então funcionaria da mesma forma sem ele. Ao trocar "-4" por "-6", o sistema informa que não consegue resolver o *host* no modelo IPv6, indicando que o site do Google ainda não suporta essa opção, mas já possui a versão IPv4:

Copiar

curl \-6 google.com.br

Caso o Google decida adotar o IPv6, provavelmente usará outro endereço de IP, permitindo o acesso tanto pelo IPv6 quanto pelo IPv4.

É interessante notar que, em nenhum momento, inserimos os endereços de IP diretamente. Utilizamos a resolução de nomes, ou DNS, que será explicada posteriormente. Ao digitar google.com.br, o sistema sabe que esse nome corresponde a um endereço de IP específico. Isso é possível graças ao mecanismo de resolução de DNS, que será abordado em detalhes mais adiante. É importante destacar que o endereço de IP e o DNS são conceitos distintos.

### **Resumo**

Nesta aula, exploramos o conceito de endereçamento na internet, que é fundamental para a comunicação de dados.

Começamos entendendo o \*\*endereço IP\*\*, que funciona como um identificador único para máquinas e aplicações em uma rede, seja ela local ou na internet. Vimos que o IP está ligado ao protocolo TCP e é essencial para a identificação de software. O comando \`ping\` foi apresentado como uma ferramenta para verificar a conectividade e o IP de um site.

Em seguida, abordamos o papel das \*\*portas\*\*, que são números específicos (de 0 a 65 mil) que ajudam a identificar o tipo de protocolo e a aplicação em uso. Exemplos incluem a porta 80 para HTTP e a 443 para HTTPS. O comando \`netstat \-an | findstr\` foi demonstrado para visualizar conexões em portas específicas.

A aula também mostrou como mapear rotas na internet usando o comando \`tracert\`. Ele permite visualizar o caminho completo que os dados percorrem, passando por diversos IPs até chegar ao destino, como o site da Alura ou da Amazon na Espanha.

Por fim, discutimos o conceito de \*\*sockets\*\*, que é a combinação de um endereço IP e uma porta. Foi apresentada a transição do \*\*IPv4\*\* (com 32 bits e cerca de 4 bilhões de endereços) para o \*\*IPv6\*\* (com 128 bits e muito mais endereços), necessária devido ao crescimento da demanda por IPs. O comando \`curl\` foi usado para demonstrar o uso do IPv4 e a tentativa de conexão via IPv6.

A aula concluiu mencionando que, embora tenhamos falado de IPs, a resolução de nomes (DNS) é o que nos permite usar nomes como \`google.com.br\` em vez de números de IP diretamente, um tópico que será aprofundado em aulas futuras.

### **Analogia**

Imagine que a internet é como um sistema de correios muito, muito grande, que entrega mensagens e informações para o mundo todo.

\*\*Endereço IP: O CEP da Internet\*\*

Assim como no mundo real, para que uma carta ou um pacote chegue ao destino certo, precisamos de um endereço. Na internet, esse endereço é o \*\*endereço IP\*\*. Ele funciona como um CEP e o número da casa de um computador ou de uma aplicação. Por exemplo, quando você digita \`alura.com.br\`, é como se você estivesse escrevendo "Rua Alura, número tal". O sistema de correios da internet (que usa o IP) sabe exatamente onde encontrar a "casa" da Alura.

O comando \`ping alura.com.br\` é como você perguntar ao carteiro: "Ei, você consegue encontrar a casa da Alura? E quanto tempo leva para ir e voltar de lá?". Ele usa o CEP (IP) para verificar se o endereço existe e se a comunicação está funcionando.

\*\*Portas: Os Apartamentos ou Setores da Casa\*\*

Agora, imagine que dentro de uma mesma casa (o endereço IP), existem vários apartamentos ou setores diferentes, cada um com uma função. Essas são as \*\*portas\*\*. Por exemplo, o apartamento 80 pode ser onde funciona a "loja de roupas" (HTTP), e o apartamento 443 é onde funciona o "banco" (HTTPS), que é mais seguro.

Quando você acessa um site, não basta saber o endereço da casa (IP), você precisa saber qual "apartamento" ou "setor" dentro dela você quer visitar. O comando \`netstat \-an | findstr :443\` é como perguntar: "Quais são todas as conexões que estão acontecendo agora no apartamento 443 (HTTPS) desta casa?".

\*\*Tracert: O GPS da Internet\*\*

O comando \`tracert\` é como um GPS superdetalhado. Se você quer ir da sua casa até a casa da Alura, o \`tracert\` mostra todo o caminho, rua por rua, cidade por cidade, até chegar lá. Ele te mostra cada "cruzamento" ou "roteador" (que também tem um IP) que a sua informação passa até chegar ao destino. Se alguma rua estiver bloqueada, o GPS tenta encontrar um desvio. É por isso que, às vezes, você vê "tempo limite esgotado", indicando que uma parte do caminho estava com problemas.

\*\*Sockets: A Combinação Perfeita\*\*

Um \*\*socket\*\* é a combinação do CEP da casa (endereço IP) com o número do apartamento (porta). É como dizer: "Quero me conectar ao apartamento 443 da casa com o IP 104.26.0.70". Essa combinação é única e permite que as aplicações se comuniquem de forma específica.

\*\*IPv4 e IPv6: A Evolução dos CEPs\*\*

No começo, tínhamos um sistema de CEPs (IPv4) que permitia cerca de 4 bilhões de endereços. Parecia muito, mas com o tempo, mais e mais casas e dispositivos foram surgindo. É como se os números de telefone estivessem acabando e precisássemos adicionar um dígito a mais (como o 9 que foi adicionado aos celulares no Brasil).

O \*\*IPv6\*\* é a nova geração de CEPs, com muito mais combinações possíveis, garantindo que teremos endereços para todos os dispositivos que se conectarem à internet no futuro.