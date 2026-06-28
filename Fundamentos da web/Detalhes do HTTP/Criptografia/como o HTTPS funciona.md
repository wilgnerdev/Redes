## Como o HTTPS funciona?

O **HTTPS (Hypertext Transfer Protocol Secure)** é a versão segura do protocolo HTTP, amplamente utilizado na web para garantir que a comunicação entre navegador e servidor seja confidencial e protegida contra ataques. Ele adiciona uma camada de segurança baseada em **SSL/TLS (Secure Sockets Layer / Transport Layer Security)**.

### **Como funciona o HTTPS**

1. **Conexão inicial (handshake TLS)**  
   Quando um cliente (como o navegador) acessa um servidor via HTTPS, ocorre o chamado *handshake*. Nesse processo, as partes negociam algoritmos de criptografia e o servidor envia um **certificado digital** para comprovar sua identidade.  
2. **Verificação do certificado**  
   O navegador verifica se o certificado foi emitido por uma **Autoridade Certificadora (CA)** confiável. Isso assegura que o site realmente é quem diz ser, evitando ataques de falsificação (como phishing ou man-in-the-middle).  
3. **Troca de chaves**  
   Durante o handshake, o cliente e o servidor trocam informações para gerar uma **chave de sessão**. Essa chave será usada para criptografar toda a comunicação de forma simétrica, garantindo velocidade e segurança.  
4. **Transmissão segura de dados**  
   Com a chave de sessão estabelecida, todas as informações trocadas (como logins, senhas e dados pessoais) são criptografadas. Assim, mesmo que alguém intercepte o tráfego, não conseguirá ler os dados.

### **Benefícios do HTTPS**

* **Confidencialidade**: dados transmitidos não podem ser lidos por terceiros.  
* **Integridade**: evita que informações sejam alteradas durante a transmissão.  
* **Autenticidade**: confirma que o servidor acessado é realmente o correto.  
* **SEO e confiança**: navegadores modernos marcam sites sem HTTPS como inseguros, e buscadores dão preferência a sites seguros nos resultados.

---

### **Referências**

* Guia da Mozilla sobre **HTTPS**: [https://developer.mozilla.org/docs/Web/HTTP/HTTPS](https://developer.mozilla.org/docs/Web/HTTP/HTTPS)  
* Documentação do **TLS 1.3** no IETF: [https://datatracker.ietf.org/doc/html/rfc8446](https://datatracker.ietf.org/doc/html/rfc8446)  
* Let’s Encrypt (CA gratuita e automatizada): [https://letsencrypt.org](https://letsencrypt.org/)  
* Google Security Blog sobre o impacto do HTTPS: [https://security.googleblog.com](https://security.googleblog.com/)

