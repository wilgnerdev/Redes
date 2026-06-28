## Corpo da requisição

## **Analisando o uso do Postman para requisições HTTP**

Já discutimos um pouco sobre como funcionam os cabeçalhos e este momento pode ser interessante para analisarmos o Postman, a fim de entendermos onde cada elemento de uma requisição HTTP está localizado. No Postman, conseguimos visualizar exatamente onde está cada parte de uma requisição HTTP.

Para começar, vamos realizar uma requisição GET para o site da Alura. No Postman, isso é feito da seguinte forma:

Copiar

GET https://www.alura.com.br

Podemos ver o site da Alura, onde realizaremos um GET para obter algumas informações. Ao solicitar o site da Alura, receberemos uma resposta contendo o HTML da página. Se clicarmos em *Preview*, o HTML será exibido em sua forma mais pura, sem processamento de CSS ou JavaScript, como feito no site da Alura. Assim, conseguimos visualizar o HTML da Alura e algumas informações pertinentes.

Copiar

\<\!DOCTYPE html\>

\<html lang\="pt-BR"\>

\<head\>

    \<meta charset\="UTF-8"\>

    \<meta name\="viewport" content\="width=device-width,initial-scale=1,minimum-scale=1.0"\>

    \<title\>Alura | Cursos online de Tecnologia\</title\>

    \<meta name\="description"

        content\="Aprenda Programação, Front-end, Back-end, Data Science, UX, DevOps, Inovação e Gestão na maior plataforma de tecnologia do Brasil"\>

    \<link rel\="canonical" href\="https://www.alura.com.br"\>

    \<link rel\="icon" href\="/assets/favicon.1790606030.ico"\>

    \<link rel\="preconnect" href\="https://fonts.googleapis.com"\>

    \<link rel\="preconnect" href\="https://fonts.gstatic.com" crossorigin\>

## **Explorando os cabeçalhos padrão do Postman**

A primeira delas são os *headers* (cabeçalhos) da requisição. Mesmo que não vejamos nenhum cabeçalho explícito, o Postman possui cabeçalhos padrão que são enviados em todas as requisições. É importante saber que, mesmo que não percebamos, o Postman pode estar enviando cabeçalhos. Esses são os cabeçalhos padrão que ele envia, como Cache-Control e Postman-Token, que são utilizados para o gerenciamento das requisições feitas pelo Postman.

Copiar

Cache-Control: no\-cache

Postman-Token: \<calculated when request is sent\>

Host: \<calculated when request is sent\>

User-Agent: PostmanRuntime/7.45.0

Accept: \*/\*

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

O cabeçalho Host é calculado quando a requisição é enviada, pois a URL pode ser alterada a qualquer momento. O User-Agent, por exemplo, não utiliza o Chrome ou Firefox, mas sim o próprio cliente HTTP do Postman em tempo real. Além disso, temos o Accept, Accept-Encoding e Connection.

## **Analisando a resposta HTTP e seus cabeçalhos**

Aqui estão algumas informações de requisição padrão que o Postman sempre faz. O mais importante é analisarmos os *headers* e o corpo da requisição que ele devolve. Temos o HTML e os *headers* associados a ele. Por exemplo, podemos ver o Content-Type, que é text/html, e o Charset ou *Encoding*, que é crucial, pois pode haver conflitos de codificação. Neste caso, está usando UTF-8. O servidor é o Cloudflare.

Copiar

Date                Thu, 21 Aug 2025 18:30:39 GMT

Content-Type        text/html; charset=UTF\-8

Transfer-Encoding   chunked

Connection          keep-alive

Server              cloudflare

Nel                 {"report\_to":"cf-nel","success\_fraction":0.0,"max\_age":604800}

Vary                Accept-Encoding

Expires             Thu, 21 Aug 2025 18:00:39 GMT

Cache-Control       public, max-age=1800

Report-To           {"group":"cf-nel","max\_age":604800,"endpoints":\[{...}\]}

CT-Cache-Status     DYNAMIC

Content-Encoding    br

Para identificar o corpo de uma resposta e de uma requisição, podemos observar dessa forma. No Postman, é possível ver toda a requisição na parte superior, que cuida da requisição, enquanto a parte inferior apresenta a resposta. O *status code* no Postman, por exemplo, apresenta 200 OK, indicando que a requisição foi bem-sucedida. Também podemos ver o tamanho da página web e o tempo que levou para processar o corpo da requisição.

## **Compreendendo o processo HTTP e introduzindo novos tópicos**

É importante compreender o processo HTTP como um todo. Podemos observar todas as partes de uma requisição. Neste caso, não houve corpo de requisição, pois não é necessário enviar nada; geralmente, o método GET não requer informações para envio. A resposta já contém um corpo, que é o próprio HTML recebido.

Para introduzir os próximos tópicos, se clicarmos no canto superior direito, onde há um símbolo semelhante ao HTML, que é o *code*, conseguimos ver o HTTP, que é o modelo padrão. Geralmente, o Postman abre por padrão o URL. Temos o HTTP, onde ele utiliza o método GET e a versão do HTTP, que é 1.1. Existem outras versões do HTTP, e será interessante discutirmos sobre elas posteriormente.

Copiar

GET / HTTP/1.1

Host: www.alura.com.br

