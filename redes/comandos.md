## Principais Comandos de Rede

### ipconfig

O comando `ipconfig` é usado para exibir e gerenciar a configuração IP dos adaptadores de rede em um sistema operacional Windows. Ele mostra informações detalhadas sobre os adaptadores de rede, incluindo endereços IP, máscaras de sub-rede e gateways padrão.

#### Sintaxe
```bash
ipconfig
```

#### Exemplo de Saída
```bash
Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::d4a8:6435:d2d8:d9f3%12
   IPv4 Address. . . . . . . . . . . : 192.168.0.105
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.0.1
```

### ipconfig /flushdns

O comando `ipconfig /flushdns` é usado para limpar o cache DNS do cliente, eliminando todos os registros armazenados temporariamente que foram obtidos através de consultas DNS. Isso pode ser útil para resolver problemas de conectividade ou quando mudanças no DNS foram feitas e precisam ser refletidas imediatamente.

#### Sintaxe
```bash
ipconfig /flushdns
```

#### Exemplo de Saída
```bash
Successfully flushed the DNS Resolver Cache.
```

### ping

O comando `ping` é usado para testar a conectividade entre dois dispositivos na rede. Ele envia pacotes ICMP Echo Request para o endereço IP especificado e espera por pacotes de resposta. É útil para diagnosticar problemas de rede e verificar se um host está ativo.

#### Sintaxe
```bash
ping [endereço IP ou nome do host]
```

#### Exemplo
```bash
ping google.com
```

#### Exemplo de Saída
```bash
Pinging google.com [172.217.29.174] with 32 bytes of data:
Reply from 172.217.29.174: bytes=32 time=22ms TTL=53
Reply from 172.217.29.174: bytes=32 time=23ms TTL=53
```

### nslookup

O comando `nslookup` é usado para consultar servidores DNS e obter detalhes sobre os nomes de domínio, como endereços IP associados. É útil para resolver problemas de DNS e verificar se os registros DNS estão corretos.

#### Sintaxe
```bash
nslookup [nome do domínio]
```

#### Exemplo
```bash
nslookup google.com
```

#### Exemplo de Saída
```bash
Server:  dns.google
Address:  8.8.8.8

Non-authoritative answer:
Name:    google.com
Addresses:  172.217.29.174
```

### tracert

O comando `tracert` (ou `traceroute` em sistemas Unix) é usado para rastrear o caminho que os pacotes de dados seguem até um destino especificado. Ele exibe cada salto (roteador ou dispositivo) que o pacote atravessa, junto com o tempo de resposta.

#### Sintaxe
```bash
tracert [endereço IP ou nome do host]
```

#### Exemplo
```bash
tracert google.com
```

#### Exemplo de Saída
```bash
Tracing route to google.com [172.217.29.174] over a maximum of 30 hops:

  1     2 ms     1 ms     1 ms  192.168.0.1
  2    10 ms     9 ms    10 ms  10.0.0.1
  3    22 ms    23 ms    21 ms  172.217.29.174
```

### route print

O comando `route print` exibe a tabela de roteamento IP do sistema. Ele mostra as rotas conhecidas pelo computador, incluindo as rotas para as redes locais e os gateways configurados.

#### Sintaxe
```bash
route print
```

#### Exemplo de Saída
```bash
===========================================================================
Interface List
 12...00 1c 42 00 00 08 ......Intel(R) Ethernet Connection
  1...........................Software Loopback Interface 1
===========================================================================
IPv4 Route Table
===========================================================================
Active Routes:
Network Destination        Netmask          Gateway       Interface  Metric
          0.0.0.0          0.0.0.0      192.168.0.1    192.168.0.105    281
        127.0.0.0        255.0.0.0        On-link       127.0.0.1    331
```

### netstat

O comando `netstat` exibe várias estatísticas e informações sobre as conexões de rede ativas, incluindo conexões TCP, portas nas quais o computador está ouvindo e outras informações de rede.

#### Sintaxe
```bash
netstat
```

#### Exemplo de Saída
```bash
Active Connections

  Proto  Local Address          Foreign Address        State
  TCP    192.168.0.105:50455    ec2-54-235-45-44:https  ESTABLISHED
  TCP    192.168.0.105:50456    ec2-52-55-122-200:https ESTABLISHED
```

### Conclusão

Os comandos de rede são ferramentas essenciais para diagnóstico, configuração e resolução de problemas de rede. Cada comando tem uma função específica, seja para exibir configurações de rede, testar conectividade, resolver nomes de domínio ou rastrear rotas na rede. A familiaridade com esses comandos é crucial para administradores de sistemas e profissionais de TI.
