## Armazenamento de informações

## **Discutindo a importância do armazenamento de informações em aplicações web**

Além da segurança, uma das questões mais importantes em uma aplicação web é o armazenamento de informações. Isso se aplica tanto ao lado do cliente quanto ao banco de dados, pois algumas informações precisam ser persistidas no cliente, não apenas no servidor.

Vamos considerar um exemplo simples. Ao acessar o site *MermaidJS*, que é utilizado para criar diagramas, podemos observar que ele está no modo escuro. Se alterarmos para o modo claro e atualizarmos a página, teoricamente, o site deveria retornar ao modo escuro, pois o valor padrão pode ser o do sistema da máquina ou a versão escura. No entanto, o site mantém a configuração no modo claro, indicando que ele persiste essa informação no navegador. Assim, ao mudar para o modo escuro e atualizar a página novamente, o estado permanece. Isso demonstra que o site possui um mecanismo para persistir informações no navegador, permitindo que ele saiba quais configurações foram guardadas, mesmo após uma atualização.

## **Explorando o uso de cookies para persistência de dados**

Um dos sistemas mais comuns para realizar essa persistência é através de cookies. Por exemplo, ao utilizar o *Postman* para consultar o site da Amazon, ao enviar uma requisição, recebemos o HTML da Amazon. Ao verificar os cookies, observamos que muitos são utilizados, como o i18n, que é importante para internacionalização e definição de idioma. O cookie BLR pode estar relacionado a questões monetárias, enquanto IPTBR refere-se ao idioma. Assim, ao acessar a Amazon novamente, o site já possui informações sobre o idioma e a moeda, garantindo que o conteúdo esteja adequado às preferências regionais da pessoa usuária.

Quando diversos sites perguntam se desejamos guardar cookies, eles estão se referindo a esse tipo de informação: idioma, moeda, entre outros. Em cerca de 90% dos e-commerces, essas informações são armazenadas por padrão, pois os sites desejam carregar o conteúdo de acordo com as preferências regionais da pessoa usuária.

## **Analisando o papel de sessões e cookies no contexto de login**

Um dos usos mais comuns de sessões e cookies é no contexto de login.

Fizemos o login no GitHub para demonstrar que, caso fechemos a aba e retornemos ao Postman, ao abrir o GitHub novamente, ele nos direciona para a tela de login, em vez de abrir diretamente a página do GitHub. Isso ocorre porque todos aqueles formulários de login, que às vezes apresentam o campo "Remember Me" para lembrar a pessoa usuária que está acessando o sistema, são geridos por cookies e sessões. Todo esse processo de reconhecimento do login feito na máquina envolve informações armazenadas no cliente, neste caso, no navegador.

Por exemplo, se tentarmos acessar o GitHub pelo Postman, o login do nosso usuário não seria realizado, pois são contextos diferentes. No GitHub, o login já efetuado é armazenado em uma sessão, e outras informações podem ser guardadas por cookies. Este é um exemplo claro de como algumas informações são armazenadas, incluindo preferências como o idioma utilizado no GitHub. Se houver um cookie que armazene essa informação para traduções, ele também pode ser utilizado. Essas pequenas alterações geralmente são guardadas por cookies, para que, caso a informação seja recarregada no navegador, ela já esteja configurada, evitando a necessidade de buscar essa informação no banco de dados ou mantê-la em um servidor. Isso pode ser vantajoso ou desvantajoso, dependendo de como a aplicação é configurada.

## **Examinando o impacto do armazenamento de sessões em e-commerces**

Um exemplo interessante é o e-commerce. Quando criamos um carrinho, como na Amazon, algumas aplicações armazenam o carrinho como um cookie ou como parte da sessão. Se criarmos um pedido em um computador e tentarmos finalizá-lo em outro, alguns e-commerces possuem mecanismos internos para guardar o carrinho, enquanto outros não. Assim, ao abrir um carrinho novo em outro computador, ele pode estar zerado. Este é um exemplo comum de sessão, onde a informação armazenada apenas no lado do cliente, e não no servidor, pode resultar em uma quebra na experiência do usuário.

## **Refletindo sobre a evolução da web e a importância do armazenamento e segurança**

Com isso, percebemos que a web evoluiu de um simples envio e recebimento de mensagens, como era na década de 90, para um ambiente com diversas preocupações, especialmente em armazenamento e segurança. É crucial que qualquer pessoa desenvolvedora compreenda os mecanismos da web para implementar corretamente esses sistemas e criar produtos adequados à experiência desejada para a aplicação.

