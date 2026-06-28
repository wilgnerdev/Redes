## Tipos de protocolos de API

As **APIs (Application Programming Interfaces)** são fundamentais para a comunicação entre sistemas, permitindo a integração de serviços, dados e funcionalidades. Existem diferentes protocolos de API, cada um com características próprias, que influenciam no desempenho, segurança e facilidade de implementação.

* **REST (Representational State Transfer)**  
  Baseado no protocolo HTTP, é o padrão mais popular atualmente. Utiliza recursos identificados por URLs e operações baseadas em métodos HTTP (GET, POST, PUT, DELETE). É simples, escalável e amplamente suportado.  
* **SOAP (Simple Object Access Protocol)**  
  Mais antigo e formal, utiliza XML para troca de mensagens. É orientado a contratos (WSDL) e conhecido pela robustez em ambientes corporativos, mas também pela maior complexidade em comparação ao REST.  
* **GraphQL**  
  Criado pelo Facebook em 2015, permite ao cliente definir exatamente quais dados deseja receber, evitando overfetching (trazer dados em excesso) ou underfetching (trazer dados insuficientes). É altamente flexível para aplicações modernas.  
* **gRPC (Google Remote Procedure Call)**  
  Desenvolvido pelo Google, utiliza **Protocol Buffers (Protobuf)** para serialização de dados binários, o que garante alta performance e baixo consumo de rede. É muito usado em microsserviços e comunicação em tempo real.  
* **WebSockets**  
  Não é um protocolo de API no sentido clássico, mas um padrão para comunicação **bidirecional em tempo real** entre cliente e servidor. Ideal para chats, jogos online e sistemas de monitoramento.

---

### **Referências**

* Documentação oficial do **REST**: [https://restfulapi.net](https://restfulapi.net/)  
* Guia da **W3C** sobre **SOAP**: [https://www.w3.org/TR/soap](https://www.w3.org/TR/soap)  
* **GraphQL** oficial: [https://graphql.org](https://graphql.org/)  
* **gRPC** oficial: [https://grpc.io](https://grpc.io/)  
* **WebSockets** MDN: [https://developer.mozilla.org/docs/Web/API/WebSockets\_API](https://developer.mozilla.org/docs/Web/API/WebSockets_API)

