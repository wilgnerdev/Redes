## Comandos bash para entender o protocolo TCP/IP

O **TCP/IP** é a base da comunicação em redes modernas, incluindo a internet. Ele é formado por uma pilha de protocolos que garante desde a identificação de dispositivos até a entrega confiável de pacotes de dados. Para estudar e entender como o TCP/IP funciona na prática, o Linux e o Bash oferecem diversos comandos que permitem inspecionar conexões, interfaces e fluxos de rede.

### **Principais comandos**

* **ifconfig ou ip addr**  
  Exibe informações sobre interfaces de rede, endereços IP atribuídos e status da conexão.  
  Exemplo:

ip addr show

*   
* **ping**  
  Testa a conectividade entre o host local e outro dispositivo, usando o protocolo **ICMP**.  
  Exemplo:

ping google.com

*   
* **traceroute**  
  Mostra o caminho percorrido pelos pacotes até um destino, revelando cada roteador intermediário.  
  Exemplo:

traceroute google.com

*   
* **netstat ou ss**  
  Exibe conexões ativas, portas abertas e estatísticas de rede. O ss é mais moderno e recomendado.  
  Exemplo:

ss \-tulnp

*   
* **tcpdump**  
  Captura pacotes em tempo real, permitindo analisar tráfego detalhado no nível TCP/IP.  
  Exemplo (capturando pacotes na porta 80):

sudo tcpdump \-i any port 80

*   
* **curl**  
  Realiza requisições HTTP/HTTPS e pode ser usado para inspecionar cabeçalhos e verificar protocolos.  
  Exemplo:

curl \-I https://www.example.com

*   
* **nmap**  
  Scanner de rede usado para descobrir hosts ativos e verificar portas abertas.  
  Exemplo:

nmap \-Pn 192.168.1.1

* 

### **Referências**

* Guia da **GNU/Linux iproute2** (substituto do ifconfig): [https://man7.org/linux/man-pages/man8/ip.8.html](https://man7.org/linux/man-pages/man8/ip.8.html)  
* Manual do **tcpdump**: [https://www.tcpdump.org/manpages/tcpdump.1.html](https://www.tcpdump.org/manpages/tcpdump.1.html)  
* Documentação do **ss/netstat**: [https://man7.org/linux/man-pages/man8/ss.8.html](https://man7.org/linux/man-pages/man8/ss.8.html)  
* Projeto **nmap**: [https://nmap.org](https://nmap.org/)  
* Tutorial de redes Linux no DigitalOcean: [https://www.digitalocean.com/community/tutorials](https://www.digitalocean.com/community/tutorials)

