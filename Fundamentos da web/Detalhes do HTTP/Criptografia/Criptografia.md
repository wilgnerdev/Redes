## Criptografia

## **Discutindo a importância da segurança na web**

Uma questão que podemos ter percebido nas explicações sobre as versões do HTTP é que a segurança se tornou primordial para o funcionamento da web como a conhecemos atualmente. Hoje em dia, realizamos muitas operações consideradas vulneráveis no ambiente da internet. Pagamos produtos por e-commerce, fazemos transferências em aplicações bancárias e enviamos informações pessoais que não queremos que sejam vazadas. Todos esses tipos de informações precisam de uma camada de segurança para impedir que sejam roubadas ou adulteradas.

Quando a web foi inicialmente concebida, especialmente na versão HTTP, ela era vulnerável a diversos tipos de ataques. Vamos discutir alguns dos ataques mais comuns que ocorriam na web e mostrar casos de como esses problemas aconteciam.

## **Explorando tipos comuns de ataques na web**

Primeiramente, temos a interceptação. Quando tentamos acessar um recurso, clicamos em um link e, em vez de obtermos o resultado esperado, somos redirecionados para outro link. Isso é chamado de interceptação. O recurso solicitado é capturado por um interceptador, que nos envia uma resposta com base nessa interceptação. Esse tipo de problema é sério, pois podemos estar enviando dados sensíveis que são utilizados pelo interceptador.

Outro ataque é o *man-in-the-middle*, que é semelhante à interceptação, mas com um cenário diferente. Nesse caso, o atacante não intercepta a requisição para redirecioná-la, mas atua como um agente no meio, capturando as informações entre a requisição enviada e a resposta recebida. Embora inicialmente pareça inofensivo, o *man-in-the-middle* pode utilizar essas informações para fins maliciosos, especialmente em transações financeiras.

Temos também o *phishing*, uma prática ainda bastante utilizada na internet. Nesse caso, um site é criado para parecer exatamente como outro site legítimo, mas não é o site verdadeiro. Isso ocorre frequentemente com sites do governo, onde um site falso é utilizado para roubar informações de pessoas distraídas que acreditam estar acessando o site oficial.

Por fim, temos o problema de *injection*, comumente exemplificado pelo *SQL Injection*. Esse tipo de invasão ocorre quando informações maliciosas são enviadas para o servidor através de formulários. Não é uma questão do lado do cliente, mas sim do lado do servidor. Pessoas mal-intencionadas podem preencher campos de formulários com comandos SQL para realizar consultas ou até mesmo deletar o banco de dados inteiro do servidor.

## **Explicando o papel do TLS e HTTPS na segurança**

O que ajudou a proteger a web contra esses tipos de ataques foi, principalmente, o protocolo de criptografia que utilizamos atualmente na web, o TLS (Transport Layer Security).

O HTTPS, que é a versão segura do HTTP, funciona a partir do protocolo TLS, que é uma camada responsável pelo transporte seguro das informações. Ele possui mecanismos de segurança que garantem que, ao enviar uma informação, ela já esteja criptografada. Mesmo que alguém intercepte a comunicação, não conseguirá descriptografar ou traduzir a informação, pois não possui o mecanismo necessário para quebrar a criptografia e verificar a mensagem corretamente.

## **Compreendendo os tipos de criptografia utilizados**

O HTTPS utiliza uma combinação de dois tipos de criptografia: simétrica e assimétrica. Na prática, para nós, como usuárias e usuários, a diferença é mínima. A URL passa a incluir um "S", indicando segurança, como em https://www.alura.com.br, em vez de http://alura.com.br.

Vamos entender a diferença entre as criptografias. A criptografia simétrica é mais simples e requer que ambas as extremidades conheçam a chave para descriptografar a mensagem. Isso ocorre no navegador, sem que precisemos nos preocupar. Já a criptografia assimétrica não exige o compartilhamento de chaves entre as extremidades. Ela utiliza um sistema de chave pública e chave privada, oferecendo maior segurança na transferência de informações, mesmo que alguém conheça a chave compartilhada.

## **Destacando a importância dos certificados digitais**

Para que a web utilize esses mecanismos de criptografia, são necessários certificados digitais. Todo site possui um certificado, emitido por uma autoridade certificadora, que garante o uso do HTTPS. No site da Alura, por exemplo, podemos verificar essas informações no navegador. Ao clicar no ícone de informações do site, ao lado da barra de endereços, vemos que a conexão é segura, pois o site utiliza HTTPS. As informações transmitidas são criptografadas e permanecem privadas, graças ao certificado válido.

Cada site possui um certificado digital específico, vinculado à aplicação, que permite a criptografia das informações enviadas. Para nós, como pessoas desenvolvedoras, é importante gerar um certificado digital para aplicações que exigem segurança. Esse certificado deve estar vinculado ao domínio da aplicação, como alura.com.br. Quando geramos um certificado digital, ele é associado ao nosso domínio específico.

