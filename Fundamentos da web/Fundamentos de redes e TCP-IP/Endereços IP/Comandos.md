Na aula, foram utilizados os seguintes comandos no terminal:

1.  **`ping alura.com.br`**
    *   **O que faz:** Este comando é usado para verificar a conectividade com um endereço de rede (neste caso, `alura.com.br`) e medir o tempo que os pacotes de dados levam para ir e voltar. Ele utiliza o endereço IP para localizar o destino e verificar se ele está acessível. É útil para testar se um site ou servidor está online e respondendo.

2.  **`netstat -an | findstr :443`**
    *   **O que faz:** Este comando é usado para exibir as conexões de rede ativas.
        *   `netstat -an`: Mostra todas as conexões e portas de escuta em formato numérico (sem resolver nomes de host).
        *   `| findstr :443`: Filtra os resultados para mostrar apenas as linhas que contêm `:443`, que é a porta padrão para o protocolo HTTPS. Ou seja, ele lista todas as conexões TCP estabelecidas que estão usando a porta 443.

3.  **`netstat -an | findstr :80`**
    *   **O que faz:** Semelhante ao comando anterior, mas filtra as conexões para a porta `:80`, que é a porta padrão para o protocolo HTTP. Ele lista todas as conexões TCP estabelecidas que estão usando a porta 80.

4.  **`tracert -h 60 alura.com.br`**
    *   **O que faz:** Este comando rastreia a rota que os pacotes de dados levam para chegar a um destino na rede.
        *   `tracert`: É o comando principal para rastrear a rota.
        *   `-h 60`: Define o número máximo de "saltos" (ou roteadores) que o comando tentará alcançar antes de desistir. Neste caso, 60 saltos.
        *   `alura.com.br`: É o endereço de destino.
    *   Ele mostra cada roteador (com seu respectivo IP) pelo qual os dados passam até chegar ao servidor da Alura, funcionando como um "GPS" da internet.

5.  **`tracert -h 60 amazon.es`**
    *   **O que faz:** Funciona exatamente como o comando `tracert` anterior, mas rastreia a rota até o site da Amazon na Espanha (`amazon.es`), mostrando o caminho diferente que os dados percorrem para chegar a um destino internacional.

6.  **`curl -4 google.com.br`**
    *   **O que faz:** Este comando é uma ferramenta para transferir dados de ou para um servidor.
        *   `curl`: É o comando principal.
        *   `-4`: Força o `curl` a usar o protocolo IPv4 para a conexão.
        *   `google.com.br`: É o endereço do site a ser acessado.
    *   Ele faz uma requisição ao site do Google usando IPv4 e exibe a resposta do servidor.

7.  **`curl -6 google.com.br`**
    *   **O que faz:** Semelhante ao comando `curl` anterior, mas tenta forçar o uso do protocolo IPv6 para a conexão.
        *   `curl`: É o comando principal.
        *   `-6`: Força o `curl` a usar o protocolo IPv6.
        *   `google.com.br`: É o endereço do site a ser acessado.
    *   Na aula, este comando demonstrou que o site do Google ainda não suportava IPv6 para essa requisição, resultando em uma mensagem de erro de resolução de host.

Esses comandos são ferramentas poderosas para entender e diagnosticar a conectividade e o fluxo de dados em redes.

