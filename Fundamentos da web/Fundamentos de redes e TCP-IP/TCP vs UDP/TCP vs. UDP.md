## TCP vs. UDP

## **Introduzindo a camada de transporte do TCP/IP**

Agora que já vimos o protocolo TCP/IP, é importante que entendamos melhor a camada de transporte do TCP/IP, que envolve a diferença entre TCP e UDP. A principal diferença entre TCP e UDP é que, apesar de ambos fazerem parte da camada de transporte do TCP/IP, eles possuem características distintas.

## **Explicando o funcionamento do TCP**

Primeiramente, o TCP/IP estabelece uma conexão e garante que a entrega dos pacotes seja ordenada. Isso significa que, para receber uma informação via TCP, é necessário que ela seja enviada na sequência correta. Caso contrário, pode haver perda de pacotes e corrupção da informação recebida. O TCP detecta e corrige erros caso algum problema ocorra durante a transmissão. Isso assegura que, ao receber uma informação através do TCP, ela tenha passado por correções de erros, caso haja interferências na comunicação e transferência.

Para que tipo de aplicação utilizamos o TCP? Principalmente em aplicações web tradicionais. Quando falamos de páginas web, imagens, textos e arquivos, geralmente esses pacotes são transferidos via TCP. Isso ocorre porque, se houver um problema, como um JavaScript não carregado adequadamente, a página pode quebrar. Precisamos garantir que todos os componentes de uma página web sejam transferidos de maneira integral, correta e ordenada. Às vezes, é necessário que o HTML seja enviado primeiro para que o JavaScript possa dinamizar a página. A ordem correta dos pacotes é crucial para evitar que a página web fique quebrada, como quando um CSS é recebido antes do HTML e não consegue aplicar os estilos, ou quando o JavaScript tenta renderizar algo em uma página que ainda não foi carregada.

## **Descrevendo o funcionamento do UDP**

Por outro lado, o UDP funciona de maneira diferente. No caso do UDP, não há estabelecimento de conexão, o que significa que a entrega não é ordenada. Podemos receber pacotes de maneira totalmente assíncrona, sem controle sobre a ordem de recebimento. Isso impede a detecção e correção de erros durante as transferências. Se houver perda de pacotes, não é possível corrigi-los durante a transferência.

A comunicação via protocolo UDP é frequentemente utilizada em jogos online ou em *streamings* de informação. Por exemplo, ao assistirmos vídeos em plataformas como Netflix ou YouTube, ocorre uma transferência de dados em vídeo. Se perdermos um dos pacotes durante essa transferência, isso não representa um problema significativo. É comum que, ocasionalmente, uma legenda não apareça porque o pacote correspondente não foi recebido, ou que uma pequena parte da imagem apresente falhas momentâneas, mas depois retorne ao normal.

## **Comparando o impacto da perda de pacotes em TCP e UDP**

Também observamos variações na qualidade do vídeo devido a picos de tráfego. Por exemplo, ao assistir um vídeo, a qualidade pode subitamente diminuir. Em situações em que o vídeo começa a tremer, mas não cai completamente, isso ocorre porque o UDP permite a continuidade da transmissão, mesmo com a perda de alguns pacotes. Esses pacotes perdidos são considerados indiferentes para mantermos a comunicação adequada da informação. Assim, ao assistirmos um filme, mesmo que haja pequenos problemas na imagem ou no som, continuamos assistindo com os pacotes restantes sendo entregues corretamente.

No caso do TCP, a situação é diferente. Com o TCP, é necessário que a informação seja entregue corretamente. Em jogos online, o princípio é semelhante. Em jogos que exigem transferência rápida de informações, como Fortnite, é comum que jogadores com conexão de internet instável experimentem travamentos no cenário. Isso ocorre porque a transferência de dados via UDP não está sendo eficiente, mas o jogador ainda consegue participar do jogo. Se a conexão se deteriorar a ponto de impedir a continuidade do jogo, o jogador é desconectado da sala e perde a fase. Isso acontece porque o UDP aceita a transferência de dados até um limite de perda de pacotes, além do qual a conexão é interrompida.

