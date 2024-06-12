## IP, IPv4 e IPv6

### IP (Internet Protocol)

O Internet Protocol (IP) é o protocolo responsável pelo endereçamento e roteamento dos pacotes de dados na camada 3 do modelo OSI. Ele atribui um endereço único a cada dispositivo conectado à internet, permitindo que os dados sejam enviados e recebidos corretamente entre dispositivos.

#### Função do IP
- **Endereçamento**: Cada dispositivo recebe um endereço IP único.
- **Roteamento**: O roteador utiliza esses endereços IP para determinar o melhor caminho para enviar os pacotes de dados ao destino correto.

### IPv4

O IPv4 é a quarta versão do protocolo IP, amplamente utilizada para endereçamento na internet. Ele usa um formato de 32 bits dividido em 8 octetos, onde cada octeto pode variar de 0 a 255.

#### Exemplo de Endereço IPv4
`192.168.0.1`

#### Características do IPv4
- **Formato**: 32 bits (dividido em 8 octetos).
- **Capacidade**: Permite até aproximadamente 4,3 bilhões de endereços únicos.

#### Problema de Escassez de Endereços
Devido ao crescimento exponencial da internet, o número de endereços IPv4 disponíveis começou a se esgotar.

#### Solução NAT (Network Address Translation)
Para mitigar a escassez de endereços IPv4, foi implementado o NAT, que permite que vários dispositivos em uma rede local compartilhem um único endereço IP público fornecido pelo ISP (Internet Service Provider).

### IPv6

O IPv6 é a sexta versão do protocolo IP, desenvolvida para resolver os problemas de escassez de endereços do IPv4. Ele usa um formato de 128 bits dividido em 16 grupos de 4 caracteres hexadecimais.

#### Exemplo de Endereço IPv6
`1050:0000:0000:0000:0005:0600:300c:326b` ou `1050:0:0:0:5:600:300c:326b`

#### Características do IPv6
- **Formato**: 128 bits (dividido em 16 grupos).
- **Capacidade**: Permite até mais de 340 undecilhões de endereços (`3.4 x 10^38`).

#### Implementação do IPv6
- **Roteadores**: Já é comum roteadores utilizarem IPv6 para roteamento entre si.
- **Usuários Finais**: Ainda não está amplamente presente entre os usuários finais devido à complexidade de configuração e à necessidade de substituir equipamentos antigos.

### IP Público vs IP Privado

#### IP Público
Um endereço IP público é utilizado para identificar dispositivos acessíveis diretamente pela internet. Ele é atribuído pelo ISP e é único globalmente.

#### IP Privado
Endereços IP privados são usados dentro de redes locais e não são roteáveis na internet. Exemplos comuns de faixas de IP privado incluem `192.168.0.0 - 192.168.255.255`.

### Conclusão

O IPv4 tem sido o principal protocolo de endereçamento da internet por décadas, mas devido à escassez de endereços, o IPv6 foi desenvolvido para fornecer um número praticamente ilimitado de endereços. A transição para o IPv6 é gradual e contínua, com muitos roteadores e redes já suportando o novo protocolo, embora a adoção completa ainda esteja em andamento.
