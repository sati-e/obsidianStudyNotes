Os endereços podem ser atribuídos estática ou dinamicamente
## Estático
O administrados de rede deve configurar manualmente as informações da rede para um host, com no mínimo:
- Endereço IP *(Identifica o computador na rede)*
- Mascara de sub-rede *(Identifica a rede conectada)*
- Gateway padrão *(Identifica a saída de rede)*
Ele é um endereço fixo e permanente na rede, utilizando quando **algo precisa ser localizado no mesmo endereço sempre.** Empresas, administradores de servidores e contas precisam dele para hospedar seus próprios servidores e gerenciá-los.
**Ex:** Servidores, recursos compartilhados *(impressoras, scanners...)*, dispositivos de automação IoT...
###### :LiCheck: Vantagem
- Melhor resolução de nomes online *(descobertos e acessados de forma confiável por meio de seus nomes de host)*
- Acesso em qualquer lugar e a qualquer hora
- Menos interrupções na conexão
- Dados precisos de geolocalização
###### :LiX: Desvantagem
- Fáceis de rastrear
- Custo
- Dificuldade pós-violação
## Dinâmico
Os provedores ISPs atribuem temporariamente um endereço IP dinâmico por meio do servidor DHCP. 
##### DHCP - Dynamic Host Configuration Protocol
Redes de residências normalmente usam um modem e um roteador sem fio, o roteador sem fio neste caso é tanto o servidor para hosts internos na LAN e como o cliente DHCP, recebendo a configuração do ISP, distribui endereços privados para os hosts internos.
Fornece um mecanismo para atribuir informações de endereços automaticamente.
O endereço não é permanentemente atribuído, se o host desliga ou se retira da rede o endereço retorna o pool para ser reutilizado.
**Fluxo básico entre um cliente DHCP e o servidor DHCP:**
1. **Discover:** O cliente envia uma mensagem de broadcast procurando por servidores DHCP na rede.
2. **Offer:** O servidor DHCP responde oferecendo um endereço IP e outras configurações de rede.
3. **Request:** O cliente escolhe uma das ofertas e envia uma solicitação formal ao servidor.
4. **Ack (Acknowledgement):** O servidor confirma a atribuição do IP ao cliente.

>[!Warning] O IPv6 utiliza o SLAAC - Stateless Address Autoconfiguration, o DHCPv6 pode ser utilizado em conjunto fornecendo detalhes extras, como servidores DNS específicos
###### :LiCheck: Vantagem
- Redução de custos
- Segurança aprimorada
- Maior flexibilidade
- Menos conflitos de endereços
###### :LiX: Desvantagem
- Problemas de hospedagem *(problemas com DNS)*
- Baixa confiabilidade técnica *(ineficaz para atividades online com alto consumo de dados)*

<br>
<br>
ref: https://www.fortinet.com/resources/cyberglossary/static-vs-dynamic-ip