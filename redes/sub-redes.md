## Sub-Redes

Sub-redes são utilizadas para dividir uma rede maior em várias redes menores. Isso é feito para organizar melhor a rede, melhorar a segurança e otimizar o uso da largura de banda. Em uma empresa, por exemplo, diferentes departamentos como RH, Marketing e TI podem ter suas próprias sub-redes.

- **Comunicação entre Sub-redes**: As sub-redes podem se comunicar entre si se houver rotas estabelecidas.
- **Priorização de Redes**: É possível priorizar redes críticas, como a de TI, em detrimento de outras, como a de RH, devido à largura de banda disponível.

#### Host vs Sub-rede

- **Host**: Um host é qualquer dispositivo conectado a uma rede que pode enviar e receber dados, como um computador, servidor, impressora, ou smartphone. Cada host possui um endereço IP exclusivo dentro de uma rede.
- **Sub-rede**: Uma sub-rede é uma subdivisão lógica de uma rede maior. Ela permite que uma rede seja segmentada em partes menores e mais gerenciáveis, facilitando a administração, melhorando a segurança e otimizando o uso da largura de banda.

### Cálculo de Sub-Redes

#### Classes de Endereço IP

| CLASSE | 1° OCTETO | Parte da rede (N) e parte para hosts (H) | Máscara        | N° Redes        | Endereços por Rede           |
|--------|-----------|-----------------------------------------|----------------|------------------|------------------------------|
| A      | 1-127     | N.H.H.H                                 | 255.0.0.0      | 126 (2^7 - 2)    | 16,777,214 (2^24 - 2)        |
| B      | 128-191   | N.N.H.H                                 | 255.255.0.0    | 16,382 (2^14 - 2)| 65,534 (2^16 - 2)            |
| C      | 192-223   | N.N.N.H                                 | 255.255.255.0  | 2,097,150 (2^21 - 2)| 254 (2^8 - 2)         |
| D      | 224-239   | Multicast                               | NA             | NA               | NA                           |
| E      | 240-255   | Experimental                            | NA             | NA               | NA                           |

#### Cálculo de Sub-Rede

##### Exemplo:

| Decimal          | Binário                                    |
|------------------|--------------------------------------------|
| 192.168.10.1     | 11000000.10101000.00001010.00000001        |

Máscara de rede: Os 24 primeiros bits nunca mudarão. No exemplo acima, apenas o último conjunto de bits mudará.

- **Máscara de rede**: 192.168.10.0/24
- **Fórmula para Hosts de Redes**: (2^b) - 2, onde b é o número de bits disponíveis para hosts.

Para uma máscara de /24:
- 2^8 - 2 = 254 hosts disponíveis na rede.

##### Endereços Importantes:

- **Gateway**: O endereço usado pelos hosts na rede para se comunicarem com outros dispositivos fora da rede local.
- **Broadcast**: O endereço usado para enviar dados a todos os dispositivos em uma rede.
- **Host Address Range**: O intervalo de endereços IP disponíveis para atribuição a dispositivos na rede.
- **Subnet Address**: O primeiro endereço em uma sub-rede, usado para identificar a sub-rede.

### Exemplo de Sub-Rede

Dado o endereço IP 192.168.10.0/24:

- **Subnet Address**: 192.168.10.0
- **First Host**: 192.168.10.1
- **Last Host**: 192.168.10.254
- **Broadcast**: 192.168.10.255
- **Gateway**: Normalmente é o primeiro ou o último endereço disponível para hosts, como 192.168.10.1.

### Conclusão

A sub-rede é uma técnica essencial para a gestão eficiente de redes grandes, proporcionando melhor organização, segurança e controle de tráfego. O entendimento de como calcular sub-redes e configurar endereços IP adequados é crucial para qualquer profissional de redes.
