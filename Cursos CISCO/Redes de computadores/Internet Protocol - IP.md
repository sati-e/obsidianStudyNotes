#redes #cybersec 
Atualmente a maioria dos computadores utilizam dual stack, uma tecnologia de rede que permite o uso do IPv4 e do IPv6 em um mesmo dispositivo.
<br>
Na prática, normalmente quem define a rede lógica é o roteador, pois é quem conecta a rede local com a internet. Mas pode ser o DHCP, administradores, firewall, switch...
<br>
Roteamento = tecnologia que permite computadores em redes lógicas diferentes se comuniquem
<br>
##### IPs
- Endereço lógico
- Identifica um host específico
- Há **uma parte que identifica a rede**.
- Há **uma parte que identifica o host/dispositivo** dentro dessa rede.
- A diferença principal é que **IPv6 tem 128 bits** (muito mais endereços possíveis) enquanto o **IPv4 tem 32 bits**.
- Possui [[Dicionário|máscara de sub-rede]]
Precisa ser configurado dentro da LAN, e mundialmente, para fornecer comunicações, locais e remotas.
>Um endereço IP é atribuído à conexão da [[Dicionário |interface de rede]] de um host *(identifica, fazendo com que os dispositivos saibam para onde enviar os dados)*
  - Cada pacote enviado pela internet tem um endereço IP de origem e destino

##### IPv4
Cada  pacote enviado pela internet tem um PIv4 de origem e destino
- 32 bits agrupados em 4 bytes (8 bits)
Ex binário:  `11010001.10100101.11001000.00000001`
Ex decimal: `209.165.200.1`
- Hierárquico:
**Ex:** `IP: 192.168.1.10`
**Parte da rede:** `192.168.1` → todos os dispositivos dessa rede têm essa parte igual.
**Parte do host:** 10 → identifica **esse dispositivo específico** dentro da rede `192.168.1.0.`
<br>
## Tipos de endereço IP - transmissão
- Unicast
- Broadcast
- Multicast
##### Unicast
Um pacote IP sempre sai de um único dispositivo, por isso **o endereço de origem é unicast.**
O protocolo IP exige que o remetente seja um único host identificável.
- Comunicações um-para-um

##### Broadcast
Envia o pacote para todos os dispositivos em uma rede
Para criar um endereço broadcast, a parte de redes continua igual, e é colocado todos os bits da parte do host como 1
Ex: Rede: `192.168.1.0/24` *(o "`/24`" indica que a máscara tem 24 bits)*
Máscara: `255.255.255.0`
Parte de host: últimos 8 bits *(`0` a `255`)*
**Endereço de broadcast**: `192.168.1.255` *(todos os bits da parte de host = 1)*
- Comunicações um-para-todos
**Direcionado:** Enviado para todos os hosts de uma rede específica
**Limitado:** Enviado para todos os host da rede local, sem precisar reconhecer o endereço de rede *(destino: `255.255.255.255`)*
- Roteadores não encaminham broadcast por padrão, evitando tráfego desnecessário
>[!Warning] Não existe no IPv6

##### Multicast
Permite que o host envie um pacote para um conjunto de host selecionados, que participem de um multicast.
- Os host que recebem são chamados de clientes multicast, eles precisam estar inscritos no grupo multicast. *(Lógica de inscrição e gerenciamento feita por software)*
- Casa grupo multicast é representado por um único endereço multicast de destino
- IPv4 reservou o intervalo `24.0.0.0` a `239.255.255.255` para multicast, cada grupo tem um endereço dentro deste intervalo.
Ex: `224.1.1.1` é um endereço multicast, mas não pertence a nenhum dispositivo específico. Ele representa **um grupo de dispositivos** que se inscreveram para receber pacotes destinados a esse endereço, ou seja, quando alguém envia um pacote para `224.1.1.1`, todos os dispositivos da lista recebem o pacote.
:LiCornerDownRight: Cada dispositivo do grupo **continua tendo seu IP unicast normal**, mas também “ouve” o endereço multicast do grupo.

## Tipos de IPv4 - Públicos e privados
##### :LiLockKeyholeOpen: Públicos
Acessível pela internet
- Único na internet
- Atribuído ao roteador/dispositivo pelo provedor de internet *(ISP, normalmente)*
- Pode ser acessado por qualquer outro dispositivo *(desde que não haja bloqueios)*
- Necessário para hospedar um site ou serviço acessível no mundo todo

##### :LiLockKeyhole: Privados
Foram introduzidos devido ao esgotamento de espaço de endereços *(antes do IPv6)*
A maioria das redes internas usa endereços privados para endereçar dispositivos internos, mas não são globalmente roteáveis.
- Reservados pela RFC 1918 *(Request for Comments)*, padronizou as faixas dedicadas para uso interno:

| Endereços e prefixos da rede | Intervalo de endereços provados RFC 1918 |
| :--------------------------- | ---------------------------------------- |
| `10.0.0.0/8`                 | `10.0.0.0 – 10.255.255.255`              |
| `172.16.0.0/12`              | `172.16.0.0 – 172.31.255.255`<br>        |
| `192.168.0.0/16`             | `192.168.0.0 – 192.168.255.255`          |
>[!Warning] Eles não são únicos, então nenhum roteador na internet deve encaminhar pacotes vindo destes endereços
- Não exclusivos
<br>
*Mas como tudo isso funciona?*
🏡 ***Em casa***
- O **roteador** recebe do provedor **um IP público** (ex: `187.55.32.101`).
- O roteador cria uma **rede local (LAN)** e distribui **IPs privados** pros seus dispositivos via **DHCP**:
PC: `192.168.0.10`
Celular: `192.168.0.11`
TV: `192.168.0.12`
- Todos eles saem pra internet usando **NAT**, aparecendo como o mesmo IP público do roteador.
<br>
## Roteamento para a Internet - NAT
##### Endereço IPv4 Privado e Network Address Translation (NAT)
Os pacotes com endereço privado não são roteáveis na internet pública, por isso os endereços de origem precisam precisam ser **traduzidos** para um endereço público antes de encaminhar o pacote para um [[Dicionário|ISP]] 
Também permite a tradução de endereços IPs de dispositivos em diferentes redes, para que possam se comunicar uns com os outros como se estivessem na mesma rede.
##### Conversão de Endereços de Rede - NAT
Converte endereços IPv4 privados e púbicos *(geralmente feito no **roteador** que conecta a rede interna à rede ISP)*
- Conserva endereços IP
- Maior segurança
- Economia de custo
- Administração de rede mais fácil
###### NAT estático
Usado principalmente em servidores que precisam ser acessíveis pela internet *(web, email...)*
- Cada IP interno tem um IP público exclusivo *(mapeamento individual)*
>[!Warning] Pouco prático em redes domésticas, porque o IP público é caro e limitado
###### NAT Dinâmico
Usado principalmente em redes que precisam de conectividade de saída com a internet

<br>
<br>
##### Anotações pessoais
Analogia sobre como funciona o IP e links:
- **O link** é como um mapa de um baú na internet, ele indica onde o baú está.
- **O conteúdo do baú** é o que você quer acessar
- **Você** é a pessoa que tem a chave (seu IP ou sessão), que permite **pegar o conteúdo** e trazê-lo até você.
Então: **você precisa saber onde está o baú e ter a chave certa para pegar o tesouro.**
<br>
Referências adicionais: https://www.fortinet.com/br/resources/cyberglossary/network-address-translation