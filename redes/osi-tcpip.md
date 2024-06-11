## Modelo OSI e TCP/IP

### Modelo OSI (Open System Interconnection)
O modelo OSI é uma norma que define uma estrutura de comunicação segmentada em 7 camadas distintas. Cada camada desempenha uma função específica na transmissão de dados entre dispositivos de rede, desde a camada física até a camada de aplicação. Nem toda comunicação necessariamente utiliza todas essas camadas, mas elas fornecem uma estrutura conceitual para entender como a comunicação em rede pode ser organizada e gerenciada.

![Modelo OSI](https://media.graphcms.com/output=format:png/resize=,width:858,height:494/XJuH7NlvRu2CPRAgC5AV)

#### 1. Física
Esta camada trata dos aspectos físicos da comunicação, incluindo os cabos, switches, roteadores e qualquer outro hardware físico que permite a conexão. Também inclui especificações sobre Ethernet, latência permitida e velocidade de transmissão.

#### 2. Enlace
A camada de enlace é responsável pela fragmentação dos pacotes em quadros, que são então enviados ao destino. Utiliza endereços MAC (Media Access Control) para identificar de forma única os dispositivos na rede, otimizando a transmissão de dados no nível de enlace.

#### 3. Rede
A camada de rede é primordial para a comunicação, pois é aqui que ocorre o envio dos pacotes através dos roteadores, que redirecionam os dados até o destino final. Cada pacote contém informações de roteamento necessárias para chegar ao destino.

#### 4. Transporte
Responsável por estabelecer a conexão com o destinatário final através dos protocolos TCP e UDP:
- **TCP (Transmission Control Protocol)**: Envia dados em segmentos que incluem informações sobre o que está sendo enviado, de onde e para onde. Requer confirmação de recebimento, garantindo uma conexão mais segura, ideal para e-mails e outras comunicações críticas.
- **UDP (User Datagram Protocol)**: Envia dados sem solicitar confirmação de recebimento, proporcionando maior velocidade, ideal para transmissões ao vivo e chamadas de vídeo.

#### 5. Sessão
Estabelece, gerencia e termina as sessões entre os dispositivos de origem e destino. Define a duração e a forma como os dados serão enviados.

#### 6. Apresentação
Cuida da criptografia e da decriptografia dos dados, garantindo uma conexão segura. Converte os dados da aplicação em um formato adequado para a transmissão ou converte os dados recebidos em um formato que a aplicação possa entender.

#### 7. Aplicação
A camada mais próxima do usuário, inclui protocolos e serviços como DNS (Domain Name System), HTTP (Hypertext Transfer Protocol) e SSH (Secure Shell).

### Modelo TCP/IP
O modelo TCP/IP é mais prático e amplamente utilizado na comunicação em redes modernas. Ele é dividido em 4 camadas, mas é conceitualmente semelhante ao modelo OSI, agrupando algumas das funções do OSI em menos camadas.

![Modelo TCP/IP](https://www.dltec.com.br/blog/wp-content/uploads/2019/02/osi-tcp-ip.png)

#### 1. Aplicação
Combina as funções das camadas de aplicação, apresentação e sessão do modelo OSI. Inclui protocolos como HTTP, FTP, SMTP e DNS, que permitem a interação direta com o usuário e a gestão de dados.

#### 2. Transporte
Equivale à camada de transporte do modelo OSI, utilizando os protocolos TCP e UDP para garantir a entrega dos dados entre os dispositivos.

#### 3. Internet
Corresponde à camada de rede do modelo OSI. Trata do endereçamento e roteamento dos pacotes de dados através da internet, utilizando protocolos como IP (Internet Protocol).

#### 4. Acesso à Rede
Combina as camadas física e de enlace do modelo OSI, lidando com a transmissão dos dados sobre o meio físico da rede e a ligação entre os dispositivos.

### Conclusão
Ambos os modelos OSI e TCP/IP fornecem estruturas importantes para a compreensão e a implementação de redes de comunicação. O modelo OSI, com suas sete camadas, oferece uma visão detalhada e segmentada de cada aspecto da comunicação em rede, enquanto o modelo TCP/IP, com suas quatro camadas, é mais direto e amplamente aplicado na prática das redes modernas. Compreender esses modelos é essencial para projetar, gerenciar e solucionar problemas em redes de computadores.
