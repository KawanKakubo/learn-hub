## Segurança em Redes

A segurança em redes é essencial para proteger dados, sistemas e dispositivos contra ameaças internas e externas. A segurança pode ser dividida em duas categorias principais: segurança física e segurança lógica.

### Segurança Física

A segurança física envolve proteger o hardware e outros componentes físicos da rede.

- **Localização do Hardware**: O hardware deve estar em um local seguro, longe de acessos não autorizados.
- **Refrigeração Adequada**: Equipamentos de rede, como servidores, precisam de refrigeração adequada para evitar superaquecimento e falhas.
- **Backup**: Armazenar backups em locais seguros, tanto fisicamente quanto virtualmente, é crucial. Exemplos incluem cofres físicos ou serviços de armazenamento em nuvem como AWS S3 ou Google Drive.
- **Redirecionamento de Servidor (Load Balancer)**: Em caso de falha de um servidor, um load balancer pode redirecionar o tráfego para outro servidor, garantindo continuidade do serviço.
- **Atualização de OS**: Manter os sistemas operacionais e softwares atualizados para proteger contra vulnerabilidades conhecidas.
- **Desativar Entradas de Periféricos**: Desativar entradas de periféricos nos servidores pode prevenir acesso não autorizado.
- **Controle de Acesso Físico**: Implementar métodos de controle de acesso, como autenticação facial, para restringir o acesso ao hardware.
- **Senhas Complexas**: Utilizar senhas complexas e armazená-las em locais seguros, como cofres físicos ou gerenciadores de senhas como LastPass ou 1Password, em vez de um notepad.

### Segurança Lógica

A segurança lógica envolve proteger os dados e sistemas contra acessos não autorizados e ataques cibernéticos.

- **Single Sign-On (SSO)**: Permite que os usuários acessem múltiplos sistemas com uma única autenticação, facilitando o gerenciamento de senhas e melhorando a segurança.
- **Implementação de Firmware**: Utilizar firmwares para monitorar quem entra na rede, para onde estão indo e com o que estão acessando.
- **Normas de ACL**: Definir normas de Listas de Controle de Acesso (ACL) explícitas para controlar quem pode acessar quais recursos na rede.
- **Conexões Criptografadas**: Utilizar criptografia de ponta a ponta, como VPNs, para proteger a troca de dados entre filiais distantes.
- **Tipos de VPN**: Existem várias VPNs, como VPN de acesso remoto e VPN site-to-site, cada uma com suas próprias aplicações e vantagens.

### Ataques

A compreensão dos tipos de ataques é crucial para implementar medidas de segurança eficazes.

- **DDoS (Distributed Denial of Service)**: Um ataque que sobrecarrega um servidor com tráfego de múltiplas fontes, tornando-o inacessível para os usuários legítimos.
- **Ransomware**: Malware que criptografa os dados da vítima e exige um resgate para liberar o acesso.
- **SQL Injection**: Um ataque que insere código SQL malicioso em uma consulta de banco de dados, permitindo ao atacante acessar ou manipular dados.

### Segurança em Wireless

Segurança em redes wireless é essencial devido à sua natureza aberta e vulnerável a ataques.

- **Bandas de Frequência**: Utilizar bandas de frequência organizadas e divididas, como 2.4GHz e 5GHz, para melhorar a transmissão de dados.
- **Redes Separadas para Clientes e Empresa**: Ter duas redes separadas, uma para clientes e outra para a empresa, pode proteger os dados sensíveis e melhorar a segurança.
- **Firmware Atualizado e Senhas Fortes**: Manter o firmware dos roteadores atualizado e utilizar senhas fortes para proteger a rede.

### Conclusão

A segurança em redes é um campo complexo e multifacetado que requer atenção tanto à segurança física quanto à lógica. Implementar boas práticas de segurança, entender os tipos de ataques e proteger redes wireless são passos essenciais para proteger dados e sistemas de ameaças.
